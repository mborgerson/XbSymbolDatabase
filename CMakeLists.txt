# CMakeList.txt : CMake project for XbSymbolSymbolDatabase, include source and define
# project specific logic here.
#
cmake_minimum_required (VERSION 3.12)

project (XbSymbolDatabase)

add_compile_definitions(_CRT_SECURE_NO_WARNINGS)

file(GLOB_RECURSE SOURCES
 "XbSymbolDatabase.c"
 "OOVPADatabase/*.inl"
)

source_group(TREE ${CMAKE_CURRENT_LIST_DIR} FILES ${SOURCES})

add_library (XbSymbolDatabase ${SOURCES})

set_target_properties(XbSymbolDatabase PROPERTIES
 C_STANDARD 11
 C_STANDARD_REQUIRED ON
)
