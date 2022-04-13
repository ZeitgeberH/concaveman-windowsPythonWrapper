Forked from [ sadaszewski'concaveman-cpp ](https://github.com/sadaszewski/concaveman-cpp)

## updates
The original python wrapper was created for Linux and doesn't work under Windows 10.


## how to make Win10 dll
First, download and install [llvm-clang 14.0.0](https://releases.llvm.org/download.html)

Then open a powershell terminal, type:

```console
clang++ -c -std=c++14 -stdlib++-isystem "C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\VC\Tools\MSVC\14.16.27023\include" concaveman.cpp -o concaveman.o

clang++ -shared -v -o concaveman.dll concaveman.o   
```
Four new files will be generated. Use the dll with the python wrapper. See jupyter notebook demo in notebook folder
