# Lesson 1: Hello world  

Learn how syscall work in this arch 

**helloworld.asm**
```.asm
SECTION .data 
msg     db   'Hello World', 0Ah

SECTION .text
global _start

_start: 

    mov edx, 13
    mov ecx, msg
    mov ebx, 1
    mov eax, 4
```
How to compile it:

```
$ nasm -f[format] elf helloworld.asm
$ ld -m elf_i386 helloworld.o -o helloworld
$ ./helloworld
Hello World
Segmentation fault!
```
