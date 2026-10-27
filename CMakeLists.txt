cmake_minimum_required(VERSION 4.3.1 FATAL_ERROR)

set(CMAKE_CXX_STANDARD 20 REQUIRED)

set(PROJECT_NAME zerox_engine_glad)
set(INCLUDE_DIR include)
set(SRC_DIR src)

Project(${PROJECT_NAME})

list(APPEND SOURCES ${SRC_DIR}/gl.c ${SRC_DIR}/wgl.c)

add_library(${PROJECT_NAME} STATIC ${SOURCES})

target_include_directories(${PROJECT_NAME} PRIVATE ${INCLUDE_DIR})
