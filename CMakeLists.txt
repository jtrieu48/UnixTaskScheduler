cmake_minimum_required(VERSION 3.15)
project(finalProject)

set(CMAKE_CXX_STANDARD 14)
add_executable(${CMAKE_PROJECT_NAME}.out
        src/main.cpp )

# set this flag when running coverage tests in Clion
#set(CMAKE_CXX_FLAGS "--coverage")

# generate debug information
set(CMAKE_CXX_FLAGS "-g")

include_directories(src)
add_subdirectory(src)

add_subdirectory(test)

target_link_libraries(${CMAKE_PROJECT_NAME}.out ${CMAKE_PROJECT_NAME}_lib)
