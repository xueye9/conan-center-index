cmake_minimum_required(VERSION 3.15)
project(test_package LANGUAGES CXX)

find_package(realsense2 REQUIRED CONFIG)

add_executable(${PROJECT_NAME} test_package.cpp)
target_link_libraries(${PROJECT_NAME} PRIVATE realsense2::realsense2)
target_compile_features(${PROJECT_NAME} PRIVATE cxx_std_11)
