cmake_minimum_required(VERSION 3.10)
project(yolov5_demo)

set(CMAKE_CXX_STANDARD 11)

# 直接包含根目录，确保能找到 postprocess.h、yolov5.h
include_directories(${CMAKE_CURRENT_SOURCE_DIR})

# 生成可执行文件，直接用根目录的 main.cc
add_executable(yolov5_demo main.cc)

# 链接必要的库
target_link_libraries(yolov5_demo -lm -pthread)
