cmake_minimum_required(VERSION 3.10)
set( TARGET_NAME imgui )

add_library( ${TARGET_NAME} 
          imconfig.h
          imgui.h
          imgui.cpp
          imgui_draw.cpp
          imgui_internal.h
          imgui_widgets.cpp
          imstb_rectpack.h
          imstb_textedit.h
          imstb_truetype.h
          imgui_demo.cpp
)

target_include_directories(${TARGET_NAME} PUBLIC ${CMAKE_CURRENT_SOURCE_DIR} )
