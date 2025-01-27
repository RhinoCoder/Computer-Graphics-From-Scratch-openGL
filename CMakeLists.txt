cmake_minimum_required(VERSION 3.10)
project(OpenGL_Project)

# Set C++ standard
set(CMAKE_CXX_STANDARD 11)

# Include directories
include_directories(
    /usr/include
    ${CMAKE_SOURCE_DIR}
)

# Add source files
add_executable(OpenGL_Project main.cpp)

# Link libraries
find_package(OpenGL REQUIRED)
find_package(GLEW REQUIRED)
find_package(GLFW REQUIRED)
find_package(GLM REQUIRED)
find_package(ASSIMP REQUIRED)
find_package(glfw3 REQUIRED)

target_link_libraries(OpenGL_Project
    ${OPENGL_gl_LIBRARY}
    GLEW::GLEW
    glfw
    glm
    assimp
)