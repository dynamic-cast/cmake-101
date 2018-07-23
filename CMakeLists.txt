cmake_minimum_required(VERSION 3.10)

# set project name
project(loadpng)

# set the version of the software
set (LOADPNG_VERSION_MAJOR 0)
set (LOADPNG_VERSION_MINOR 1)

# which type of build (could be a Release)
set(CMAKE_BUILD_TYPE Debug)

# set where you want to install your program
set(CMAKE_INSTALL_PREFIX ../install)

# *magic* We don't need this :)
#set(CMAKE_CXX_FLAGS "-std=c++11")

# set var CMAKE_BINARY_DIR
set(CMAKE_BINARY_DIR ${CMAKE_INSTALL_PREFIX}/bin)

# set executable location
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR})

# set library path
set(LIBRARY_OUTPUT_PATH ${CMAKE_BINARY_DIR})

# PROJECT_SOURCE_DIR is the top level source directory for the current project.

# OPTION 1
# set var loadpng_src
set(loadpng_src
    ${PROJECT_SOURCE_DIR}/libs/lodepng.cpp
    ${PROJECT_SOURCE_DIR}/example_encode.cpp)

# OPTION 2 - have lodepng in another directory
# add libs folder
# add_subdirectory(libs)
# # set var loadpng_src
# set(loadpng_src
#     ${PROJECT_SOURCE_DIR}/example_encode.cpp)

# Adds an executable target called loadpng to be built from the source files loadpng_src
add_executable(loadpng ${loadpng_src})

# OPTION 2
# link lodepng lib
# target_link_libraries(loadpng libs)

