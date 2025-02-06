# Meta
2025-02-02 12:35
**Tags:** [[C++]]
**Activity:** #learning 
**Status:** #completed 

# Visual Studio Solution Explorer

In *Solution Explorer* > *Source Files* > *HelloWorld.cpp*

In the text editor, Visual Studio has already opened *HelloWorld.cpp*. Select and delete all of the code, then type the following:
```C++ title:HelloWorld.cpp
#include <iostream>

int main()
{
	std::cout << "Hello, world!";
	return 0;
}
```

`F7` or `Ctrl + Shift + B` to compile (or Build* > *Build Solution*).

Successful compile output:
```Shell title:output.sh
Build started at 12:43 PM...
1>------ Build started: Project: HelloWorld, Configuration: Debug x64 ------
1>HelloWorld.cpp
1>HelloWorld.vcxproj -> D:\repos\voidaowl\hello_world_cpp\HelloWorld\x64\Debug\HelloWorld.exe
========== Build: 1 succeeded, 0 failed, 0 up-to-date, 0 skipped ==========
========== Build completed at 12:43 PM and took 03.986 seconds ==========
```

`Ctrl + F5` to run (or *Debug* > *Start without debugging*).

> [!Note]
> When running your program directly from Visual Studio Code, you may see an additional line of output that looks something like this:
> `D:\repos\voidaowl\hello_world_cpp\HelloWorld\x64\Debug\HelloWorld.exe (process 14436) exited with code 0 (0x0).`
> 
> This is normal. VS is providing additional info about whether your program exited normally or not.

