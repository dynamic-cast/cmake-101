cmake_minimum_required(VERSION 3.10)
project(loadpng)

# set the version of the software
set (LOADPNG_VERSION_MAJOR 0)
set (LOADPNG_VERSION_MINOR 1)

# which type of build (could be a Release)
set(CMAKE_BUILD_TYPE Debug)

# set where you want to install your program
set(CMAKE_INSTALL_PREFIX install)

# *magic* We don't need this :)
#set(CMAKE_CXX_FLAGS "-std=c++11")


# set where you want the binaries to be
set(CMAKE_BINARY_DIR ${CMAKE_INSTALL_PREFIX}/bin)
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR})
set(LIBRARY_OUTPUT_PATH ${CMAKE_BINARY_DIR})

add_subdirectory(libs)

set(loadpng_src
    ${PROJECT_SOURCE_DIR}/example_encode.cpp)

add_executable(loadpng ${loadpng_src})


target_link_libraries(loadpng libs)

