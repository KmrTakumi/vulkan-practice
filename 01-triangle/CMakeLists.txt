cmake_minimum_required(VERSION 4.0)
project(01-triangle LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(Vulkan REQUIRED)
find_package(glfw3 REQUIRED)

add_executable(01-triangle 01-triangle.cpp)

target_link_libraries(01-triangle PRIVATE glfw Vulkan::Vulkan)