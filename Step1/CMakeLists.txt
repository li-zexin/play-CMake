# 1: Set the minimum required version of CMake to be 3.10
cmake_minimum_required(VERSION 3.10)

# 2: Create a project named Tutorial
# 7: Set the project version number as 1.0 in the project command
project(Tutorial VERSION 1.0)

# 6: Set the variable CMAKE_CXX_STANDARD to 11 and the variable CMAKE_CXX_STANDARD_REQUIRED to True
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# 8: Use configure_file to configure and copy TutorialConfig.h.in to TutorialConfig.h
configure_file(TutorialConfig.h.in TutorialConfig.h)

# 3: Add an executable called Tutorial to the project
add_executable(Tutorial tutorial.cxx)

# 9: Use target_include_directories to include ${PROJECT_BINARY_DIR}
target_include_directories(Tutorial PUBLIC "${PROJECT_BINARY_DIR}")
