cmake_minimum_required(VERSION 3.6)

set(TARGET DLLJson)

project(${TARGET})

file(GLOB TARGET_SRC "*.c*")
file(GLOB TARGET_HD "*.h*")
add_library(${TARGET} SHARED ${TARGET_SRC} ${TARGET_HD})

set_target_properties(${TARGET} PROPERTIES COMMON_LANGUAGE_RUNTIME "")

set(Stat_INCLUDE ${CMAKE_SOURCE_DIR}/StatLibJson)
target_include_directories(${TARGET} PUBLIC ${Stat_INCLUDE})

add_dependencies(${TARGET} StatLibJson)
set(ANTLR_LIB "C:/Users/Main/Desktop/ANTLR/tmp/lib/antlr4-runtime.lib")
set(Stat_LIB ${CMAKE_SOURCE_DIR}/x64/Debug/StatLibJson.lib)
target_link_libraries(${TARGET} ${ANTLR_LIB} ${Stat_LIB})