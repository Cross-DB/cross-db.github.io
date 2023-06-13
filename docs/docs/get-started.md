---
template: overrides/blog.html
---

# Get Started

## Download
-------------------------------------------------------------------------------

Choose the OS and CPU, then [**Download**](https://crossdb.org/products/download/) here.

**Linux package file list**

 File             | Descritpion
 ----             | ----
crossdb.h         | The only header file
libcrossdb.so     | The only shared library
examples/         | CrossDB example code

**Windows package file list**

 File             | Descritpion
 ----             | ----
crossdb.h         | The only header file
crossdb.dll       | The only shared library
crossdb.lib       | For build with MSCV compiler
examples/         | CrossDB example code

**MacOS package file list**

 File             | Descritpion
 ----             | ----
crossdb.h         | The only header file
libcrossdb.dylib  | The only shared library for X64 and AMD64
examples/         | CrossDB example code

<!--
examples List
 File      | Descritpion
 ----      | ----
example.c  | Simple CrossDB example
tutorial.c | Complete CrossDB tutorial guide
schema.c   | CrossDB Schema Example
upgrade/   | `old.c` is old struct program, `new.c` is new struct program
-->

## Linux
-------------------------------------------------------------------------------

### Run Examples

```sh
cd examples

./build.sh example.c
./example.bin

./build.sh tutorial.c
./tutorial.bin

```

### Build in your project

- You can check examples/build.sh to build the library in your project folder.

- Yo can also install CrossDB globally and use it as common library.

	1\. Install `libcrossdb.so` to `/usr/lib`

	```c
	#include "crossdb.h"
	// your code
	```

	2\. Build this way: `gcc my.c -lcrossdb -pthread -ldl`


## Windows
-------------------------------------------------------------------------------

### Run Examples with MSVC

Start `Visual Studio` command line from menu `x64 Native Tools Command Prompt for VS 20xx`

Enter CrossDB package folder

```sh
cd examples

build example.c
example.exe

build tutorial.c
tutorial.exe

```

### Run Examples with MINGW64

```sh
cd examples

./build.sh example.c
./example.bin

./build.sh tutorial.c
./tutorial.bin

```

>**Note**
>You can run in `git bash` or `MSYS2 MINGW64`
>If you only have MINGW64, you an run in commandline
>
>`gcc -o example.exe -Wall -O2 example.c -I.. crossdb.dll`

### Build in your project

- For `MINGW64`, you can just use `crossdb.h` and `crossdb.dll` to compile.
- For `Visual Studio`, You can add `crossdb.h` `crossdb.lib` and `crossdb.dll` to your project.


## MacOS
-------------------------------------------------------------------------------

### Run Examples

```sh
cd examples

./build.sh example.c
./example.bin

./build.sh tutorial.c
./tutorial.bin

```

### Build in your project

- You can check examples/build.sh to build the library in your project folder.

- Yo can also install CrossDB globally and use it as common library.

	1\. Install `libcrossdb.dylib` to `/usr/local/lib`

	```c
	#include "crossdb.h"
	// your code
	```

	2\. Build this way: `clang my.c -lcrossdb`


<!--
=== "🛶 Windows MSVC Command Line"
	``` c linenums="1"
	start cl
	c1 example.c -llib
	```

=== "🛶 MacOS/FreeBSD clang"
	``` c linenums="1"
	clang example.c -llib
	```

=== "🛶 Linux gcc"
	``` c linenums="1"
	gcc example.c -llib
	```
-->
