cmake_minimum_required(VERSION 3.12)
project(LaneDetectionHough)

set(CMAKE_CXX_STANDARD 11)

aux_source_directory(./ SRC_DIR)
find_package(OpenCV REQUIRED)
include_directories(${OpenCV_INCLUDE_DIRS})

add_executable(LaneDetectionHough ${SRC_DIR})

target_link_libraries(LaneDetectionHough ${OpenCV_LIBS})