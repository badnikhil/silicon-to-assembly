# Silicon to Assembly: Documentation Roadmap & Unit Structures

> [!NOTE]
> The following unit structures and topics are subject to change as the documentation progresses.

This roadmap outlines the journey from **CPU internals** (the "Silicon") to low-level assembly programming. Each unit builds upon the previous one to provide a continuous, architecture-independent flow.

---

## Unit 1: Foundations of Computing (Current)
*Focus: The "Silicon" - how CPUs work at a hardware level.*

- **1.Foundation.md**: CPU internals and architectural basics.
- **2.architecture_basics.md**: Simplified explanation for architectural terms like x86, RISC, ISA
- **3.CPU_registers.md**: Discussion around registers and register sets for x86 and ARM.
- **4.Assembly_vs_assemblers.md**: The "Created" language fallacy and the mechanics of the assembler.
- **Extras-3.md**: The Natural Unit (Word) vs. The Addressable Unit (Byte).

---

## Unit 2: Memory, Data, and Addressing Models
*Focus: How the CPU interacts with data in memory.*

- **1.Memory_Hierarchy.md**: Registers vs. Cache vs. RAM - Speed and volatility.
- **2.Endianness_and_Alignment.md**: Big-Endian vs. Little-Endian and data alignment.
- **3.Addressing_Modes.md**: From immediate values to runtime address calculations.
- **4.Segmentation_and_Paging.md**: Conceptual look at memory protection.

---

## Unit 3: The Assembly Workflow & Core Instructions
*Focus: Converting ideas into machine-readable instructions.*

- **1.Assemblers_Linkers_Loaders.md**: The journey from `.asm` source to executable.
- **2.Data_Transfer_Instructions.md**: The `MOV` equivalent and its hardware constraints.
- **3.Arithmetic_and_Logic.md**: ALU operations (ADD, SUB, AND, OR, XOR, SHL/SHR).
- **4.Status_Flags.md**: The EFLAGS/RFLAGS register and processor state.

---

## Unit 4: Control Flow and the Stack
*Focus: Making decisions and managing function calls.*

- **1.Branching_and_Loops.md**: Conditional and Unconditional jumps.
- **2.The_Stack_Mechanism.md**: LIFO structure and the Stack Pointer (SP).
- **3.Subroutines_and_Calls.md**: Using `CALL` and `RET`.
- **4.Calling_Conventions.md**: How parameters travel between functions.

---

## Unit 5: System Interfacing & Performance
*Focus: Interacting with hardware and optimizing code.*

- **1.Interrupts_and_Syscalls.md**: Software vs. Hardware interrupts.
- **2.Input_and_Output.md**: Port-mapped I/O vs. Memory-mapped I/O.
- **3.Basic_Optimizations.md**: Simple tricks for faster execution.
- **4.Hardware_Features.md**: Pipelining and an intro to modern SIMD.

---

## Unit 6: Synthesis - From High-Level to Assembly
*Focus: Closing the gap between C/C++ and Assembly.*

- **1.C_to_Assembly_Patterns.md**: How common language constructs look in assembly.
- **2.Functional_Protocols.md**: Maintaining stack frames (Prologue and Epilogue).
- **3.Inline_Assembly_Basics.md**: Why and when to mix assembly with high-level languages.
- **4.Disassembly_Basics.md**: How to read and interpret machine code output.
