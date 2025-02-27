cmake_minimum_required(VERSION 3.10.0)
project(my_opengl_project VERSION 0.1.0)
cmake_policy(SET CMP0072 NEW)

find_package(OpenGL REQUIRED)

add_executable(my_opengl_project 
    src/es01.cpp
    src/glad.c
    )

target_include_directories(my_opengl_project
    PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}/dependencies
    )

target_link_libraries(my_opengl_project 
    glfw
    OpenGL::GL
    )