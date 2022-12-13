cmake_minimum_required(VERSION 3.16)

SET(BINARY add_test)
SET(EXECUTABLE_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/build)
add_compile_options(-fprofile-arcs -ftest-coverage -ggdb)
add_link_options(-lgcov --coverage)

include_directories(../src)
file(GLOB_RECURSE TEST_SOURCES LIST_DIRECTORIES false *.h *.c)
set_source_files_properties(${TEST_SOURCES} PROPERTIES LANGUAGE CXX)
SET(SOURCES ${TEST_SOURCES})

add_executable(${BINARY} ${TEST_SOURCES})
target_link_libraries(${BINARY} PUBLIC add gtest pthread)
