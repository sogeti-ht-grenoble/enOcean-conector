cmake_minimum_required(VERSION 2.8)

#Disable in source compilation
if ( ${CMAKE_SOURCE_DIR} STREQUAL ${CMAKE_BINARY_DIR} )
message( FATAL_ERROR "In-source builds not allowed. Please make a new directory (called a build directory) and run CMake from there. You may need to remove CMakeCache.txt." )
endif()

project(Gateway C CXX)

#Ensure cross compilation not used by default
option(PI "Enable Raspberry Pi compilation" OFF)

enable_testing()

if(PI)
	include(Pi.cmake)
endif()
include(Output.cmake)
include(UT.cmake) 
include(Externals.cmake)
include(CompilerFlags.cmake)

add_subdirectory(src/Gateway)
