# OpenCV

## Windows

### MinGW

Here are the detailed instruction on how to compile OpenCV on Windows for MinGW 64-bit.

1. Install [C++](cpp.md)
2. Install CMake:
    1. Download the latest release version of `Windows x64 Installer` of [CMake](https://cmake.org/download/)
    2. Install CMake selecting:
        - [x] Add CMake to PATH environment variable
    3. (Re)open a powershell and test the installation with:
        -  `cmake --version`
4. Get OpenCV:
5. Compile OpenCV:
    1. Download the last release source code of [OpenCV](https://github.com/opencv/opencv))
    2. Run the executable and extract to `C:\`
    3. Create a folder `mingw<version>` at path: `C:\opencv\opencv<version>\build\x64` *(the last OpenCV version currently is 4.11, while the last MinGW version currently is 14.20, so it will be: `C:\opencv\opencv411\build\x64\mingw1420`)*
    4. Open CMake and set it up:
        1. Set "Where is the source code" to `C:\opencv\opencv<version>\sources` (i.e. the file containing CMakeLists.txt)
        2. Set "Where to build the binaries" to the mingw folder:  
        `C:\opencv\opencv<version>\build\x64\mingw<version>`
        3. Click on "Configure"
        4. Click on "Specify native compilers"
        5. For C add: `C:/mingw64/bin/gcc.exe` and for C++ add: `C:/mingw64/bin/c++.exe` (if MinGW hasn't been installed following the [C++](cpp.md), use the equivalent paths)
        6. Click on "Finish"
        7. Click "Generate"
    5. Open a powershell and cd to the build path:  
    `cd C:\opencv\opencv<version>\build\x64\mingw<version>`
    6. Run the command: `mingw32-make` and pray the Gods...
    7. Run the command: `mingw32-make install`

If everything has been successful, you will have the following paths:
- **inc:** `C:\opencv\opencv<version>\build\x64\mingw<version>\install\include`
- **bin:** `C:\opencv\opencv<version>\build\x64\mingw<version>\install\x64\mingw\bin`
- **lib:** `C:\opencv\opencv<version>\build\x64\mingw<version>\install\x64\mingw\lib`
