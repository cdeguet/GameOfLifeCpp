cmake_minimum_required(VERSION 3.6)
project(GameOfLife)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

add_subdirectory(contrib/googletest)

include_directories(${gtest_SOURCE_DIR}/include ${gmock_SOURCE_DIR}/include)

set(SOURCE_FILES src/test.cpp)

add_executable(GameOfLife ${SOURCE_FILES})
target_link_libraries(GameOfLife gtest gtest_main)
