cmake_minimum_required(VERSION 3.23.2)

project(imgui)

add_library(imgui STATIC imgui.h imgui_internal.h imgui.cpp imgui_demo.cpp imgui_draw.cpp imgui_widgets.cpp imgui_tables.cpp
            backends/imgui_impl_glfw.h backends/imgui_impl_glfw.cpp backends/imgui_impl_opengl3.h backends/imgui_impl_opengl3.cpp)
target_include_directories(imgui PUBLIC .)

target_link_libraries(imgui glad)
target_link_libraries(imgui glfw)