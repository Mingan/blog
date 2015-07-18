---
published: true
layout: post
tags:
  - books
category: articles
comments: true
title: "Caleb Doxsey: An Introduction to Programming in Go"
---

In my effort to better myself at my job, I try to learn new things about programming, SW development and related issues. Programming languages fall into this group. I rarely get deep into any given language, but I try to sample them, understand how and when to use them; I get acquainted with various approaches to programming.

The languages I've tried: Scala, CoffeeScript, LESS, Stylus, Scheme and Clojure. I've come to use some of them on daily basis (CoffeeScript, CSS preprocessors), others I hardly got at all (eg. Scheme), some excited me but I never had the need to use them regularly (Scala and Clojure [which is much easier dialect of Lisp to get into]). My most recent discovery is Go. I've heard the buzz around the language and some nice discussions about it (I believe one of them was on the [Giant Robots Smashing into Other Giant Robots podcast](https://robots.thoughtbot.com/) but I'm unable to find the episode) and it sounded interesting. At first, I thought, I won't have any reason to use it, because we use a different technology set at [Enectiva](http://www.enectiva.cz/en/about-enectiva/). However, in the last few months we've discovered that some parts of the system might benefit from a rewrite into a language closer to the metal.

Therefore I started learning about Go. The simplest and very instructional way to get a taste of Go is the [online tour](https://tour.golang.org/); though, I found some of the problems unnecessarily hard - not because of Go, but because of the given task (although people with CS background would probably disagree). After that (and watching many videos and presentations) I got my hands on Mark Summerfield's [Programming in Go](https://www.goodreads.com/book/show/13705101-programming-in-go). It's a thick book which reads more like a reference book than a teaching material. However, it demonstrates the aspects of the language and the common library on complete examples. If you skim through all the methods on strings and get to the examples, you're fine. Still, I'm not even half way through.

A few weeks ago, I had some spare time and decided to re-implement one of our troublesome components in Go. I've done it previously in Clojure; it took me three days to wrap my head around it but I managed to get in working in the end and was very impressed with the performance. Since Go is much closer to the languages I'm used to thinking in, this time it took mu just a single afternoon to the same job. But because it was the first time I tried writing Go on my own, I had to go back and lookup things (how do I declare a method on a type?, how are the references passed around? how do I instantiate an array/map?). For that purpose Caleb Doxsey's [*Introduction to Programming in Go*](https://www.goodreads.com/book/show/19047668-an-introduction-to-programming-in-go) (also [available for free online](http://www.golang-book.com/)) was an excellent resource. The book is very short - way too short for learning the language on its own - but provides a very brief and practical summary of the language. It answered almost all of my questions, for the rest there's Stack Overflow.

The book has 14 chapters starting from the basics of code organization and goes through types, variables, control structures, functions, pointers and others to include even overview of the core packages. As I've said, I doubt anyone could learn the language from this book, but as a point of reference for a programmer coming from a different language, it's indispensable.

My only critique is the lack of references/further reading recommendations. The final chapter includes few suggestions, but I would greatly appreciate links in each chapter for more in depth resources for further study. However, this doesn't change the fact, that it's a great book when trying out Go.
