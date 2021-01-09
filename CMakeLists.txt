cmake_minimum_required(VERSION 3.13 FATAL_ERROR)

set(PROGECT_NAME battle-city)

project(${PROGECT_NAME})

add_executable(${PROGECT_NAME} src/main.cpp)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)
set(GLFW_INSTALL OFF CACHE BOOL "" FORCE)

add_subdirectory (external/glfw)
target_link_libraries (${PROGECT_NAME} glfw)