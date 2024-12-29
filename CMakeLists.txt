cmake_minimum_required(VERSION 3.28)

set(CMAKE_CXX_STANDARD 23)
set(CXX_STANDARD C++23)
set(target project_name)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin")

project(${target} VERSION 1.0 LANGUAGES CXX)
add_executable(${target} src/main.cpp)

file(GLOB sources "src/*.cpp")
file(GLOB includes "src/*.h")
add_library(ProjectName STATIC ${includes} ${sources})
target_link_libraries(${target} PRIVATE ProjectName)

include(CTest) # calls enable_testing()
if(BUILD_TESTING)
    add_subdirectory(tests)
endif()
