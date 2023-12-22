cmake_minimum_required(VERSION 3.10)
project(projectName VERSION 1.0)

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS}")
set(CMAKE_C_COMPILER gcc)


#define out paths as /build
#set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/build)
#set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/build)
#set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/build)
#set(CMAKE_SUPPRESS_REGENERATION true)
#set(CMAKE_SKIP_BUILD_RPATH true)

#add source files to executable
file(GLOB_RECURSE SRC_FILES src/*.c)
#.exe
add_executable(projectName ${SRC_FILES})
#add_library(projectName STATIC ${SRC_FILES})


#includes
target_include_directories(projectName PRIVATE src)
#target_include_directories(projectName PUBLIC src/3rdParty)

#libraries
#find_package(SDL2 REQUIRED)
#target_include_directories(projectName PUBLIC ${SDL2_INCLUDE_DIRS})
#target_link_libraries(projectName PUBLIC m)
