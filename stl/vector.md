---
layout: default
title: "std::vector"
has_children: false
parent: STL Containers
---

## std::vector

`std::vector` is a high-level container describing a contiguous piece of element "typed" (_e.g._ `float`, `int`, custom objects) memory. In its simplest form it can be thought of a self-describing pointer to the data, with descriptors for the current number of elements (size), total allocated memory (capacity). In fact, GNU's implementation of `std::vector` returns a size of 24 bytes for `sizeof` accounting for these three pointers, each of 8 bytes.
Access to any element 


`std::vector` underlying contiguous memory representation with the three stores iterators (pointers).
```
begin <---------size------------------> end                       capacity
| | | | | | | | | | | | | | | | | | | | |X|X|X|X|X|X|X|X|X|X|X|X|X|
|      logical valid region             |    undefined behavior   |
```

---
**NOTE**
Memory contiguity is required to get performance in HPC systems due to its vectorization and cache friendly (zero per-element overhead) characteristics.
---


The following functions can be used to modify the underlying memory:

- **reserve**: increases the capacity

	memory growth is implementation dependent as **must** be considered when programming with the 

	```
	std::vector<int> myData(4); // constructor will always initialize
	Memory:
	|0|0|0|0|

	myData.reserve(5);
	Memory (gcc implementation):
	|0|0|0|0|X|X|X|X|

	myData.capacity(); // 8, power of 2
	myData.size(); // still 4, reserve doesn't not modify size
	```

- **resize**: increases the size (end-begin) and capacity (only if required).


Summary:

- Use `std::vector` as your first choice container for array like structures
- Be familiar with underlying memory effects of `resize`, `reserve`, `assign` and constructor
- Prefer element access (for each) or iterator access over pointer (&v[index]) access
- Understand trade-offs between memory initialization and safety 
- Understand allocation and deallocation costs
