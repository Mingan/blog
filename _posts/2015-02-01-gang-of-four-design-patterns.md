---
published: false
layout: post
title: "Gang of Four: Desing Patterns"
tags: 
  - books
category: articles
comments: true
image: 
  feature: red_dwarf_gunmen.jpg
---

Last week I finished an older book _[Design Patterns](https://www.goodreads.com/book/show/10110722-n-vrh-program-pomoc-vzor)_ by GoF. It's one of the bibles of SW development and I had never read it so it was time to fix that. Plus [the interview with GoF on Software Engineering Radio #215](www.se-radio.net/2014/11/episode-215-gang-of-four-20-years-later/) was very interesting.

My notes are a little sparse because I borrowed the book from library and already had to return it. Luckily, there's a nice [overview of the book on Wikipedia](http://en.wikipedia.org/wiki/Software_design_pattern). The borrowed book was in Czech and tried really hard to translate everything including the names of all the patterns. It reminded me of my university courses when the lecturers insisted on using the strange Czech names of the patterns with an explanation that it's easier for beginners. It's not, it's just confusing. The translator and publisher had enough insight to at least keep the English terms in subtitles and parenthesis to anchor them.

The book created a prototype for documenting design patterns and is pretty straightforward. It opens with a motivation, continues with a shallow but extensive example of a text editor and then dives into the catalogue of patterns themselves. It consists of three groups: creational, structural and behavioural patterns. The complete list is on the Wikipedia.

I have to admit I mostly didn't read the code samples. They are written in C++ or Smalltalk and even though I would get through the code I settled for the description of the pattern with its implications which were generally the most interesting part of each pattern.

Nice thing about reading the book is that I have some experience and I was able to appreciate the patterns better than during the first semester when everything was way too abstract. I have actively used some of the patterns in my day to day work and sometimes I even knew I was doing that! Generally the patterns aren't anything magical or surprising. They're just a distillation of a lot of effort put forth by programmers over the years trying to solve problems as best as possible. Generally, anyone would come to them facing the same problem and having time to think about it, albeit probably not realizing all the implications. There lies the greatest benefit of the book. Plus having names for things. (Which doesn't prevent flames about a single pattern. Apparently there's Singleton - the good kind but other Singletons are anti-patterns, Dependency Injection is a hot topic etc.)

On the other hand, reading the book I often thought that the patterns (or most of their parts) are just crutches to solve problems of the language. The authors mention the possibility and that some of the patterns are supported at the language level in different languages. Since I've worked mostly with dynamic langauges (PHP, Ruby, JavaScript, CoffeeScript) or expressive languages (Clojure, to a lesser degree Scala) I had the nagging feeling that the patterns are most useful when writing code in static languages like Java which put obstacles in programmer's way. Several reviews on GoodReads (eg. [Carl-Erik Kopseng's](https://www.goodreads.com/review/show/817768045?book_show_action=true)) mention other, newer books on design patterns. I'm especially looking forward to _[Design Patterns in Ruby](https://www.goodreads.com/book/show/2278064.Design_Patterns_in_Ruby?ac=1)_ because I have the feeling that many of the patterns aren't implemented via a set of related classes but rather by an approach, typical use case or convention.

What the aforementioned Wikipedia page about design patterns made me realize is the long list of concurrency patterns which I'll have to read up on. I rarely have to deal with concurrency in my code and have only a very superficial understanding of it supplemented by a label _Dangerous: Enter only if you want your head to explode_. However, I believe the list of patterns and three episodes of SE Radio will be helpful.