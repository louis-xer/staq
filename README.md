# SynthewareQ
## Version 1.0

**Build status:**
[![Build Status](https://travis-ci.com/meamy/synthewareQ.svg?token=csCkgudbmX5jejx5vM8V&branch=master)](https://travis-ci.com/meamy/synthewareQ)

---
## About

SynthewareQ is a modern C++17 library for the synthesis, transformation,
optimization and compilation of quantum circuits. It is usable either 
through the provided binary tools, or as a header-only library that can 
be included to provide direct support for parsing & manipulating circuits
written in the [openQASM](https://github.com/Qiskit/openqasm) circuit
description language.

Inspired by Clang, SynthewareQ is designed to manipulate openQASM syntax trees
directly, rather than through an intermediate representation which makes 
retrieving the original source code impossible. In particular, openQASM
circuits can be inspected and transformed (in most cases) without losing the
original source structure. This makes synthewareQ ideally suited for
source-to-source tranformations, where only specific changes are desired.
Likewise, this allows translations to other common circuit description languages
and libraries to closely follow the openQASM source.

Check out the [wiki](https://github.com/meamy/synthewareq/wiki) for
more information about the library and included tools.

---
## Installation

### Linux & Mac OS
SynthewareQ uses CMake for its build system. To build the main synthewareQ
executable, from the root directory execute

  ```bash
  mkdir build && cd build
  cmake ..
  make synthewareQ
  ```

To build the synthewareQ tool suite, from the `build` directory, enter 
`make tools`. Unit tests can be built with the command `make unit_tests`.

### Windows
Building on windows requires [Visual Studio](https://www.visualstudio.com) 2017 
or later for cmake support. In Visual Studio, open
[CMakeLists.txt](https://github.com/meamy/synthewareq/blob/master/CMakeLists.txt)
as a cmake project, then simply build as a regular Visual Studio project.

---
## License
SynthewareQ is distributed under the MIT license. Please see the
[`LICENSE`](https://github.com/meamy/synthewareq/blob/master/LICENSE) file for
more details.

---
## Acknowledgements
Thanks to the excellent [EPFL logic synthesis
libraries](https://github.com/lsils/lstools-showcase) which are used to perform
logic synthesis in synthewareQ, and in particular Bruno Schmitt's
[tweedledum](https://github.com/boschmitt/tweedledum) library, from which the
openQASM parser was adapted.
