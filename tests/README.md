# Running Unit Tests

This directory should contain the unit tests for shell scripts in the `bin/` and `lib/` directories.

## Dependencies

Unit tests are run using [`shunit2`], an [xUnit] test runner developed for Bourne based shell scripts.

### Using the [`homebrew`] Package Manager

[`homebrew`] is a package manager for MacOS and Linux. The developers of `shunit2` have made the command available for installation using:

```sh
$ brew install shunit2
# Installation logs will be here.
```

### Manual Installation

If you want to install it manually without the aid of a package manager, you'll need to download the release version from the [`shunit2`] project repository and add it to a location accessible through your `PATH` environment variable. This process will differ depending on your system configuration and user privileges.

## Getting Started

Typically your unit test script will define a series of test functions and then source or invoke the `shunit2` test suite:

```sh
#! /bin/sh

testEquality() {
  assertEquals 1 1
}

# Invoke or source shunit2 depending on your installation.
shunit2
```

Please refer to the [function reference] for a full rundown on how to write unit tests that are compatible with this library.

<!-- Links -->

[`shunit2`]: https://github.com/kward/shunit2
[xUnit]: https://en.wikipedia.org/wiki/XUnit
[`homebrew`]: https://brew.sh/
[function reference]: https://github.com/kward/shunit2#function-reference