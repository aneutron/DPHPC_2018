cmake_minimum_required(VERSION 3.3)
project(DPHPC)

# Set compile flags
set(CMAKE_CXX_FLAGS "-std=c++11")

# Support for vim YCM
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

# Set directory fo binaries 
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin")

# Precise includes
include_directories("include/")

# Gather source for main executable 
file(GLOB SRCS src/*)

# Add executable 
add_executable(exec ${SRCS})