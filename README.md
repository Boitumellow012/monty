Monty Interpreter
The Monty Interpreter is a simple program written in C that reads Monty Bytecode files, interprets their instructions, and executes them.

Project Structure
The project directory is organized as follows:

css
Copy code
.
├── monty
├── monty.h
├── execute.c
├── main.c
├── operations
|  ├── op_push.c
|  ├── op_pall.c
|  ├── op_pint.c
|  ├── op_pop.c
|  ├── op_swap.c
|  ├── op_add.c
|  ├── op_sub.c
|  ├── op_div.c
|  ├── op_mul.c
|  ├── op_mod.c
|  ├── op_pchar.c
|  ├── op_pstr.c
|  └── op_nop.c
├── free_stack.c
└── bytecodes
    ├── 00.m
    ├── 01.m
    ├── ...
    └── 12.m
monty: Compiled executable file.
monty.h: Header file containing function prototypes, definitions, and struct declarations.
execute.c: Contains the execute_opcode() function that determines which opcode to execute.
main.c: Contains the main() function that reads the bytecode file and executes opcodes.
operations: Directory with files containing functions for each opcode (e.g., push(), pint(), pop(), etc.).
stack.c: Contains stack-related functions (e.g., stack_len(), push_stack(), pop_stack(), free_stack()).
bytecodes: Folder containing the Monty bytecode files to be executed.
Installation
To install and run the Monty Interpreter, follow these steps:

Clone the repository: git clone https://github.com/FourtyThree43/monty
Change into the monty directory: cd monty
Compile the interpreter: gcc -Wall -Werror -Wextra -pedantic *.c -o monty
Run the interpreter: ./monty <filename>.m
Replace <filename> with the name of the file containing the Monty code you want to execute.

Usage
The Monty Interpreter takes a single argument, which is the path to a Monty Bytecode file. The file should contain instructions for the interpreter to execute, with one instruction per line.

Supported Opcodes
The Monty Interpreter supports the following opcodes:

push: Pushes an integer onto the stack.
pop: Removes the top element of the stack.
swap: Swaps the top two elements of the stack.
add: Adds the top two elements of the stack.
sub: Subtracts the top element of the stack from the second top element.
div: Divides the second top element of the stack by the top element.
mul: Multiplies the second top element of the stack with the top element.
mod: Computes the modulus of the second top element of the stack with the top element.
pall: Prints all values on the stack.
pint: Prints the value at the top of the stack.
pchar: Prints the character at the top of the stack.
pstr: Prints the string starting at the top of the stack.
nop: Does nothing.
For more details on how to use the Monty Interpreter, refer to the project documentation.

This revised version maintains the content while reorganizing and formatting it for clarity and readability.
