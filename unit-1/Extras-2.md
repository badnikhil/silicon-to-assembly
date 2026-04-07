## Extras – 2: How CPU Determines Where to Store the Result

When an operation is performed, a natural question arises:
> “Where does the result go?”

This is not decided randomly. It depends on the **instruction format and operand specification**.

---

### 1. Basic Idea

An instruction does not only tell the CPU *what to do*, but also:
- **Where to get data from**
- **Where to store the result**

This information is provided through **operands**.

---

### 2. Common Rule (General Case)

In many instruction formats:

> The **first operand acts as the destination**

Example:
```

ADD R1, R2

```

Meaning:
- Take value from R1  
- Add value from R2  
- Store result back in **R1**

So:
```

R1 = R1 + R2

```

---

### 3. Types of Instruction Formats

Different CPUs use different formats to decide destination:

---

#### a) Two-Operand Format

```

ADD A, B

```

- A -> destination (also used as source)  
- B -> source  

Result:
```

A = A + B

```

This is common in many architectures.

---

#### b) Three-Operand Format

```

ADD R1, R2, R3

```

- R1 -> destination  
- R2, R3 -> sources  

Result:
```

R1 = R2 + R3

```

This is clearer and avoids overwriting source values.

---

#### c) One-Operand (Accumulator-Based)

```

ADD X

```

- Uses a special register called **Accumulator (AC)**  

Result:
```

AC = AC + X

```

Here:
- Destination is fixed (Accumulator)

---

#### d) Zero-Operand (Stack-Based)

```

ADD

```

- Operates on top elements of a stack  

Process:
1. Pop two values  
2. Add them  
3. Push result back  

No explicit destination is written — it is implied by the stack.

---

### 4. How CPU Knows the Destination

The CPU determines destination using:

- Instruction format (how many operands)
- Position of operands in instruction
- Addressing mode bits
- Sometimes fixed rules (like accumulator or stack)

The **Control Unit decodes this information** and routes the result accordingly.

---

### 5. Role of Registers and Memory

The result can be stored in:

- CPU registers (fastest, most common)
- Memory locations
- Special registers (like accumulator)

Example:
```

ADD R1, [1000]

```

- R1 -> destination  
- Memory address 1000 -> source  

---

### 6. Why First Operand is Often Destination

Using the first operand as destination:
- Simplifies instruction design  
- Reduces number of bits needed  
- Makes decoding easier  

But this is just a convention, not a rule for all CPUs.

---

### 7. Key Takeaway

The destination of a result is not guessed — it is explicitly or implicitly defined by the instruction format.

- Two-operand -> first operand is usually destination  
- Three-operand -> separate destination field  
- Accumulator -> fixed destination  
- Stack -> implicit destination  
