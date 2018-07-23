project(libs)

set(libs_src
    ${PROJECT_SOURCE_DIR}/lodepng.cpp)

message(${libs_src})
add_library(libs STATIC ${libs_src})
