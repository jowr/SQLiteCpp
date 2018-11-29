# CMake file for compiling the sqlite3 library under Windows (for ease of use)
#
# Copyright (c) 2012-2016 Sebastien Rombauts (sebastien.rombauts@gmail.com)
#
# Distributed under the MIT License (MIT) (See accompanying file LICENSE.txt
# or copy at http://opensource.org/licenses/MIT)

# Create a library that respects the default CMake settings
set(CMAKE_INCLUDE_CURRENT_DIR ON)
if(BUILD_SHARED_LIBS OR SQLITE3_BUILD_SHARED_LIBS)
  add_library(sqlite3 SHARED sqlite3.c sqlite3.h)
else(BUILD_SHARED_LIBS OR SQLITE3_BUILD_SHARED_LIBS)
  add_library(sqlite3 STATIC sqlite3.c sqlite3.h)
endif(BUILD_SHARED_LIBS OR SQLITE3_BUILD_SHARED_LIBS)
