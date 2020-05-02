cmake_minimum_required (VERSION 3.13)
project (luaexpat)

include_directories ("${PROJECT_SOURCE_DIR}/../../src/")
include_directories ("${PROJECT_SOURCE_DIR}/../")

file(GLOB SOURCE
    "*.c"
    "*.h"
)

add_library(luaexpat ${SOURCE})

target_link_libraries(luaexpat expat)
