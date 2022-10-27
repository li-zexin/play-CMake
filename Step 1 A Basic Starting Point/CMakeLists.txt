# Any project's top most CMakeLists.txt must start by specifying a minimum CMake version using the cmake_minimum_required() command. This establishes policy settings and ensures that the following CMake functions are run with a compatible version of CMake.
cmake_minimum_required(3.19.5)

# To start a project, we use the project() command to set the project name. 
project(play-CMake c)

# the add_executable() command tells CMake to create an executable using the specified source code files.
add_executable(play-CMake main.c)


