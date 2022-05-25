cmake_minimum_required(VERSION 3.10)

project(libserialport)
include_directories(${PROJECT_SOURCE_DIR})
add_definitions(-DLIBSERIALPORT_MSBUILD)
add_library(${PROJECT_NAME} SHARED serialport.c timing.c windows.c)
target_link_libraries(${PROJECT_NAME} SetupAPI.lib)
