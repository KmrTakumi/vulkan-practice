cmake_minimum_required(VERSION 4.0)
project(00-window LANGUAGES CXX)

find_package(glfw3 REQUIRED)

add_executable(00-window 00-window.cpp)

target_link_libraries(00-window PRIVATE glfw)