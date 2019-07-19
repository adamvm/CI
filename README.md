[![Build Status](https://travis-ci.org/selyunin/gtest_submodule.svg?branch=master)](https://travis-ci.org/selyunin/gtest_submodule)

# Cmake + googletest (git submodule) + travis CI

A project showing the following features:
* [`cmake`](https://cmake.org/)-based build for C++ project source files;
* [`googletest`](https://github.com/google/googletest) 
  as a [`git submodule`](https://git-scm.com/book/en/v2/Git-Tools-Submodules);
* [`travis-ci`](https://travis-ci.org/) pipeline for running tests. 

C++ project that uses google test as a git submodule
and integrates a travis CI pipeline.

## Directory structure
* [`CMakeLists.txt`](./CMakeLists.txt) cmake project files
* [`include/`](./include) header files (`*.h`)
* [`src/`](./src) source files (`*.cpp`)
* [`test/`](./test) test files  (`*.cpp`)

## Cloning the project
Use `git clone --recursive ...` to download the project and its git submodules.
Otherwise from the project root repository one needs to download the submodules: 
`git submodule update --init`.

## Building the project
1. Creating the executables follows standard `cmake` procedure:
```
    mkdir build
    cd build && cmake ..
```

2. Compile the code (it will also compile the gtest for the first time):
```
    make
```

3. Run executable:
```
    ./project1
```

4. Cmake supports `add_test` function, then the tests can be launch 
`make test` or `ctest` commands.
```
    ./runUnitTests
```
