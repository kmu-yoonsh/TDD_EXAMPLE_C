cmake_minimum_required(VERSION 3.8)


set(This Example)

project(${This} C CXX)

set(CMAKE_C_STARNDARD 99)
set(CMAKE_CXX_STARNDARD 11)
set(CMAKE_POSITION_INDEPENDENT_CODE ON)

enable_testing()

add_subdirectory(googletest)

set(Headers
    Example.h
)

set(Sources
    Example.c
)

add_library(${This} STATIC ${Sources} ${Headers})

add_subdirectory(test)
