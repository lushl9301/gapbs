cmake_minimum_required(VERSION 3.12)
project(prune)

set(CMAKE_CXX_STANDARD 14)
find_package(OpenMP)
if (OPENMP_FOUND)
    set (CMAKE_C_FLAGS "${CMAKE_C_FLAGS} ${OpenMP_C_FLAGS}")
    set (CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${OpenMP_CXX_FLAGS}")
    set (CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} ${OpenMP_EXE_LINKER_FLAGS}")
endif()

include_directories(src)
add_executable(converter
               src/benchmark.h
               src/bitmap.h
               src/builder.h
               src/command_line.h
               src/converter.cc
               src/generator.h
               src/graph.h
               src/platform_atomics.h
               src/pvector.h
               src/reader.h
               src/sliding_queue.h
               src/timer.h
               src/util.h
               src/writer.h)
add_executable(sssp
               src/benchmark.h
               src/bitmap.h
               src/builder.h
               src/command_line.h
               src/generator.h
               src/graph.h
               src/platform_atomics.h
               src/pvector.h
               src/reader.h
               src/sliding_queue.h
               src/sssp.cc
               src/timer.h
               src/util.h
               src/writer.h)
