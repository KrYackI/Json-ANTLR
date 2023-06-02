cmake_minimum_required(VERSION 3.6)

set(TARGET Json.exe)

project(${TARGET})

set(CMAKE_CXX_STANDARD 17)

set(Json_DIR "D:/git_reps/Json")

set(Json_INCLUDE "/StatLibJson")

add_executable(${TARGET} main.cpp)

target_include_directories(${TARGET} PUBLIC ${Json_DIR}${Json_INCLUDE})

add_dependencies(${TARGET} StatLibJson)
set(ANTLR_LIB "C:/Users/Main/Desktop/ANTLR/tmp/lib/antlr4-runtime.lib")
set(Json_LIB ${CMAKE_BINARY_DIR}/StatLibJson/Debug/StatLibJson.lib)
target_link_libraries(${TARGET} ${ANTLR_LIB} ${Json_LIB})