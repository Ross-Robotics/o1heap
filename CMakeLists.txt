cmake_minimum_required(VERSION 3.22)

project(o1heap)

add_library(o1heap STATIC
    "o1heap/o1heap.c"
)

set_target_properties(o1heap PROPERTIES POSITION_INDEPENDENT_CODE ON)

target_include_directories(o1heap
    PUBLIC
        $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/o1heap>
        $<INSTALL_INTERFACE:include/o1heap>
)
