file(GLOB PROJECT_SOURCES
    *.h
    */*.h
    *.cpp
    */*.cpp
    )
message(STATUS "PROJECT_SOURCES:\n${PROJECT_SOURCES}")

cmake_minimum_required(VERSION 3.10)
project(tcp-echo-client)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
set(CMAKE_BUILD_TYPE Debug)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Wextra -Werror -pedantic")
set(CMAKE_CXX_FLAGS_DEBUG "${CMAKE_CXX_FLAGS_DEBUG} -ggdb")

include_directories(SYSTEM /usr/include/c++/7)
add_executable(tcp-echo-client ${PROJECT_SOURCES})

