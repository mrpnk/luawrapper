cmake_minimum_required(VERSION 3.22)
project(luawrapper)

set(CMAKE_CXX_STANDARD 23)


# boost
#find_package(Boost REQUIRED)
#include_directories(${Boost_INCLUDE_DIRS})

# lua
include_directories(../lua-5.4.6/src/)

# including lua wrapper
include_directories(include)

add_library(luawrapper luawrapper.cpp)



target_link_libraries(luawrapper ../../lua-5.4.6/cmake-build-release/lua)

