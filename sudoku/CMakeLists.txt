cmake_minimum_required(VERSION 3.20)
project(sudoku)

set(CMAKE_CXX_STANDARD 17)

find_package(SDL2 REQUIRED)
include_directories(${SDL2_INCLUDE_DIRS})

find_package(SDL2_ttf REQUIRED)
include_directories(${SDL2_TTF_INCLUDE_DIR})

find_package(SDL2_image REQUIRED)
include_directories(${SDL2_IMAGE_INCLUDE_DIR})

#include_directories(sudoku assets)

add_executable(sudoku
        main.cpp

        Game.cpp
        Game.h

        CellObject.cpp
        CellObject.h
        )


target_link_libraries(sudoku ${SDL2_LIBRARIES} ${SDL2_TTF_LIBRARIES} ${SDL2_IMAGE_LIBRARIES})
