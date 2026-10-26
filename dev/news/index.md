# Changelog

## progress (development version)

## progress 1.2.3

CRAN release: 2023-12-06

- Compiling packages linking to progress with `-Wformat-security` does
  not produce warnings now.

## progress 1.2.2

CRAN release: 2019-05-16

- Fix two bugs in the C++ API that can potentially cause irregular
  behavior ([\#94](https://github.com/r-lib/progress/issues/94), 1).

## progress 1.2.1

CRAN release: 2019-05-13

- Add the `message_class` argument, to add extra classes to the messages
  thrown by progress.

- Add support for RKWard, running interactive session
  ([\#76](https://github.com/r-lib/progress/issues/76),
  [@devillemereuil](https://github.com/devillemereuil)).

- Add support for unicode characters and a right to left progress bar
  ([\#86](https://github.com/r-lib/progress/issues/86), 1).

- Fix a potential crash in the C++ API
  ([\#91](https://github.com/r-lib/progress/issues/91), 1).

## progress 1.2.0

CRAN release: 2018-06-14

- Option to change the ‘current’ character in the progress bar.
  [\#47](https://github.com/r-lib/progress/issues/47)

- New `:tick_rate` token, similar to `:rate`, but units are not assumed
  to be bytes. [\#45](https://github.com/r-lib/progress/issues/45)

- Total number of ticks can be set to `NA` now, if unknown.
  [\#48](https://github.com/r-lib/progress/issues/48)

- All progress bars (including the ones from the C++ API) can be turned
  off via the `progress_enabled` option
  [\#44](https://github.com/r-lib/progress/issues/44)

- The `stream` argument is deprecated and the progress bar is always
  printed with [`message()`](https://rdrr.io/r/base/message.html) calls.

- Total number of iterations can be zero, to support special cases
  better.

- Add `finished` variable, which can be queried to see if a progress bar
  is finished. [\#54](https://github.com/r-lib/progress/issues/54) 1.

- Add a `terminate()` method, which can be called to explicitly remove
  the progress bar, [\#53](https://github.com/r-lib/progress/issues/53)
  1.

- Outputs greater than the bar width are automatically trimmed, 1.

- Add a [`message()`](https://rdrr.io/r/base/message.html) method to
  print a message line(s) above the progress bar,

  1.  

- :elapsedfull token: elapsed time in hh:mm:ss format.

- Fix C++ compiler warnings.
  [\#43](https://github.com/r-lib/progress/issues/43)

- Fix C++ API on Windows.
  [\#56](https://github.com/r-lib/progress/issues/56)

- Pass `self` to the callback function.
  [\#55](https://github.com/r-lib/progress/issues/55) 1

## progress 1.1.2

CRAN release: 2016-12-14

- Do not run tests on CRAN, Solaris does not have microbenchmark

## progress 1.1.1

CRAN release: 2016-12-13

- Move README.md, so that it is not parsed on CRAN
- Use https URLs instead of http, whenever possible

## progress 1.1.0

- Support for the `:spin` token which adds a simple ASCII spinner,
  [@richfitz](https://github.com/richfitz)
- Respect custom token width for calculation of the bar width,
  [@mllg](https://github.com/mllg)

## progress 1.0.2

CRAN release: 2015-06-05

- Fix the C++ API on Windows, and on older compilers in general.

## progress 1.0.1

CRAN release: 2015-05-30

First version on CRAN.
