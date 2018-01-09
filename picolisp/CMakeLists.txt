cmake_minimum_required(VERSION 3.6)
project(picolisp)

set(CMAKE_CONFIGURATION_TYPES "Debug" CACHE STRING "" FORCE)
set(CMAKE_WINDOWS_EXPORT_ALL_SYMBOLS on CACHE BOOL "option1")
set(BUILD_SHARED_LIBS on CACHE BOOL "option2")
set (CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_LIBRARIES "${CMAKE_CXX_STANDARD_LIBRARIES} ")
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/../)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/../)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/../)

set(SOURCE_FILES
apply.cpp
flow.cpp
gc.cpp
io.cpp
main.cpp
math.cpp
pico.h
subr.cpp
sym.cpp
targetver.h
stdafx.cpp
stdafx.h)

include_directories(${CMAKE_SOURCE_DIR})

add_definitions(-DUNICODE -D_UNICODE)
add_executable(picolisp  ${SOURCE_FILES} )
