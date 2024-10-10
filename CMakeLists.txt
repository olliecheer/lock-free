cmake_minimum_required(VERSION 3.16)
project(lock-free)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)



include(FetchContent)
FetchContent_Declare(
  googletest
  URL https://github.com/google/googletest/archive/71815bbf7de6e10c11821d654a2fae2cf42de0f7.zip
)
FetchContent_Declare(
  benchmark
  URL https://github.com/google/benchmark/archive/24e0bd827a8bec8121b128b0634cb34402fb3259.zip
)

FetchContent_MakeAvailable(googletest)
FetchContent_MakeAvailable(benchmark)




include_directories(${CMAKE_SOURCE_DIR})


add_subdirectory(bench)
add_subdirectory(test)

