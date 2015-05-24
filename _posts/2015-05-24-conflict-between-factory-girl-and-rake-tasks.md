---
published: true
layout: post
tags: 
  - programming
  - rake
  - factory girl
category: articles
comments: true
title: "Conflict between FactoryGirl and Rake tasks"
---

I'm riding the wave and getting into [Docker](https://www.docker.com/). So far, it seems like an excellent tool. My first experiment was running a container with Postgres which would serve as a testing database when running [RSpec](http://rspec.info/).

I managed to set it up, get the connection working, change the database configuration in the Rails project to connect to it. A problem occurred when I tried to load the database schema into it with `RAILS_ENV=test rake db:schema:load`. Suddenly I started getting errors about being unable to connect to Redis. WTF?

The source of the problem wasn't hard to find (sort of), but a little bit unexpected. In [Enectiva](http://www.enectiva.cz/en/about-enectiva) we have many monitoring Rake tasks with gather data and report the status of the application. One of them monitors the status of [Resque](https://github.com/resque/resque) (eg. how many tasks have been process in the last X minutes, how many jobs are queued) and stores it in a database. The task initializes instance of a model and sets values for individual fields/metrics. Some of them are simply copied from Resque, some require a little preprocessing. Those in the second group have helper methods defined within the task and the names mirror the fields. So far so good.

For testing, [FactoryGirl](https://rubygems.org/gems/factory_girl) generates functions for setting up factories. That includes the model used to store the metrics. Therefore it defines methods named the same way as metrics (that's what it's supposed to do) and the same as the helper methods within the Rake task. 

Both components define the methods in the global namespace and therefore override each other. It makes sense, but Rake DSL with `namespace` method make it a little misleading. There are several possible solutions:

1. Rename the helper functions in the task - it's a hacky solution, but very simple
2. Wrap the whole task in a `module` - this doesn't really work, because `Rake::DSL#namespace` and `Rake::DSL#task` are defined as private and [then patched onto the global namespace](https://github.com/ruby/rake/blob/master/lib/rake/dsl_definition.rb#L201) which makes it really hard to call them from within a module
3. Wrap only the helper functions in a `module` and call them as such from the task - this means two namespacing structures side by side either within the same file, or in separate files and directories
4. Wrap the helper functionality in a full-fledged class/module and move it the code somewhere else - this is basically just a rephrasing of the previous option

I don't really like any of the options. (3) and (4) bring unnecessary complexities, (2) beats the whole purpose of having a DSL and (1) feels dirty.

Do you have any suggestions how to deal with this?
