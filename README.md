seq.asm
=======
### Minimal implementation of UNIX seq command in x86_64 assembly.
-----
A simple implementation of the UNIX seq command in 100% x86_64 assembly.
The seq command generates a sequence of numbers from the given parameters.
This implementation serves as a well-documented example project for those
learning assembly, much like the [calc.asm](https://github.com/flouthoc/calc.asm)
project.

Compiling
---------
As this project is written in Intel-syntax assembly, you'll need `nasm` to compile it.
After it's installed, you can compile the program by doing the following:
```
$ nasm -f elf64 -o seq.o seq.asm
$ ld -o seq seq.o
```

Usage
-----
This implementation accepts either one or two parameters for sequence generation:

```
./seq <start> <end>
```
or
```
./seq <end>
```
If only one argument is provided, start is assumed to be 1.

Examples
--------
Two arguments:
```
$ ./seq 10 15
10
11
12
13
14
15
```
One argument:
```
$ ./seq 5
1
2
3
4
5
```

Fork Me
-------
Feel free to fork the project and submit pull requests with features or fixes.
