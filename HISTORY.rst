History
=======

1.1.0 (2020-06-08)
------------------

* Add ``shift()`` method to move forward in time by a delta whilst travelling.
  This is based on freezegun's ``tick()`` method.

  Thanks to Alex Subbotin for the feature in
  `PR #27 <https://github.com/adamchainz/time-machine/pull/27>`__.

* Fix to work when either ``clock_gettime()`` or ``CLOCK_REALTIME`` is not
  present. This happens on some Unix platforms, for example on macOS with the
  official Python.org installer, which is compiled against macOS 10.9.

  Thanks to Daniel Crowe for the fix in
  `PR #30 <https://github.com/adamchainz/time-machine/pull/30>`__.

1.0.1 (2020-05-29)
------------------

* Fix ``datetime.now()`` behaviour with the ``tz`` argument when not time-travelling.

1.0.0 (2020-05-29)
------------------

* First non-beta release.
* Added support for ``tz_offset`` argument.
* ``tick=True`` will only start time ticking after the first method return that retrieves the current time.
* Added nestability of ``travel()``.
* Support for ``time.time_ns()`` and ``time.clock_gettime_ns()``.

1.0.0b1 (2020-05-04)
--------------------

* First release on PyPI.
