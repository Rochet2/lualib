#
# Copyright (C) 2010 - 2014 Eluna Lua Engine <http://emudevs.com/>
# This program is free software licensed under GPL version 3
# Please see the included DOCS/LICENSE.md for more information
#

file(GLOB lualib_sources *.c *.h)
list(REMOVE_ITEM lualib_sources ${CMAKE_CURRENT_SOURCE_DIR}/lua.c)
list(REMOVE_ITEM lualib_sources ${CMAKE_CURRENT_SOURCE_DIR}/luac.c)

set(lua_STAT_SRCS
  ${lualib_sources}
)

include_directories(
  ${CMAKE_CURRENT_SOURCE_DIR}
)

add_library(lualib STATIC ${lua_STAT_SRCS})
