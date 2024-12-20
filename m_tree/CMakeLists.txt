cmake_minimum_required(VERSION 2.27)

project(m_tree)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/binaries)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/binaries)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/binaries)

find_package(Python3 3.11 EXACT REQUIRED COMPONENTS Interpreter Development.Module OPTIONAL_COMPONENTS Development.Embed GLOBAL)
find_package(Eigen3 CONFIG REQUIRED)

add_subdirectory(./source)
add_subdirectory(./python_bindings)
add_subdirectory(./tests)
