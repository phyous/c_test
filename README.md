# c_test
Demo of creating, compiling and calling into c\c++ functions from python 3

## Installation
1. To compile: `python3 setup.py install`. This will compile and copy the .so library to the appropriate locaiton:
```
c_test python3 setup.py install
running install
running build
running build_ext
running install_lib
running install_egg_info
Writing /usr/local/lib/python3.9/site-packages/hello-0.1.0-py3.9.egg-info
```

2. For dynamic linked libraries to be loaded, the paths searched must be in `LD_LIBRARY_PATH`. Ensure this is defined; ex: `export LD_LIBRARY_PATH=/usr/local/lib/python3.9/site-packages`

## Use
In `main.cpp` we defined function `hello_world`. Assuming the .so file generated is in the right place, you can now call:
```
➜  c_test python3
Python 3.9.0 (default, Nov 21 2020, 14:55:42)
[Clang 12.0.0 (clang-1200.0.32.27)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> import hello
>>> hello.hello_world()
Hello, world!
```
