cmake_minimum_required(VERSION 3.22.1)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

project(nvcpkg CXX)
add_executable(nvcpkg src/main.cpp)

find_package(fmt REQUIRED)
target_link_libraries(nvcpkg PRIVATE fmt::fmt)
