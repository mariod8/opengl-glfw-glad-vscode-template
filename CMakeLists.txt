cmake_minimum_required(VERSION 3.23)

set(PROJECT_NAME yourproject)

project(${PROJECT_NAME})

add_subdirectory(libs)

add_executable(${PROJECT_NAME} src/main.cpp)
target_link_libraries(${PROJECT_NAME} glad)
target_link_libraries(${PROJECT_NAME} glfw)
find_package(OpenGL REQUIRED)
target_link_libraries(${PROJECT_NAME} OpenGL::GL)