# Meta
2025-02-01 19:06
**Tags:** [[C++]]
**Activity:** #learning 
**Status:** #completed 

# High-level Languages

A **compiler** is a program that reads the source code of one language and translates it into another (usually a low-level) language. A C++ compiler translates C++ code into machine code.

> [!info] **Optional reading**
> Most C++ compilers can also be configured to generate assembly code. This is useful when a programmer wants to see specific instructions the compiler is generating for a section of the program.

The machine code output by the compiler can be packaged into an executable file. Running executable files **does not** require the compiler to be installed.

An **interpreter** is a program that directly executes instructions in the source code without requiring them to be compiled first.

Interpreters tend to be more flexible than compilers, but are less efficient when running programs because the interpreting process needs to be done every time the program is run.

> [!info] **Optional reading**
> A good comparison of the advantages of compilers vs interpreters can be found [here](https://stackoverflow.com/questions/38491212/difference-between-compiled-and-interpreted-languages/38491646#38491646). Also check [[Compilers vs interpreters|this note]]
> 
> Another advantage of compiled programs is that distributing a compiled program doesn’t require distributing the source code. In a non-open-source environment, this is important for intellectual property (IP) protection purposes.

## Benefits
High-level languages are named so because they provide a high level of abstraction from the underlying architecture.

They allow programmers to write software without knowing much about the platform it will be run on, thus being able to create **cross-platform** applications.

Programs written in high-level languages are easier to read, write, and learn, because they resemble natural languages and common-use mathematics.

High-level languages typically include additional capabilities that make it easier to perform common programming tasks.