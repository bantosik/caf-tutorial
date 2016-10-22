cmake_minimum_required(VERSION 3.5)

project(caf_tutorial)
set (CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake/Modules/")

message(status "Starting running my package")
find_package(CAF REQUIRED COMPONENTS core)

include_directories(${CAF_INCLUDE_DIRS})

set(SOURCE_FILES main.cpp)

add_executable(caf_tutorial ${SOURCE_FILES})

target_link_libraries (caf_tutorial ${CAF_LIBRARIES})