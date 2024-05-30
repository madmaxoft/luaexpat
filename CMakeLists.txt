cmake_minimum_required (VERSION 3.13)
project (luaexpat)

add_library(luaexpat SHARED
	lxplib.cpp
	lxplib.h
)

add_library(luaexpat-static STATIC
	lxplib.cpp
	lxplib.h
)

target_link_libraries(luaexpat
	expat-static
	lua
)

target_link_libraries(luaexpat-static
	expat-static
	lua-static
)
