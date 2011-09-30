---
layout: post
title: Doing maths in JavaScript
author: rednum
published: true
---

One of the things that we must get right at Smarkets is floating point arithmetic. As it turned out while adding some new feature to our frontend - displaying potential profit and loss as you are adding a new bet - we need some better javascript library to handle floating point numbers properly. The best way to get it was to get an intern - ie. me - to write it!

Hence I present [decnum], the javascript decimal numbers library. It is a standalone project that provides arbitrary-precision numbers with arithmetic and comparison. The library comes with some tests, which you can run using [nodeunit].

Since decnums are implemented as arrays of 'digits' in base 10000, most of the operations can get a bit slow for really big numbers - especially division and multiplication, which run in quadratic time (rest of the operations run in linear time). This shouldn't be a problem unless you are using some really huge numbers in your calculations (or want some crazy precision) - but if you do, you probably shouldn't be writing in javascript in the first place!


[nodeunit]: https://github.com/caolan/nodeunit
[decnum]: https://github.com/smarkets/decnum
