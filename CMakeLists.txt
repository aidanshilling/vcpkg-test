cmake_minimum_required(VERSION 3.0)

set(CMAKE_TOOLCHAIN_FILE 
  "/home/aidan/vcpkg/scripts/buildsystems/vcpkg.cmake")
set(CMAKE_CXX_STANDARD 20)

project(vcpkg-test)

find_package(GLEW REQUIRED)

add_executable(${PROJECT_NAME} src/main.cpp)

target_link_libraries(${PROJECT_NAME}
  PUBLIC
    GLEW::GLEW
)
