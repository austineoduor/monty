
0x19. C - Stacks, Queues - LIFO, FIFO

 General

. What do LIFO and FIFO mean

. What is a stack, and when to use it

. What is a queue, and when to use it

. What are the common implementations of stacks and queues

. What are the most common use cases of stacks and queues

. What is the proper way to use global variables

 Installation

. Clone the repository https://github.com/austineoduor/monty.git

. Compile the program gcc gcc -Wall -Werror -Wextra -pedantic -std=c90 *.c -o monty

. Run the program as follows:

. Usage: monty <file.m>

. Ex: ./monty ./bytecodes/00.m

The Monty language

Monty 0.98 is a scripting language that is first compiled into Monty byte codes (Just like Python). It relies on a unique stack, with specific instructions to manipulate it. The goal of this project is to create an interpreter for Monty ByteCodes files.

Monty byte code files

Files containing Monty byte codes usually have the .m extension. Most of the industry uses this standard but it is not required by the specification of the language. There is not more than one instruction per line. There can be any number of spaces before or after the opcode and its argument:

Example

julien@ubuntu:~/monty$ cat -e bytecodes/000.m

push 0$

push 1$

push 2$

push 3$
                   pall    $
push 4$

     push 5    $

        push    6        $
pall$

julien@ubuntu:~/monty$


Example 2

julien@ubuntu:~/monty$ cat -e bytecodes/001.m

push 0 Push 0 onto the stack$

push 1 Push 1 onto the stack$

$

push 2$

    push 3$
                   pall    $
$

$
                           $
push 4$
$

    push 5    $

        push    6        $
$

pall This is the end of our program. Monty is awesome!$

julien@ubuntu:~/monty$


Other files

. monty.h - Header file; Contains function, struct and global variable declarations

. bytecodes - A directory containing test files used while making this program

 Author

austine oduor
Jeff Ochieng


