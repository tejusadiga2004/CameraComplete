# The Flutter tooling requires that developers have CMake 3.10 or later
# installed. You should not increase this version, as doing so will cause
# the plugin to fail to compile for some customers of the plugin.
cmake_minimum_required(VERSION 3.10)

project(camera_complete_library VERSION 0.0.1 LANGUAGES C)

add_library(camera_complete SHARED
  "camera_complete.c"
)

set_target_properties(camera_complete PROPERTIES
  PUBLIC_HEADER camera_complete.h
  OUTPUT_NAME "camera_complete"
)

target_compile_definitions(camera_complete PUBLIC DART_SHARED_LIB)
