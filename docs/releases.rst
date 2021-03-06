txio releases
=============

2.8.1
-----

- July 21, 2017
- fix: the asyncio version of sleep() correctly returns a Future instance


2.8.0
-----

- June 8, 2017
- fix: asyncio - remove the hacks for "simulating" chained futures (no longer works - cpy36 has native code for future)
- new: run CI on Python 3.5 and 3.6


2.7.1
-----

- May 1, 2017
- asyncio: example and docs for running multiple loops
- asyncio: log exception tracebacks when they're available for error-message


2.7.0
-----

- April 15, 2017
- allow alternate asyncio loops
- new future creation API for alternate loops


2.6.1
-----

- February 9, 2017
- added inline sleep helper (Twisted only for now)


2.6.0
-----

- December 29, 2016
- avoid giving negative times to `callLater` with batched timers (issue #81)


2.5.2
-----

- November 6, 2016
- fix pytest3/2
- fix Sphinx 1.4+ doc building
- Copyrights transferred from Tavendo to Crossbar.io Technologies


2.5.1
-----

- April 28, 2016
- Bug with ``make_batched_timer`` remembering (via a closure) the
  reactor/event-loop too persistantly


2.5.0
-----

- April 28, 2016
- Document that ``@coroutine`` and ``@inlineCallbacks`` are not supported
- Objects returned from the :func:`txaio.make_batched_timer` API now
  have millisecond resolution and spread out their notifications over
  the entire range of the bucket.


2.4.0
-----

- April 22, 2016
- Added :func:`txaio.make_batched_timer` API. The main use-case for
  this is when you have lots of of timers, but their exact resolution
  isn't important; batching them into buckets causes far fewer
  delayed call instances to be outstanding in the underlying
  event-loop/reactor.


2.3.1
-----

- April 10, 2016
- added universal wheels


2.3.0
-----

- April 9, 2016
- More logging infrastructure and APIs to support moving all of
  Crossbar.io's logging to txaio.


previous releases
-----------------

- We didn't produce any release notes prior to 2.4.0
- Instead of making up summaries of all previous releases after the
  fact, you will have to do something like ``git log v1.1.0..v2.0.0``
  to see what changed between releases. If you **do** make a summary,
  pull-requests are welcome!
