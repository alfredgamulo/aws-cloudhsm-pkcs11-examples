cmake_minimum_required(VERSION 2.8)
project(hsm_info)

find_library(cloudhsmpkcs11 STATIC)

include_directories("../common")

add_executable(hsm_info hsm_info.c hsm_info.h)
target_link_libraries(hsm_info cloudhsmpkcs11)
