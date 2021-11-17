# Review Session for Section 17 - 18

## Correction and Clarification

# Smart Pointer

- Since C++ 11, you can use smart pointers to dynamically allocate memory and not worry about deleting the memory when you are finished using it. A smart pointer automatically
deletes a chunk of dynamically allocated memory when the memory is no longer being used. This helps to prevent memory leaks from occurring. 

- We don't need to use `delete` to release the memory any more for smart pointers, in comparison to raw pointers. 

- Don't forget to use `#include <memory>`

 Here is an example of the syntax for defining a unique_ptr that points to a dynamically allocated `Rectangle` object:
 ``` cpp
unique_ptr<Rectangle> rectanglePtr(new Rectangle);

 ```

This statement defines a `unique_ptr` named `rectanglePtr` that points to a dynamically allocated Rectangle object. Here are some details about the statement:
- The notation `<Rectangle>` that appears immediately after `unique_ptr` indicates that the pointer can point to a Rectangle .
- The name of the pointer is `rectanglePtr` .
- The expression `new Rectangle` that appears inside the parentheses allocates a chunk of memory to hold a `Rectangle`. The address of the chunk of memory will be assigned
to the `rectanglePtr` pointer.

# Exceptions

- The line containing a throw statement is known as the throw point . When a throw statement is executed, control is passed to another part of the program known as an exception
handler . When an exception is thrown by a function, the function aborts.
## Review Questions

- To handle an exception, a program must have a `try/catch` construct. The general format of the `try/catch` construct is:
``` cpp
try
{
// code here calls functions or object member
// functions that might throw an exception.
}
catch( ExceptionParameter )
{
// code here handles the exception
}
// Repeat as many catch blocks as needed.
```
-  There are two possible ways for a thrown exception to go uncaught. The first possibility is for the try/catch construct to contain no catch blocks with an exception parameter of the
right data type. The second possibility is for the exception to be thrown from outside a try block. In either case, the exception will cause the entire program to abort execution.

- Once an exception has been thrown, the program cannot jump back to the throw point. The function that executes a throw statement will immediately terminate. If that function
was called by another function, and the exception is not caught, then the calling function will terminate as well. This process, known as unwinding the stack, continues
for the entire chain of nested function calls, from the throw point, all the way back to the try block. 

- If an exception is thrown by the member function of a class object, then the class destructor is called. If statements in the try block or branching from the try block created any other
objects, their destructors will be called as well.

Q1. What is the difference between a try block and a catch block?


<details>

<summary> Click me to show the answer below!</summary>

try block is used to contain a block of code executing any statements that might directly or indirectly cause an exception to be thrown. The try block is immediately followed by one or more catch blocks,
which are the exception handlers. A catch block starts with the key word catch , followed by a set of parentheses containing the definition of an exception parameter.

</details>


Q2. What happens if an exception is thrown, but not caught?

<details>

<summary> Click me to show the answer below!</summary>

Program terminates. 

</details>


Q3. If multiple exceptions can be thrown, how does the catch block know which exception to catch?

<details>

<summary> Click me to show the answer below!</summary>

Different catch blocks have different types. If the type of the exception throwned is of the type of the catch block, the catch block will be activated. 

</details>


Q4. How can an exception pass data back to the exception handler?

<details>

<summary> Click me to show the answer below!</summary>

Following the rules of stack unwinding. Please refer to the clarification section. 
</details>





