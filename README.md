# Java_lab
Some notes

CArchitecture
The JVM architecture consists of several key components:

Class Loader Subsystem: Loads, links, and initializes classes and interfaces.

Loading: Finds and loads class files.
Linking: Verifies and prepares classes for the JVM.
Initialization: Initializes class variables and executes static initializers.
Runtime Data Areas: Memory areas used by the JVM during execution.

Method Area: Stores class structure like metadata, the constant pool, and the code for methods.
Heap: Runtime storage for objects and arrays.
Java Stack: Stores frames, each corresponding to a method call, including local variables, operand stack, and frame data.
Program Counter (PC) Register: Points to the current instruction in a method.
Native Method Stack: Used for native methods written in languages other than Java.
Execution Engine: Executes the bytecode.

Interpreter: Interprets bytecode instructions one by one.
Just-In-Time (JIT) Compiler: Compiles bytecode into native machine code for faster execution.
Garbage Collector (GC): Manages memory by reclaiming memory used by unreachable objects.
Native Method Interface (JNI): Enables Java code to call or be called by native applications and libraries.

Native Method Libraries: Libraries required by the native method interface.

Programming Languages Used for JVM
The JVM itself is typically written in low-level programming languages that provide the necessary performance and access to system resources:

C: The primary language used for writing the JVM. It provides low-level memory management and system interaction capabilities.
C++: Used for more complex parts of the JVM, such as the HotSpot Just-In-Time (JIT) compiler and other performance-critical components.
Assembly Language: Used for certain parts of the JVM that require direct hardware interaction or performance optimization.
Key Components in Detail
Class Loader Subsystem

Bootstrap Class Loader: Part of the JVM, loads the core Java libraries.
Extension Class Loader: Loads classes from the extension directories.
Application Class Loader: Loads classes from the application's classpath.
Runtime Data Areas

Heap Memory: Divided into young generation (Eden space, survivor spaces) and old generation. Managed by the garbage collector.
Method Area: Stores class-level data like runtime constant pool, field and method data, and code for methods.
Java Stack: Each thread has its own stack, storing frames for each method call.
Execution Engine

Interpreter: Translates bytecode to machine code line by line.
JIT Compiler: Compiles entire bytecode to machine code at runtime for performance. Uses techniques like method inlining, loop unrolling, etc.
Garbage Collector: Automatically manages memory, deallocating objects that are no longer reachable.
Performance Enhancements
Adaptive Optimization: The JVM can optimize the execution of frequently run methods by re-compiling them with more aggressive optimizations.
Tiered Compilation: Combines the benefits of both the interpreter and the JIT compiler by using multiple levels of compilation.
