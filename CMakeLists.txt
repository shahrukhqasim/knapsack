cmake_minimum_required(VERSION 2.8)
project(knapsack)

set(Boost_USE_STATIC_LIBS OFF)
set(Boost_USE_MULTITHREADED ON)
set(Boost_USE_STATIC_RUNTIME OFF)
FIND_PACKAGE(Boost 1.40 COMPONENTS regex program_options REQUIRED )

include_directories(.)

set(CMAKE_CXX_STANDARD 11)

add_library(knapsack SHARED
        knapsack/knapsack.cc
        knapsack/knapsack.h)

target_link_libraries(knapsack ${Boost_LIBRARIES})
