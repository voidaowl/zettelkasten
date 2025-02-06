# Meta
2025-02-04 21:24
**Tags:** [[C++]]
**Activity:** #learning 
**Status:** #completed 

# General run-time issues

#### Q: When executing a program, the console windows blinks and then closes immediately.
First, add or ensure the following lines are near the top of your program (in Visual Studio, ensure the lines appear after `#include "pch.h"` or `#include "stdafx.h"`, if those exist):

```C++ title:example.cpp
#include <iostream>
#include <limit>
```

Second, add the following code at the end of your `main()` function (right before the `return` statement):
```C++ title:example.cpp
std::cin.clear(); // reset any error flags
std::cin.ignore(std::numeric_limits<std::streamsize>::max(), '\n'); // ignore any characters in the input bugger until we find an enter character
std::cin.get(); // get one more char from the user
```

This will cause the program to wait for the user to press a key before continuing, which will give you time to examine your program’s output before your OS closes the console window.

The commonly suggested `ssytem("pause")` may only work on certain OSs and should be avoided.

#### Q: I ran my program and get a window but no output.
Your virus scanner or anti-malware may be blocking execution. Try disabling it temporarily and see if that’s the issue.

#### Q: My program compiles but it’s not working correctly. What do I do?
Debug it! See [This].
