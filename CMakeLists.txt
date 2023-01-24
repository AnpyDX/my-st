# CMake for Suckless st (compile_command.json)
cmake_minimum_required(VERSION 3.2)
project("st")

set(CMAKE_C_STANDARD 99)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

aux_source_directory(. ST_SOURCES)

add_executable("st" ${ST_SOURCES})

target_include_directories(
    "st" PUBLIC
    /usr/include/X11
    /usr/include
    )
