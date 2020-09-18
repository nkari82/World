cmake_minimum_required(VERSION 2.8)

set(PROJECT_NAME "world")

project(${PROJECT_NAME})

FILE(GLOB SRCS "src/*.cpp" "src/*.c")

FILE(GLOB HEADERS "src/world/*.h" "src/world/*.hpp")

add_library(${PROJECT_NAME} STATIC ${SRCS} ${HEADERS})

target_include_directories(${PROJECT_NAME} PUBLIC "src")

install(TARGETS ${PROJECT_NAME})
