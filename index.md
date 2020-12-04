---
layout: default
title: C++ for HPC 
has_children: false
nav_order: 1
---

# {{ page.title }}

![](./public/logo.png){:height="120px" width="120px"}

This is the website for ORNL's training introduction to *C++ for HPC applications*. 

The goal of these courses is to understand modern C++ (C++11, C++17) in high-performance computing applications including usage examples. Topics covered: memory management, input/output I/O, STL containers, RAII, parallel algorithms, move semantics, threads, combining MPI and modern C++, GPU programming using Nvidia CUDA and Thrust, and AMD ROC.

Contents include:

* [Memory Management]({{ page.url | prepend: site.github.url }}memory/index): 
  - RAII
  - Memory alignment
  - Move semantics
  - Callable objects (e.g. functions)
  - C++11 smart pointers: `std::unique_ptr` and `std::shared_ptr`
  - C++17: `std::any`, `std::optional`, `std::variant`
  - Error handling: exceptions
  
* [STL Containers]({{ page.url | prepend: site.github.url }}stl/index):
  - iterators
  - [`std::vector`]({{ page.url | prepend: site.github.url }}stl/vector)
  - `std::map`, `std::unordered_map`, `std::set`, `std::unordered_set`
  - `std::multimap`
  - `std::list`
  - `std::deque`
  - `<algorithm>`

* Parallel programming
  - C++11 data `<thread>` and task `std::async` parallelism
  - C++17 parallel algorithms
  - MPI and modern C++
  - GPU: Nvidia CUDA, Thrust
  - GPU: AMD ROC
