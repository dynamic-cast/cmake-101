project(libs)

set(libs_src
    ${PROJECT_SOURCE_DIR}/lodepng.cpp)

add_library(libs STATIC ${libs_src})
