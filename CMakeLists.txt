cmake_minimum_required(VERSION 3.10)
set( TARGET_NAME imgui )

file( GLOB HEADER_FILES "*.h" "*.hpp" )
file( GLOB SOURCE_FILES "*.cpp" )

if (NOT DEFINED ImGui_LIBRARY_TYPE)
	set(ImGui_LIBRARY_TYPE "STATIC")
	message( "-- ImGui_LIBRARY_TYPE set to " ${ImGui_LIBRARY_TYPE} )
endif ()

add_library( ${TARGET_NAME} ${ImGui_LIBRARY_TYPE} ${HEADER_FILES} ${SOURCE_FILES} )
target_include_directories(${TARGET_NAME} PUBLIC ${CMAKE_CURRENT_SOURCE_DIR} )