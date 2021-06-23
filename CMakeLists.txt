cmake_minimum_required(VERSION 3.13)
project (tolua++)

include_directories ("${PROJECT_SOURCE_DIR}/../../src/")
include_directories ("${PROJECT_SOURCE_DIR}/include/")
include_directories ("${PROJECT_SOURCE_DIR}/../")
include_directories ("${PROJECT_SOURCE_DIR}")

SET (LIB_SOURCE
	src/lib/tolua_event.cpp
	src/lib/tolua_is.cpp
	src/lib/tolua_map.cpp
	src/lib/tolua_push.cpp
	src/lib/tolua_to.cpp
)

add_library(tolualib ${LIB_SOURCE})
target_link_libraries(tolualib lualib)
