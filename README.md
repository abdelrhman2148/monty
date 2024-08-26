Monty Interpreter
Monty 0.98 is a scripting language that compiles into Monty byte codes, similar to Python. It operates using a unique stack and specific instructions to manipulate it. This project involves creating an interpreter for Monty ByteCodes files.

Monty Byte Code Files
Monty byte code files typically have the .m extension, though this is not a strict requirement. Each file contains instructions where each line has at most one instruction. Instructions can have any number of spaces before or after the opcode and its argument:

plaintext
Copy code
push 0
push 1
push 2
  push 3
                   pall
push 4
    push 5
      push 6
pall
Monty byte code files can also include blank lines and comments (text following an opcode or argument):

plaintext
Copy code
push 0    # Push 0 onto the stack
push 1    # Push 1 onto the stack

push 2
  push 3
                   pall

push 4

    push 5
      push 6

pall    # This is the end of our program. Monty is awesome!
Usage
To compile the interpreter, use:

sh
Copy code
gcc -Wall -Werror -Wextra -pedantic *.c -o monty
To run the interpreter:

sh
Copy code
./monty bytecode_file
Available Operation Codes
push <value>: Pushes an element onto the stack.
Example: push 1 (Pushes 1 onto the stack)
pall: Prints all values on the stack, starting from the top.
pint: Prints the value at the top of the stack.
pop: Removes the top element from the stack.
swap: Swaps the top two elements of the stack.
add: Adds the top two elements of the stack. The result is stored in the second node, and the first node is removed.
nop: Does nothing (No operation).
sub: Subtracts the top two elements of the stack from the second top element. The result is stored in the second node, and the first node is removed.
div: Divides the top two elements of the stack from the second top element. The result is stored in the second node, and the first node is removed.
mul: Multiplies the top two elements of the stack. The result is stored in the second node, and the first node is removed.
mod: Computes the remainder of the top two elements of the stack from the second top element. The result is stored in the second node, and the first node is removed.
#: Comment indicator. Anything following # on a line is treated as a comment.
pchar: Prints the integer at the top of the stack as its ASCII character representation.
pstr: Prints integers in the stack as ASCII characters. Stops when the value is 0, when the stack is empty, or when a non-ASCII value is encountered.
rotl: Rotates the top of the stack to the bottom.
rotr: Rotates the bottom of the stack to the top.
stack: Sets the format of the data structure to stack (LIFO).
queue: Sets the format of the data structure to queue (FIFO).

This For 0x19 Monty Project

Abdelrhman Fikri
