---
layout: post
title: Doing maths in JavaScript
author: rednum
published: true
---

One of the things that we must get right at Smarkets is floating point arithmetic. While adding some new features to our frontend, it turned out we needed a better JavaScript library to handle floating point numbers for correctly displaying profit and loss. The best way to get one was to get an intern—i.e. me—to write it!

Hence I present [decnum], the JavaScript decimal numbers library. It is a standalone project that provides arbitrary-precision numbers with arithmetic and comparison. The library comes with some tests, which you can run using [nodeunit].

Since _decnums_ are implemented as arrays of "digits" in base 10000, most of the operations can get a bit slow for really big numbers—especially division and multiplication, which run in quadratic time (the rest of the operations run in linear time). This shouldn't be a problem unless you are using some really huge numbers in your calculations (or want some crazy precision), but if you do, you probably shouldn't be writing in JavaScript in the first place!


[nodeunit]: https://github.com/caolan/nodeunit
[decnum]: https://github.com/smarkets/decnum
