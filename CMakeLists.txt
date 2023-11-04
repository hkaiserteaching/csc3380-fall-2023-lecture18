cmake_minimum_required(VERSION 3.19)
project(fall2023-csc3380-lecture18)

set(CMAKE_CXX_STANDARD 20)

find_package(FLTK CONFIG REQUIRED)

set(fltk_toolkit_sources
    code/Graph.cpp
    code/GUI.cpp
    code/Simple_window.cpp
    code/Window.cpp
)

add_executable(functions code/functions.cpp ${fltk_toolkit_sources})
target_link_libraries(functions PRIVATE fltk fltk_images)

add_executable(e_power_x code/e_power_x.cpp ${fltk_toolkit_sources})
target_link_libraries(e_power_x PRIVATE fltk fltk_images)
