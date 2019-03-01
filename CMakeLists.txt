cmake_minimum_required (VERSION 3.10)
project (helloworld-cpp)

message("Using compiler " ${CMAKE_CXX_COMPILER_ID})

add_subdirectory(src)