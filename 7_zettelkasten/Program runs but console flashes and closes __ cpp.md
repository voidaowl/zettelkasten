# Meta
2025-02-02 12:55
**Tags:** [[C++]]
**Activity:** #learning 
**Status:** #completed 

# If your program runs but the console window flashes and closes immediately

When the program has finished running, most modern IDEs will keep the console open so you can inspect the result. Older IDEs automatically close the console window after program execution.

If that happens, ensure the following lines are at the top of your program:
```C++ title:example.cpp
#include <iostream>
#include <limits>
```

Second, add the following code at the end of the `main()` function (just before the return statement):
```C++ title:example.cpp
std::cin.clear(); // reset any error flags
std::cin.ignor(std::numeri_limits<std::streamsize>::max(), '\n'); // ignore any characters in the input buffer until we find a newline
std::cin.get(); // get one more char from the user (waits for user to press enter)
```

This will cause your program to wait for the user to press `Enter` before continuing.

Other solutions, such as the `system("pause")` solution may only work on certain operating systems and should be avoided.

If the console window doesn’t open at all and your program doesn’t appear to be running, your anti-virus or anti-malware may also be blocking execution. If that’s the case, disable the scanners temporarily, or exclude the project directory from your scans.

> [!Tip] **Tip**
> If you’re using anti-virus and anti-malware, consider excluding your project directory from the scans, as compiling and debugging may cause false positives.



