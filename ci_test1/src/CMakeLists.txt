cmake_minimum_required(VERSION 3.16)

add_compile_options(-fprofile-arcs -ftest-coverage -ggdb)
add_link_options(-lgcov --coverage)

#SET (SRC_FILES add.c)
add_library(add OBJECT add.c)
