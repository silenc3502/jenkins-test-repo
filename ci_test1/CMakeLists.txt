cmake_minimum_required(VERSION 3.16)
project(ci_test1)

set(CMAKE_C_STANDARD 99)
#SET(CMAKE_CXX_STANDARD 11)
set(CMAKE_C++_COMPILER g++)
set(CMAKE_BUILD_TYPE Debug)

add_subdirectory(src)
add_subdirectory(test)
