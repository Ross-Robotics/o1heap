cmake_minimum_required(VERSION 3.22)

project(o1heap)

add_library(o1heap STATIC
    "o1heap/o1heap.c"
)

target_include_directories(o1heap
    PUBLIC
        $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/o1heap>
        $<INSTALL_INTERFACE:include>
)
