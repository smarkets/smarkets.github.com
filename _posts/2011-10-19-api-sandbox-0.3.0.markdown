---
layout: post
title: API Sandbox v0.3.0
author: mokele
published: true
---
We've updated the sandbox and the relevant code on [GitHub][] and [smarkets.github.com][] to the API version 0.3.0. What we've added is are:

 * [orders-for-market-request][] - to fetcha list of open orders per market. We don't think this set of messages is perfect quite 
   yet, but we wanted to give you access to what is currently available so we can move towards the best solution. Iterative design++. 
   We also want to have access to all open orders for an entire account, but seen as that might be of considerable size for many 
   market makers we need to rethink how best to expose such high volumes of orders in the most elegant way possible. We really want 
   the best.

 * more [logout-reasons][] for your debugging pleasure

 * All connections are now over SSL - the cert isn't verified due to just being a sandbox, but we'll be sorting that 
   out don't you worry.

 * Fixes to async [contract-quotes][] payloads when subscribed to a market so they're sure to include a zero quantity for quotes
   where no quantity is left available. This will occur when all of a given quantity at a price is executed or cancelled.

 * Session Cleanup - All sessions left unused for more than 24 hours will be cleaned up and will no longer be resumable. 
   We want to make creating new sessions as light weight as possible, so to achieve this we need to clean up the cruft on an ongoing 
   basis. For 24 hour, 36(5|6) days a year access to the api we recommend maintaining a persistent connection to Smarkets, whether 
   that's through just 1 ongoing session or 5, we don't mind... but if you leave one unused and want to forget about the market 
   subscriptions and live order updates for that session, we'll be cleaning that up, ok? good. For shorter-term connections to 
   Smarkets such as mobile apps you can either make your connection to us on a server of your own and expose that to your mobile 
   app, or simply have your mobile app create a new session and disconnect to save battery life. We'll be writing more about the
   best approaches depending on what you're developing, so stay tuned for that.

Added to this, we'll soon be eating our own dog food by having our own website [Smarkets.com][] place bets on your behalf 
over our WebSockets server connecting directly with our streaming API. We're pretty excited about this part!

<p align="center"><a href="http://blaugh.com/2006/11/15/tastes-like-chicken" rel="bookmark"><img class="comic" title="Tastes Like Chicken" alt="Tastes Like Chicken" src="http://blaugh.com/cartoons/061115_your_own_dogfood.gif" width="447" height="250"/></a></p>

See you on freenode IRC channel #smarkets

[Github]: https://github.com/smarkets/
[smarkets.github.com]: http://smarkets.github.com/
[orders-for-market-request]: /smk_api_docs/#seto/orders-for-market-request
[logout-reasons]: /smk_api_docs/#eto/logout
[Smarkets.com]: https://smarkets.com/
