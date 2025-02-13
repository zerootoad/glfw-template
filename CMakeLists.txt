cmake_minimum_required(VERSION 3.10)
project(LearningGLFW)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

find_package(glfw3 REQUIRED)

include_directories(${CMAKE_SOURCE_DIR}/include)
include_directories(/usr/include) 

set(GLAD_SRC ${CMAKE_SOURCE_DIR}/src/glad.c)

add_executable(LearningGLFW src/main.cc ${GLAD_SRC})

target_link_libraries(LearningGLFW glfw)
target_link_libraries(LearningGLFW GL)
