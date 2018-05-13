project(expat)
cmake_minimum_required(VERSION 2.8)

file(GLOB_RECURSE src-files src/*.c)
add_library(expat STATIC ${src-files})
target_include_directories(expat PUBLIC include)
target_compile_definitions(expat PUBLIC -DHAVE_MEMMOVE)
target_compile_definitions(expat PUBLIC -DXML_STATIC)