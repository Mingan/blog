---
published: false
layout: post
title: "Kent Beck: Extreme Programming"
tags:
  - books
category: articles
comments: true
---

__[Extreme Programming](https://www.goodreads.com/book/show/10110673-extr-mn-programov-n)__ by Kent Beck is hardly a new book. XP and other agile methodologies have been rehashed over and over, interpreted and re-interpreted, mixed and stirred, elaborated and simplified at least as much as Wittgenstein. This book goes to the root of XP and explains all about it or at least quite a lot.

First off the book is really short, structured in sections Problem, Solution and Implementation composed of 36 brief chapters which are nicely summarized in the contents. There is no need to go through all of the chapters and discuss individual points but still I want to mention at least some of them.

Software development is described as a balancing act of four components: cost, time, quality and scope; from which only scope can be effectively manipulated. Lowered quality leads to technical debt, growth of dirty code no one wants to touch and eventually collapse of the SW. This is similar to the [broken window theory](http://en.wikipedia.org/wiki/Broken_windows_theory) which might not be true for crime but is much more easily applicable to code. Time is usually set be the customer, marketing, sales or by running out of money in case of bootstrapping and can't be much shifted. Even if it was, the knowledge that the deadline can be postponed is often counterproductive.

Money is a simple constraint. On one hand every project needs enough money to operate but abundance leads to catastrophe - either more developers are hired with the belief that the project will be done faster or existing developers are paid directly or indirectly (by spending on their environment) more giving them more to lose. Scope can be manipulated but the client must be willing to accept that process. My personal experience from smaller projects says that people really like it and see the benefit of rapid iterative development. Larger projects are more often bound by absurd up front specifications and contracts which preclude them from any adaptation over time.

An important stance XP takes is that changes should be made only when they are necessary. It's basically the [YAGNI principle](http://en.wikipedia.org/wiki/You_aren%27t_gonna_need_it) taken to the extreme. In a way it makes sense, especially on the smaller scale. Where I'm more skeptical is a larger scale and architecture of the whole system which in my view deserves more planning which stakes the road to the future but isn't taken as a dogma. Again it's about balancing of the two approaches. If people spend a lot of time planning long into the future they're reluctant to let go of those plans; blindly going and solving only the very next problem (even though there are inevitable exceptions) isn't a viable strategy either.

The core values of XP are:

1) communication;
2) simplicity;
3) feedback; and
4) courage.

Even though it seems obvious it's a good reminder of the values because people tend to leave them behind under pressure. Luckily Kent comes back to the topic of fear and reversal to old (bad) habits again and again. In the end developers are just people driven by emotions, personal goals and tendency to prefer short-term benefits even against their better judgment. It's crucial to find a way to keep their goals aligned with goals of the project and the company. Personally, I see a risk here that these goals becoming one and the same. Complete developers' devotion commonly expected in the start-up world might be beneficial for the company in a short run but is detrimental to the individuals in the long run.

The second part of the book, Solution, describes the day to day life of XP teams. The most controversial point from this section for me is the complete devotion to the principles and practices of XP. I can easily identify with some of them (testing, incremental changes, responsibility, measuring & benchmarking, 40 hour week, continuous integration), I doubt others (the suggested physical arrangement) and I have some reservations about the rest (the amount of pair programming). Some of my reservations come from my lack of experience and I'm open to experiments but my point is that it looks very easy to not implement the XP as a whole but to cherry pick only parts of it and end up disappointed because it didn't meet the expectations. Beck addresses this issue in several chapters but I remain sceptical about gradual implementation of XP.

An interesting point brought into the forefront in the last section are the limits of applicability of XP. The author lists types of projects which are bound to fail or struggle with XP (integration middleware projects, framework development, large teams, high stakes).

To summarize I really like most of the core ideas behind XP and I'm a part of a team which implements some them. Still I find it hard to imagine to implement XP as a whole especially if moving there gradually. On the other hand it's important to deliver maintainable SW and the process is bound to be at least slightly different every time. Defining what is and what isn't XP is hard and unnecessary exercise if the process works for the developers, the project and the company.