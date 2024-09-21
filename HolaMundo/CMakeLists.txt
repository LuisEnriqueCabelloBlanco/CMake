cmake_minimum_required(VERSION 3.5)

set(CMAKE_CXX_STANDARD 11)

project("HolaMundo" VERSION 1.0)

configure_file(hola.h.in hola.h)

add_subdirectory(my_lib)

add_executable(main "main.cpp")

target_link_libraries(main PUBLIC MathFunctions)

target_include_directories(main PUBLIC "${PROJECT_BINARY_DIR};${PROJECT_SOURCE_DIR}/my_lib")


