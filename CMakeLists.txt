cmake_minimum_required(VERSION 3.10)
set( TARGET_NAME imgui )

file( GLOB HEADER_FILES "*.h" "*.hpp" )
file( GLOB SOURCE_FILES "*.cpp" )

#FIXME make STATIC
add_library( ${TARGET_NAME} SHARED ${HEADER_FILES} ${SOURCE_FILES} )
target_include_directories(${TARGET_NAME} PUBLIC ${CMAKE_CURRENT_SOURCE_DIR} )