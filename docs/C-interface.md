Bitprim's C interface, the [bitprim-node-cint](https://github.com/bitprim/bitprim-node-cint) project, is built on top of the C++ interface. Asides from allowing a C library or program to consume all the Bitprim functionality, it can act as the base to create bindings for many current popular programming languages, such as Javascript, C\#,  Golang, Java and Python. All of these languages can interface easily with C, but not with C++.

Granted, the Object Oriented paradigm is lost when transitioning to C, but it can be "recovered" when implementing a binding in an object oriented language such as C\#. In such a context, classes can be built in order to give application programmers a friendlier interface for integrating Bitcoin in their projects, bridging the gap created by C/C++'s inherent complexity.

Therefore, Bitprim's interface is not really meant to be consumed directly, but as the basis for a higher level binding in another language. To make this task easier, most functions will receive a parameter which will wrap the implicit object \(this\), so that OOP can be preserved in the binding if possible.

## Resource management

---

To avoid memory leaks, all C functions which allocate memory that must be released by the user are clearly documented as such. When implementing a binding on top of the C interface, it is advisable to use the [RAII idiom](https://www.hackcraft.net/raii/) whenever possible to relieve the application programmer from the burden of manual memory management.

## Basic structure - memory management

---

Since this is C we're dealing with, there is nothing beyond a set of functions and some user defined types, but there is [a structure](https://github.com/bitprim/bitprim-node-cint/tree/master/include/bitprim/nodecint) nevertheless. The main "entry point" for the interface are the functions from [executor\_c.h](https://github.com/bitprim/bitprim-node-cint/blob/master/include/bitprim/nodecint/executor_c.h) and the types defined in [primitives.h](https://github.com/bitprim/bitprim-node-cint/blob/master/include/bitprim/nodecint/primitives.h). To start consuming node functionality, the first step is calling one of these functions:

```c
executor_t executor_construct(char const* path, FILE* sout, FILE* serr);

executor_t executor_construct_fd(char const* path, int sout_fd, int serr_fd);
```

Any function with the **construct** suffix will create an object in dynamic memory, which will have to be released by calling the associated **destruct**:

```c
void executor_destruct(executor_t exec);
```

This pattern will be seen with many other types; whenever an object is created by the user with a construct function, it will need to be released with destruct as soon as it is no longer needed.

Another case is when a function needs to create an object for returning it. For example, if we wanted to fetch the transaction history for a specific Bitcoin address, we could use the fetch\_history function:

```c
void fetch_history(executor_t exec, payment_address_t address, size_t limit, size_t from_height,
                   history_fetch_handler_t handler);
```

There's another concept in play here: a pointer to function acting as a callback. Looking at the definition for history\_fetch\_handler\_t in primitives.h:

```c
typedef void (*history_fetch_handler_t)(int error, history_compact_list_t history);
```

The second parameter, history, is created dynamically, and therefore must be released by the user, even if he didn't create it. This has to be done this way because there is no way for the C interface to know when the user is done using history. Therefore, it is up to him/her to call history\__compact\_\_list_\_destruct\(history\)._

The remaining header files follow these conventions; transaction.h contains functions for manipulating a transaction object, block.h for blocks, and so on. Keep in mind that objects must be destroyed manually.

## API documentation

---

[Detailed documentation](api.md)


