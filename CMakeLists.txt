cmake_minimum_required(VERSION 2.6)

project(afk)

SET(EXTRA_CXX_COMPILE_FLAGS "-std=c++11 -I./src -I./test -O2 -Werror -Wall -pedantic")

SET(CMAKE_CXX_FLAGS  "${CMAKE_CXX_FLAGS} ${EXTRA_CXX_COMPILE_FLAGS}")

INCLUDE_DIRECTORIES(./include/)

SET(AFK_HEADERS include/afk/algorithm.h)

SET(TEST_FILES test/algorithm_tests.cpp)

add_executable(all-tests ${TEST_FILES} ${MANUFACTURE_TEST_FILES})

install(FILES ${AFK_HEADERS} DESTINATION include/afk)
