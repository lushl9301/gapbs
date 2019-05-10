cmake_minimum_required(VERSION 3.12)
project(sparsify)

set(CMAKE_CXX_STANDARD 14)

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
add_executable(sparsify
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
