# helloworld-cpp

[![CircleCI](https://circleci.com/gh/paulaverilla/helloworld-cpp.svg?style=svg)](https://circleci.com/gh/paulaverilla/helloworld-cpp)

This project illustrates the use of different C++ tools and technologies in a simple hello world example.

## Source Control
Git

When excluding files locally, configure the file `.git/info/exclude`.

## Source Repository
Github.

See: https://github.com/paulaverilla/helloworld-cpp

## Build
1. Open a terminal. Install system dependencies.
    ```bash
    apt update
    apt upgrade -y
    apt install build-essential -y
    apt install cmake -y
    ```
    *Optional:* To build with Clang, run:
    ```bash
    apt install clang -y
    ```
2. Build the project.
    
    ```bash
    mkdir build
    cd build
    cmake ${PROJECT_ROOT}
    make -j$(nproc)
    ```
    *Optional:* To build with GNU, configure the environment variables before running CMake:
    ```bash
    export CC=/usr/bin/gcc
    export CXX=/usr/bin/g++
    ```
    *Optional:* To build with Clang, configure the environment variables before running CMake:
    ```bash
    export CC=/usr/bin/clang
    export CXX=/usr/bin/clang++
    ```
3. Run.
    ```bash
    ./build/src/helloworld-cpp
    ```
    The console output should display:
    ```bash
    Hello world!
    ```
## Continuous Integration
The CI used in this project is CircleCI. Currently, it has Ubuntu 18.04 (ubuntu:bionic) as the base docker image for the build environment.

See: https://circleci.com/gh/paulaverilla/helloworld-cpp

Travis CI was initially considered, but its official Ubuntu support that can be used by default is still Ubuntu 14.04. It can be switched to 16.04, but no Ubuntu 18.04 support is available. See: https://docs.travis-ci.com/user/reference/overview/#virtualization-environments