# C++

## Windows

### GCC

1. Download the latest version of [MinGW](https://github.com/niXman/mingw-builds-binaries) by clicking on `MinGW-W64 online installer`
2. Run the setup and select:

  | Option                            | Selection |
  |-----------------------------------|-----------|
  | Select a version                  | latest    |
  | Select an architecture            | 64 bit    |
  | Select a thread model             | posix     |
  | Select a build revision           | rev2      |
  | Select a C runtime                | ucrt      |
  | Select directory for installation | C:/       |

3. This will create a directory in `C:\mingw64`. Now add the path `C:\mingw64\bin` to the system environment variable `Path`.
4. (Re)open a powershell and test the installation with `g++ --version`

<div class="warning">
  N.B. the thread model posix is needed in order to compiler OpenCV
</div>