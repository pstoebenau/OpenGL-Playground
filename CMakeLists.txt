cmake_minimum_required(VERSION 3.0)

project(openglplayground)

# Find GLEW package
find_package(GLEW REQUIRED)
include_directories(${GLEW_INCLUDE_DIRS})

# Find GLFW package
find_package(glfw3 REQUIRED)
include_directories(${GLFW_INCLUDE_DIRS})

# Set source files
set(SOURCES src/main.cpp)

# Add executable target
add_executable(openglplayground ${SOURCES})

# Link GLEW and GLFW libraries
target_link_libraries(openglplayground GLEW::GLEW glfw)