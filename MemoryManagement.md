# Javascript Memory Management
- Memory Allocation Explained
- Memory Optimization Discussed

## Memory Allocation Explained
Low-level languages like C and C++ requires you to allocate and free up memory manually. This makes them much more difficult to work with and user or developer's issue. However, Higher-level languages like Javascript, Python and C# automatically allocates memory when objects or primitives types variables are created and frees these spaces when they are not in use anymore. This process is called ```GARBAGE COLLECTION```

In javascript (Browser and Node or Server environment) primitive Data types like: ```Number``` ```String``` ```Boolean``` ```Null``` ```Undefined``` ```Symbol``` ```BigInt``` have their values stored in a ```STACK``` and this is because the size of the value in this Data types are somewhat known. Object Data types like: ```Object``` ```Array``` and ```Function``` have their references stored in a ```MEMORY HEAP``` . When data is access in the heap, they are accessed through their reference not value.<br/><br/>
(Illustration)[https://github.com/ajayioyetomi/Javascript-Memory-Management/blob/main/memory-allocation.png?raw=true]



