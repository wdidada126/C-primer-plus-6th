cmake_minimum_required(VERSION 3.10)
project(primer_plus_exercise)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(SOURCE_DIR "src")

file(GLOB SOURCE_FILES "${SOURCE_DIR}/*.cpp")

# 为每个文件单独创建可执行文件
add_executable(chapter_2 src/chapter_2.cpp)
add_executable(chapter_3 src/chapter_3.cpp)
add_executable(chapter_4 src/chapter_4.cpp)
add_executable(chapter_5 src/chapter_5.cpp)

if(WIN32)
    target_link_libraries(chapter_2 PRIVATE -static)
    target_link_libraries(chapter_3 PRIVATE -static)
    target_link_libraries(chapter_4 PRIVATE -static)
    target_link_libraries(chapter_5 PRIVATE -static)
endif()


