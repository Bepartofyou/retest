cmake_minimum_required(VERSION 2.8)
project(retest)

include_directories(${CMAKE_SOURCE_DIR}/../re/include)
include_directories(${CMAKE_SOURCE_DIR}/../rem/include)
link_directories(${CMAKE_SOURCE_DIR}/../re/Win32/Debug/bin)
link_directories(${CMAKE_SOURCE_DIR}/../rem/Win32/Debug/bin)

set(SRC_LIST
    src/main.c
    src/test.h
    src/test.c
    src/list.c
)
message(STATUS "src_list  " ${SRC_LIST})

add_executable(retest ${SRC_LIST})
target_link_libraries(retest re-win32 rem-win32)