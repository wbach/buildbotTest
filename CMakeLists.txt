project(GameEngineCM)
cmake_minimum_required(VERSION 3.0)


SET(GCC_COVERAGE_LINK_FLAGS    "-static-libgcc")
SET( CMAKE_CXX_FLAGS  "-std=c++14 -Wuninitialized -Wtype-limits -Wdelete-incomplete -Wall -pedantic ${CMAKE_CXX_FLAGS} ${GCC_COVERAGE_COMPILE_FLAGS} -Wno-expansion-to-defined" )
SET( CMAKE_EXE_LINKER_FLAGS  "${CMAKE_EXE_LINKER_FLAGS} ${GCC_COVERAGE_LINK_FLAGS}" )

add_compile_options(
    -std=c++14
)

add_executable(Test main.cpp)




