cmake_minimum_required(VERSION 2.8 FATAL_ERROR)
project("LAStools")

if (!MSVC)
	add_compile_options(-O3 -Wall -Wno-strict-aliasing)
else()
	add_definitions(-D_CRT_SECURE_NO_WARNINGS)
endif()

add_subdirectory(LASlib/src)
add_subdirectory(LASlib/example)
add_subdirectory(LASzip/example)
add_subdirectory(src)

