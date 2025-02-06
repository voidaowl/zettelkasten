# Meta
2025-02-01 23:12
**Tags:** [[C++]]
**Activity:** #learning 
**Status:** #completed 

# Step 1: Define the problem

Examples:
- “I want to write a program that will allow me to enter many numbers, then calculate the average.”
- “I want to write a program that generates a 2d maze and lets the user navigate through it.”
- “I want to write a program that reads in a file of stock prices and predicts whether the stock will go up or down.”

# Step 2: Determine the “how”

Typically, good solutions have the following characteristics:
- They are straightforward.
- They are well documented.
- They are built modularly.
- They can recover gracefully or give useful error messages when something unexpected happens.

A **bug** is any kind of programming error that prevents the program from operating correctly. The activity of removing bugs is called **debugging**.

# Step 3: Write the program

The set of C++ instructions that we put into the text editor is called the **source code**. It’s advised to used a **text editor** or an **integrated development environment**.

> [!info] ✅ **Best practice**
> Name the first/primary source code file of each program `main.cpp`.

# Step 4: Compile the source code

The C++ compiler performs two tasks:
1. Check the code to make sure it follows the rules of C++. If not, it throws errors. Compilation is aborted until errors are fixed.
2. Translates the code into machine language instructions, stored into an **object file**.

# Step 5: Link object files and libraries

A **linker** kicks in after the compiler successfully finishes. It’s job is to combine of the object files and produce the desired output file (e.g. `.exe`). The process is called **linking**.

Tasks:
1. Check validity of object files.
2. Ensure all cross-file dependencies are resolved properly.
3. Link library files.

A **library file** is a collection of precompiled code that has been “packaged up” for reuse in other programs (e.g. the C++ Standard Library).

> [!info] **Building**
> The term *building* is often used to refer to the full process of converting source code files into an executable that can be run. A specific executable produced as the result of building is called a **build**.
> The process can be automated with tools like `make` or `build2`.

# Step 6: Testing and Debugging

**Testing** is the process of assessing whether your software is working as expected. Basic testing typically involves trying different input combinations to ensure the software behaves correctly in different cases.

**Debugging** is the process of finding and fixing programming errors.