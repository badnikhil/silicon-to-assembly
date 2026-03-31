# Introduction to CPU Internals and Architectural Basics

Before Starting To Learn Assembly Language , You need good understanding of CPU internals and some other concepts of CPU architecture.We'll Cover everything from scratch and in a meaningful Flow. Let's Start from the CPU itself, Because this is the place where everything starts and end.

## What is the CPU?

Central Processing Unit (CPU) -> The task of CPU is to execute Binary Instructions.For executing a Binary instruction , the CPU needs to identify what Instruction the Programmer wants it to Execute.Conceptually, an instruction consists of an opcode and operand(s). However, in actual machine code, instructions include additional encoding to specify registers, addressing modes, and data.

## Opcodes and Operand

*Opcodes and Operand* -> The binary representation of the operation part of an instruction is called the opcode (operation code). It tells the CPU what operation to perform like addition , subtraction etc(However Opcodes have more deeper breakdown for how CPU identifies an operation and it is explained in Extras - 1 ).

Operands specify the value or the location or both used in an operation.

Example: add 4 to RAX register

For example if we want the CPU to add 4 to the accumulate register(rax) in a x86 64 bit CISC CPU

**This is a simplified conceptual representation, not actual x86 encoding**

The instruction is '00000001 00000000 00000100' Here '00000001' is the Opcode which tells the CPU to perform addition in ALU. '00000000' represents the first operand, which tells the CPU to use the value stored in  RAX register and typically store the result there. 00000100 represents the second operand, which tells the CPU that the value 4 is to be used.

so combining the instruction

'00000001 00000000 00000100' -> perform addition in the ALU between the value  in the rax register and value 4.After that store the result in RAX register.

**please note that this is a very oversimplified breakdown of an instruction for a good understanding on how instructions are understood by CPU.**

in assembly we write it as

'add rax , 4' which is a far more better and understandable representation .

However, this question may arise how the CPU determines where to store the value after an Operation and it is deeply explained in Extras-2.Generally, the first  operand acts as the destination.
