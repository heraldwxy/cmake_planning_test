cmake_minimum_required(VERSION 3.29.2)
project(planning
    VERSION 0.0.1
    DESCRIPTION "module directory cmake configuration"
    HOMEPAGE_URL "https://github.com/heraldwxy/cmake_planning_test"
    LANGUAGES CXX
)

set(CMAKE_CXX_STANDARD 17)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)
set(PNC_Map_Dir ${CMAKE_SOURCE_DIR}/src/pnc_map)
set(Process_Dir ${CMAKE_SOURCE_DIR}/src/process)

add_subdirectory(src)