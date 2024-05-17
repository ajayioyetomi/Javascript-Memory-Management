# Javascript Memory Management
- Definition
- Memory lifecycle
- Memory Allocation And Engine Storage
- References in memory management
- Memory Optimization

## Definition
The practice of managing and coordinating memory in your software is known as memory management. It makes sure that memory blocks are correctly managed and distributed so that the application and other processes that are currently running have the memory they require to complete their tasks

## Memory Lifecycle
There are 3 phases or parts of the memory life cycle which are the same for all programming languages are;
- Allocation: When we declare a variable, we need to allocate the memory. In JavaScript, this is handled automatically.
- Using the allocated memory, by using it in your code expression.
- Releasing the memory when not in use anymore. In JavaScript, this is handled automatically (it is called JavaScript garbage collection).


## Memory Allocation And Engine Storage
Low-level languages like C and C++ requires you to allocate and free up the memory manually. This makes them much more difficult to work with and user or developer's issue. However, Higher-level languages like Javascript, Python and C# automatically allocates memory when objects or primitive types variables are created and frees these spaces when they are not in use anymore. This process is called ```GARBAGE COLLECTION```.

JavaScript engines store their data in two places; the Stack Memory and the Heap Memory. In javascript (Browser and Node or Server environment) primitive Data types like: ```Number``` ```String``` ```Boolean``` ```Null``` ```Undefined``` ```Symbol``` ```BigInt``` have their values stored in a ```STACK MEMEORY```. Object Data types like: ```Object``` ```Array``` and ```Function``` have their references stored in a ```HEAP MEMEORY``` .When data is access in the heap, they are accessed through their reference not value. [Image to Illustrate or virtualize](https://github.com/ajayioyetomi/Javascript-Memory-Management/blob/main/memory-allocation.png)

- Stack Memory: Static Memory allocation: is a type of data structure that uses the Last-in-First-out (LIFO) manner, to store static data. Because of its fixed size, known during compile time by the engine, it is static
- Heap Memory: Dynamic memory allocation: Heap is another way of storing data in memory. This is used for storing objects (in this context here, our objects mean both object and functions) in memory.

The JavaScript heap doesn’t allocate a fixed amount of memory like the stack does, instead, it allocates more space during run time i.e the size is known at run time and there is no limit for its object memory.


 ```Memory Leak```is a memory allocation that the JavaScript engine is unable to recover. Also memory leak said to have occured if the Garbage Collector cannot help to free up unused memory space. Memory leak can occur in javascript application due to different reasons. 

|Stack Memory | Heap Memory| 
|-------------|------------|
|Stores primitive data types and values|Store object data types and values|
|Size is known at compile time| Size is known at run time|
|Allocate a fixed amount memory|No limit to amount of memory|



#### Common causes of memory leaks
- Using needless global variables or functions
- Closures
- Timers not cleared
- Event listerners not removed
- cached variables not cleared

## References in Memory management
All variables start by pointing to the stack. A reference to the item in the heap is stored in the stack if the value is not primitive. We need to maintain a reference to the heap in the stack since the memory of the JavaScript heap is not organized in any specific way. The objects in the heap can be compared to residences, with references serving as the references' addresses.

## Memory Optimization
Memory optimization is generally done by the garbage collector in javascript and most high-level language, but their are the different ways or best practice to avoid memory leakage in your applicaiton or code.
#### Common practice to optimize memeory usage
- Minimize global variable usage.
- Set references/object types to null or reassign them to other value needed.
- Object pool
- Proper event listener management or usage
- Proper management of timer functions



