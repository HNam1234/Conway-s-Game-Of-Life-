cmake_minimum_required(VERSION 3.5)
project(Conway's-Game
        VERSION 0.0.1
        DESCRIPTION "SIMPLE GAME"
        LANGUAGES CXX)
add_executable(GameBinary main.cc
               src/ansi_escapes.cc
               src/cell.cc
               src/grid.cc
               include/ansi_escapes.h
               include/cell.h
               include/grid.h
               include/life.h)
target_compile_features(GameBinary PRIVATE cxx_std_17)

include_directories(${CMAKE_SOURCE_DIR}/include)