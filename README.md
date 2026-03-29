# 8-bit Arithmetic Logic Unit (ALU) Design Using Circuit Verse
An Arithmetic Logic Unit (ALU) is the core component of a digital system or processor that performs arithmetic and logical operations on binary data. It can execute operations like addition, subtraction, AND, OR, and other logic functions. The ALU takes input operands and control signals to determine which operation to perform. It plays a crucial role in data processing and decision-making within a CPU.


---

## Contents
1. [Introduction](#Introduction)
2. [Problem Statement](#Problem-Statement)
3. [Objectives](#Objectives)
4. [Key Features](#Key-Features)
5. [Peripheral Circuits](#Peripheral-Circuits-of-1-Bit-ALU) <br>
     - [Full Adder](#i-Full-Adder)  
     - [Full Subtractor](#ii-Full-Subtractor)  
     - [NAND Gate](#iii-NAND-Gate)  
     - [XNOR Gate](#iV-XNOR-Gate)  
     - [NOT Gate](#V-NOT-Gate)  
     - [NOR Gate](#Vi-NOR-Gate)  
     - [Right Shift](#vii-Right-Shift)   
7. [Tools & Technologies](#Tools--Technologies)
8. [Methodology](#Methodology)
9. [Working Principle](#Working-Principle)
10. [Results and Analysis](#Results-and-Analysis)
11. [Future Scope](#Future-Scope)
12. [Conclusion](#Conclusion)

---

## Introduction
This project presents the design and simulation of an 8-bit Arithmetic Logic Unit (ALU) using a hierarchical and modular approach. The ALU is constructed by combining two 4-bit ALUs, where each 4-bit ALU is further built using four 1-bit ALU units. Each 1-bit ALU is capable of performing multiple operations including ***Arithmetic operation***, as well as ***Logical operations*** along with bit ***Shift operations***. The use of this structured design approach simplifies scalability, improves flexibility, and reduces overall complexity. The complete system is implemented and verified using CircuitVerse to ensure correct functionality for all operations.

The design is implemented and simulated using CircuitVerse.

---

## Problem Statement
In digital systems, Arithmetic Logic Units (ALUs) are essential for performing arithmetic and logical operations. However, traditional ALU designs become complex and difficult to scale when increasing the number of bits, leading to higher hardware complexity and reduced efficiency.

There is a need for a modular and scalable design approach that simplifies implementation while maintaining functionality. This project addresses the problem by designing an 8-bit ALU using a hierarchical structure of 1-bit and 4-bit ALU blocks, improving flexibility and ease of expansion.

---

## Objectives
The main objective of this project is to design and implement a scalable and efficient 8-bit Arithmetic Logic Unit (ALU) using a hierarchical approach. This includes developing a 1-bit ALU capable of performing multiple arithmetic and logical operations, and then constructing a 4-bit ALU and finally an 8-bit ALU using these basic units. The project also aims to ensure correct functionality of operations while maintaining modularity and ease of expansion. Additionally, the design is verified through simulation to analyze its performance and reliability.

---

## Key Features

- **Hierarchical Design**  
  The ALU is designed using a structured approach where an 8-bit ALU is built using two 4-bit ALUs, and each 4-bit ALU is constructed from four 1-bit ALUs, reducing complexity.

- **Modular Architecture**  
  Each unit (1-bit ALU) is independently designed and reused, making the overall system easy to design, debug, and extend.

- **Control Signal Based Operation**  
  Operations are selected using control inputs (S2, S1, S0), allowing flexible and efficient switching between different functions.

- **Efficient Carry Propagation**  
  Carry and borrow signals are properly propagated between stages, ensuring accurate arithmetic operations in multi-bit designs.

- **Scalability**  
  The design can be easily extended to higher bit-width ALUs (16-bit, 32-bit) by following the same modular structure.

- **Simulation Verified Design**  
  The entire ALU is tested using CircuitVerse to verify correct functionality for all operations and input combinations.

---

## Peripheral Circuits of 1-Bit ALU
Each 1-bit ALU has the following peripheral circuits:

### i. Full Adder  
  Performs binary addition of inputs A and B along with carry-in.  
  It produces sum and carry-out for arithmetic operations.

### ii. Full Subtractor  
  Performs subtraction between inputs A and B with borrow-in.  
  It generates difference and borrow-out signals.

<table align="center">
  <tr>
    <td align="center">
          <img width="1048" height="337" alt="image" src="https://github.com/user-attachments/assets/ff9c3aff-e8df-4e30-8e15-a3840c528452" /><br/>
      <small>Fig 1a. 1-Bit Full Adder</small>
    </td>
    <td align="center">
          <img width="1049" height="329" alt="image" src="https://github.com/user-attachments/assets/b0cefd26-87a6-4342-8276-f79ae2f389a1" /><br/>
      <small>Fig 1b. 1-Bit Full Subtractor</small>
    </td>
  </tr>
</table>

### iii. NAND Gate  
  Produces output as the negation of AND operation.  
  It is a universal gate used for implementing logic functions.

### iv. XNOR Gate  
  Outputs high when both inputs are equal.  
  Commonly used for comparison operations.

### v. NOT Gate  
  Inverts the input signal (0 becomes 1 and vice versa).  
  Used for bit-wise complement operations.

### vi. NOR Gate  
  Produces output as the negation of OR operation.  
  Useful in logic design and also acts as a universal gate.

### vii. Right Shift  
  Shifts the bits of input A towards the right by one position.  
  Used in operations like division and data manipulation.

<table align="center">
    <td align="center">
          <img width="387" height="358" alt="image" src="https://github.com/user-attachments/assets/7f3f6f6c-b9d8-4830-afe2-e56eb3062dfc" /><br/>
      <small>Fig 1c. Logical block </small>
    </td>
    <td align="center">
          <img width="1042" height="315" alt="image" src="https://github.com/user-attachments/assets/a08c3a6a-44a0-495e-977b-3727dc666c3e" /><br/>
      <small>Fig 1d. Right Shift Register </small>
    </td>
</table>

These operations are selected using control/select lines.

---

## Tools & Technologies
- CircuitVerse (Simulation)  
- Digital Logic Design  
- Components Used:  
  - Logic Gates (AND, OR, NOT, NAND, NOR, XOR, XNOR)  
  - Full Adder / Full Subtractor  
  - Multiplexer  

---

## Methodology
The ALU is designed using a bottom-up approach:

1. **Design of 1-bit ALU**
   - Implement all 8 operations
   - Use multiplexer for operation selection  

2. **Design of 4-bit ALU**
   - Combine four 1-bit ALUs  
   - Provide common control signals  

3. **Design of 8-bit ALU**
   - Combine two 4-bit ALUs  
   - Ensure proper carry propagation  

4. **Simulation**
   - Test for all input combinations  
   - Verify correctness of outputs  

---

## Working Principle
- Inputs: Two 8-bit operands (A and B)  
- Control signals select the operation  
- Each 1-bit ALU processes corresponding bits  
- Outputs are combined to form final 8-bit result  

For arithmetic operations:
- Carry is propagated between stages  

For logical operations:
- Each bit is processed independently  

---

## Results and Analysis
- The ALU correctly performs all 8 operations  
- Modular design simplifies debugging and scalability  
- Carry propagation works correctly in multi-bit operations  
- Logical operations show independent bit-level execution  

---

## Future Scope
- Extend to 16-bit / 32-bit ALU  
- Add multiplication and division operations  
- Implement using Verilog/SystemVerilog  
- FPGA-based hardware implementation  
- Optimize delay and power consumption  

---

## Conclusion
The project successfully demonstrates a scalable and modular ALU design using a hierarchical approach. By constructing higher-bit ALUs from smaller units, complexity is reduced and flexibility is increased.

This design forms a strong foundation for processor-level implementations.

---

## 🔗 Project Simulation
👉 **[Click here](https://circuitverse.org/simulator/embed/alu-a876b67e-f7d1-406c-b691-8cb2c7e5fe75)**

