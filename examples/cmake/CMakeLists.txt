cmake_minimum_required(VERSION 3.1.0)

project(hello_librealsense2)

# Find librealsense2 installed package
# We provide a search hint to the default Windows installation path
find_package(realsense2 REQUIRED HINTS "Intel RealSense SDK 2.0")

# Enable C++11
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED TRUE)

# Add the application sources to the target
add_executable(${PROJECT_NAME} hello_librealsense2.cpp)

# Link librealsense2 to the target
target_link_libraries(${PROJECT_NAME} ${realsense2_LIBRARY})
