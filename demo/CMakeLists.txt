cmake_minimum_required(VERSION 2.8)
project(Test)

link_directories(libs)
include_directories(include)

#message(STATUS "11111${PROJECT_SOURCE_DIR}")

add_subdirectory(utils)
aux_source_directory(. SRCS_DIR)
add_executable(Test ${SRCS_DIR})
target_link_libraries(Test utils)
