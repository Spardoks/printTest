cmake_minimum_required(VERSION 3.4)

include("cmake/HunterGate.cmake")
HunterGate(
    URL "https://github.com/Spardoks/hunter/archive/v0.23.302.tar.gz"
    SHA1 "3ac66557e177c324177946ae70bb25a40947248e"
)

project(demo_print)

hunter_add_package(print)
find_package(print CONFIG REQUIRED)

add_executable(demo demo.cpp)
target_link_libraries(demo print::print)

