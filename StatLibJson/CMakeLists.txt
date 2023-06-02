cmake_minimum_required(VERSION 3.6)

set(TARGET StatLibJson)

project(${TARGET})

set(CMAKE_CXX_STANDARD 17)

set(ANTLR_INCLUDE ${CMAKE_SOURCE_DIR}/StatLibJson/antlr4)
set(ANTLR_LIB "C:/Users/Main/Desktop/ANTLR/tmp/lib/antlr4-runtime.lib")

file(GLOB TARGET_SRC "*.c*")
file(GLOB TARGET_HD "*.h*")
add_library(${TARGET} STATIC ${TARGET_SRC} ${TARGET_HD})

target_include_directories(${TARGET} PUBLIC ${ANTLR_INCLUDE})
target_link_libraries(${TARGET} ${ANTLR_LIB})