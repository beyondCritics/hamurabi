cmake_minimum_required(VERSION 3.19)

project(
  hamurabi 
  VERSION 1.0
  DESCRIPTION "Hamurabi: Classis BASIC gaming." 
  LANGUAGES C)

set(CMAKE_C_STANDARD 11)
set(CMAKE_C_STANDARD_REQUIRED ON)
set(CMAKE_C_EXTENSIONS OFF)

add_executable(hamurabi main.c city.c)
 
set(default_build_type "Release")
if (${CMAKE_BUILD_TYPE} STREQUAL "Release")
  set_property(TARGET hamurabi PROPERTY INTERPROCEDURAL_OPTIMIZATION TRUE)
endif()


