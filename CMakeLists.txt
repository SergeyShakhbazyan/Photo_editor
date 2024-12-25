cmake_minimum_required(VERSION 3.30)
project(Photo_editor)

set(CMAKE_CXX_STANDARD 20)

set(CMAKE_PREFIX_PATH  "Users/sergeyshakhbazyan/Qt/6.6.1/macos")

find_package(Qt6 REQUIRED COMPONENTS Widgets)

include_directories(${OpenCV_INCLUDE_DIRS})
include_directories(${Qt6Widgets_INCLUDE_DIRS})

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

include_directories(${Qt6Widgets_INCLUDE_DIRS})

add_executable(Photo_editor main.cpp)

target_link_libraries(Photo_editor Qt6::Widgets)
target_link_libraries(Photo_editor ${OpenCV_LIBS})