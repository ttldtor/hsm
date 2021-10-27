cmake_minimum_required(VERSION 3.16)
project(hsm-bin)

set(CMAKE_CXX_STANDARD 20)

include(${CMAKE_BINARY_DIR}/conan_paths.cmake)

find_package(Boost)
find_package(fmt)
find_package(hsm)
add_executable(hsm-bin src/main.cpp)

target_link_libraries(hsm-bin PRIVATE Boost::boost fmt::fmt-header-only hsm::hsm)