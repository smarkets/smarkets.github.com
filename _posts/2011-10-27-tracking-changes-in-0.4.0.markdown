---
layout: post
title: Tracking Changes in v0.4.0
author: mokele
published: true
---
How can I track when the API gets updated? On [GitHub][] of course. With the awesome 
[compare view][] we can diff [0.3.0 with 0.4.0][] without batting an eyelid. 
Subscribing to these articles and hanging out on IRC are also a good idea.

You can also track the [public Smarkets API docs][] project and keep up to date 
when new specs are released and any and all explanation changes.

Along with this API spec update the [erlang][] application and [python][] library 
have been updated with some extra payload sending functions for the new types. 
Added to that, [skarab][] (Hunter) has started work on a C# library named 
[IronSmarkets][] which is now in heavy development. He'll be talking about that 
in more details soon right here. So stay tuned for that.

The sandbox is for customers in a position to be placing bets at this time,
but we'll be providing more tools on top of the API for mass quote fetching 
in the coming months. See you on the other side!

/me goes back to organising [live #erlang release upgrades][]

[live #erlang release upgrades]: http://www.youtube.com/watch?v=O_HyZ5aW76c#t=1m4s
[IronSmarkets]: https://github.com/smarkets/IronSmarkets
[skarab]: https://github.com/skarab
[public Smarkets API Docs]: https://github.com/smarkets/smk_api_docs/commits/master
[GitHub]: https://github.com/smarkets
[compare view]: https://github.com/blog/612-introducing-github-compare-view
[0.3.0 with 0.4.0]: https://github.com/smarkets/smk_api_common/compare/v0.3.0...v0.4.0
