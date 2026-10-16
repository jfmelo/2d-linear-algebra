cmake_minimum_required(VERSION 4.4)
project(LinearAlgebra)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

include (FetchContent)

FetchContent_Declare(
	raylib
	GIT_REPOSITORY "https://github.com/raysan5/raylib.git"
	GIT_TAG "master"
)

FetchContent_MakeAvailable(raylib)

add_executable(${PROJECT_NAME})
target_sources(${PROJECT_NAME} PRIVATE "src/main.c")
target_link_libraries(${PROJECT_NAME} PRIVATE raylib)
