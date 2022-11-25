cmake_minimum_required(VERSION 3.22)

# sets build dir to bin/lib folder in cwd
# https://stackoverflow.com/questions/6594796/how-do-i-make-cmake-output-into-a-bin-dir
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/lib)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/lib)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/bin)

project(template)

# add deps here

#add_subdirectory(example)

# collect sources here

file(GLOB_RECURSE EXAMPLE_SOURCES src/*.cpp src/*.hpp)

# add executables/libraries

add_executable(example ${EXAMPLE_SOURCES})