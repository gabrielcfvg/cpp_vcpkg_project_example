cmake_minimum_required(VERSION 3.22.1)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

project(nvcpkg CXX)
add_executable(nvcpkg src/main.cpp)

find_package(fmt REQUIRED)

target_link_libraries(nvcpkg PRIVATE -lstdc++ fmt::fmt)
target_compile_options(nvcpkg PRIVATE -std=c++17 -g)
