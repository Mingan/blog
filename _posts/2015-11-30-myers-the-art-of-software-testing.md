---
published: true
title: "Glenford J. Myers: The Art of Software Testing"
layout: post
tags:
  - books
category: articles
comments: true
---

I'm not completely sure how I stumbled onto this book, but since testing takes up a huge chunk of my work day I decided to read more about it. [*The Art of Software Testing*](https://www.goodreads.com/book/show/11482964-the-art-of-software-testing) is apparently a piece of classic and a milestone in literature about testing. I read the third edition which has some additional chapters, e.g. about mobile application testing, which weren't present in the previous editions.

It is apparent that the book has some history (the first edition is from the late 70s) but are some timeless ideas. Those are mostly in the first part of the book explaining the philosophy behind testing and they include:

 - successful tests fail, thus finding bugs;
 - everything cannot be tested, testing is always a balancing act;
 - you're less likely to successfully test your own code;
 - errors tend to cluster, or
 - testing is hard.

 These are well known concepts but it doesn't hurt to get reminded of them and consider them once in a while.

 The following part of the book goes into more details and practical examples. First formal methods for analyzing programs and designing test cases are introduced, then different types of tests. A whole chapter is dedicated to unit testing while all higher-order (integration, acceptance, security, installation etc.) tests are jammed into a single chapter. The next one discusses benefits of usability testing and the last one debugging.

 There are many ideas in these chapters which are not today's common practice and often go against it. For example, a subsection is devoted to a process how to create the minimum number of inputs (and tests) for a unit so that all possible corner cases are covered. The common wisdom repeated over and over again is *test only one thing at a time*. It makes more sense and makes it easier to track problems (and more importantly grow the test suite when the requirements change). I wonder whether the desire to minimize the number of tests stems from limited resources of the time. Similarly debugging by testing is framed as not the best option - Myers prefers pure reasoning, either by deduction or by induction - contrary to most advice one can hear today: a bug occurred, simulate the problematic circumstances, write a failing test (or tests) and fix the bug.

 Lastly there are three chapters inserted only into this edition. They clearly don't fit in with the rest of the book and have very little value. The first one claims to focus on testing in Agile environment but ends up explaining Agile methodologies, [extreme programming](/articles/kent-beck-extreme-programming/) and TDD. The middle chapter is about testing Internet applications and comes down to: it's hard because there are many moving parts, most of which the programmer cannot control. This sentiment carries over to the last chapter on mobile applications.

 It might seem I didn't like the book, but that's not the case. I really liked the first three chapters because they can be applied any time. The following chapters were a bit dated and often contrary to my standpoint (and the general web development sentiment). It is possible, that Myers is right and everyone else has it all wrong, but I seriously doubt that. The last three chapters are just added fluff about things which are explained better elsewhere and I'd recommend to skim them at most.
