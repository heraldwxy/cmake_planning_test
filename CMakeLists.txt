cmake_minimum_required(VERSION 3.29.2)
project(planning
    VERSION 0.0.1
    DESCRIPTION "module directory cmake configuration"
    HOMEPAGE_URL "https://github.com/heraldwxy/cmake_planning_test"
    LANGUAGES CXX
)

set(CMAKE_CXX_STANDARD 17)
enable_testing()

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)
set(PNC_Map_Dir ${CMAKE_SOURCE_DIR}/src/pnc_map)
set(Process_Dir ${CMAKE_SOURCE_DIR}/src/process)
set(Show_Result_Dir ${CMAKE_SOURCE_DIR}/src/show_result)

set(EIGEN3_INCLUDE_DIR "C:/Users/WANGX/Downloads/eigen-3.4.0/eigen-3.4.0")
list(APPEND CMAKE_MODULE_PATH "${EIGEN3_INCLUDE_DIR}/cmake")
message("CMAKE_MODULE_PATH=${CMAKE_MODULE_PATH}")

find_package(Eigen3 3.4 REQUIRED)
if(TARGET Eigen3::Eigen)
    message(STATUS "-------Eigen3 3.4 found in ${CMAKE_MODULE_DIR}--------")
endif()

add_subdirectory(src)
add_subdirectory(test/map_test)

