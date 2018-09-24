find_package(SDL2 REQUIRED)
find_package(OpenGL REQUIRED)

add_library(imgui STATIC
  ${CMAKE_CURRENT_SOURCE_DIR}/src/imgui.cpp
  ${CMAKE_CURRENT_SOURCE_DIR}/src/imgui_demo.cpp
  ${CMAKE_CURRENT_SOURCE_DIR}/src/imgui_draw.cpp
  ${CMAKE_CURRENT_SOURCE_DIR}/src/imgui_impl_opengl3.cpp
  ${CMAKE_CURRENT_SOURCE_DIR}/src/imgui_impl_sdl.cpp
  )
target_include_directories(imgui PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/include/imgui/ ${SDL2_INCLUDE_DIRS}) # ImGui expects the includes to be includable with #include "imgui.h"
target_compile_options(imgui PRIVATE "-std=c++1z" "-Wno-everything")


  
