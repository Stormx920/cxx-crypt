cmake_minimum_required(VERSION 3.27.1)
project(cxx-crypt)
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

file(GLOB SOURCE_FILES "src/lib/*.hpp" "src/*.cpp")

include_directories(src/lib)

#set(SOURCE_FILES "src/*.cpp")

set(CMAKE_CXX_COMPILER=/usr/bin/clang++)

add_executable(cxx-crypt ${SOURCE_FILES})
set_target_properties(cxx-crypt PROPERTIES
    RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/../bin
)
