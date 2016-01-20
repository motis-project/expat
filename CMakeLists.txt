project(expat)
cmake_minimum_required(VERSION 2.8)

include_directories(include/expat)
file(GLOB_RECURSE src-files src/*.c)
add_library(expat ${src-files})
set_target_properties(expat PROPERTIES COMPILE_FLAGS -DHAVE_MEMMOVE)
