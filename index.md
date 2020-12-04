---
layout: default
title: C++ for HPC 
has_children: false
nav_order: 1
---

# {{ page.title }}

![](./public/logo.png){:height="120px" width="120px"}

This is the website for ORNL's training introduction to *C++ for HPC applications*. The goal is to expose the audience to the features of modern C++ and how they can be used and exploited considering performance aspects. We'd attempt to cover the gap between C++ programming resources and computer science topics.

Topics covered: memory management, input/output I/O, STL containers, RAII, parallel algorithms, move semantics, threads, combining MPI and modern C++, GPU programming using Nvidia CUDA and Thrust, and AMD ROC.

Much of the material is from:

- Strostroup's [The C++ Programming Language 4th Edition](https://www.stroustrup.com/4th.html)
- [C++ core guidelines](https://isocpp.github.io/CppCoreGuidelines/CppCoreGuidelines)
- [E4S open source software stack](https://e4s-project.github.io/Resources/ProductInfo.html)

What this covers:
  - Underlying performance concepts
  - An overview of modern C++ features in HPC 
  - Modern C++ and performance implications
  - Examples from open source implementations
    
What this doesn't cover:
  - A programming course
  - Computer science research topics
  - Hardware topics

Contents include:

* Intro
  - C++ standards
  - C still matters, but C++ is "free"
  - C++ towards Exascale
  - Summary and advice

* [Memory Management]({{ page.url | prepend: site.github.url }}memory/index): 
  - Memory model: pointers, allocation, alignment
  - RAII
  - C++11 move semantics
  - C++11 Callable objects (e.g. functions)
  - C++11 smart pointers: `std::unique_ptr` and `std::shared_ptr`
  - C++17: `std::any`, `std::optional`, `std::variant`
  - Error handling: exceptions and assert
  - Summary and advice
  
* [STL]({{ page.url | prepend: site.github.url }}stl/index):
  - Templates
  - Containers, iterators
  - [`std::vector`]({{ page.url | prepend: site.github.url }}stl/vector)
  - `std::map`, `std::unordered_map`, `std::set`, `std::unordered_set`
  - `std::multimap`
  - `std::list`
  - `std::deque`
  - `<algorithm>`
  - Summary and advice

* Parallel programming
  - Memory models: memory-shared, memory-distributed, GPUs
  - C++11 data `<thread>` and task `std::async` parallelism
  - C++17 parallel algorithms
  - MPI and modern C++
  - GPU: Nvidia CUDA, Thrust
  - GPU: AMD ROC
  - Summary and advice
