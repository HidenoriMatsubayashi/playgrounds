cmake_minimum_required(VERSION 3.10)
project(runner LANGUAGES C)

set(TARGET "hello_world")

find_package(PkgConfig)
pkg_check_modules(GTK REQUIRED IMPORTED_TARGET gtk+-3.0)

add_executable(${TARGET} "main.c")
target_link_libraries(${TARGET} PRIVATE PkgConfig::GTK)
