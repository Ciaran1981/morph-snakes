
cmake_minimum_required(VERSION 2.8)
project(MorphSnakes)

find_package(Threads)

include_directories(${PROJECT_SOURCE_DIR}/include)
add_definitions(-std=c++11)

add_executable(tests
    tests/tests.cpp
    multisnakes/include/ndimage.h
    multisnakes/include/narrowband.h
    multisnakes/include/morphsnakes.h
)
target_link_libraries(tests ${CMAKE_THREAD_LIBS_INIT})
