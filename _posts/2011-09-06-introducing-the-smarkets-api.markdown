---
layout: post
title: Introducing the Smarkets API
author: mokele
published: true
---
So, it's time to talk about the Smarkets API, get even more feedback, and get you people using it! We're still in private alpha, so the sandbox is only open to a few (hopefully you) people. Apologies if you don't have access quite yet, it's a busy time and we need to make sure everything is running smoothly before jumping too far ahead of ourselves.

Now let's get down to business.

The Smarkets API was designed with two main objectives in mind - keeping developers happy, and letting them trade in the most sensible way possible. Hopefully it evolves to be far more than these things, but so far this has led us to the following design decisions:

 * Hosting as much as we can on [GitHub][] _(this one's an obvious first step in the right direction)_
 * Having a wire protocol compatible with [Protocol Buffers][] allowing access to the Smarkets messaging protocol in [a large number of different languages](http://code.google.com/p/protobuf/wiki/ThirdPartyAddOns) _(this is a no-brainer for ease-of-use)_
 * __push__ messages _(it's a trading platform - there's real money at stake)_
   * real-time market price updates
   * order executions
   * _and a lot more planned_
 * Exposing [ids](/smk_api_docs/#seto/entity-relationship) for horses, jockeys, and football teams _(a requirement from speaking with client developers)_
 * Beginning with officially supported [Python][] and [Erlang][] SDKs. _(These are the languages we use internally; it's what we know best)_
 * Evolving the API on an ongoing basis based on feedback from the community. All feedback is welcome, and greatly encouraged. Join us in the __#smarkets__ IRC channel on Freenode

We're planning some developer meet-ups and tutorial sessions, so [subscribe][] and we'll keep you updated and help you in every way possible to take advantage of the Smarkets API for trading sports, current affairs, politics, entertainment, and much more.

If you have any questions in the form "Are you planning to X?", the answer is most probably yes.

[GitHub]: https://github.com/smarkets
[Protocol Buffers]: http://code.google.com/p/protobuf/
[Python]: https://github.com/smarkets/smk_python_sdk
[Erlang]: https://github.com/smarkets/smk_erlang_sdk
[subscribe]: http://feeds.feedburner.com/SmarketsApi
