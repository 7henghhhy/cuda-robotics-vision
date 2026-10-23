cmake_minimum_required(VERSION 3.24)

project(cuda_robotics_vision LANGUAGES CXX CUDA)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CUDA_STANDARD 17)
set(CMAKE_CUDA_STANDARD_REQUIRED ON)

# CUDA targets will be added after the Day 15 environment check and Day 17
# vector_add implementation. Keeping this file minimal avoids claiming that
# the toolkit or a specific GPU architecture has already been verified.
