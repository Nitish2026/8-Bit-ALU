# 8-bit Arithmetic Logic Unit (ALU) Design Using Circuit Verse

## Introduction
An **Arithmetic Logic Unit (ALU)** is the core component of a digital system responsible for performing arithmetic and logical operations.

This project presents the design and simulation of an 8-bit Arithmetic Logic Unit (ALU) using a hierarchical and modular approach. The ALU is constructed by combining two 4-bit ALUs, where each 4-bit ALU is further built using four 1-bit ALU units. Each 1-bit ALU is capable of performing multiple operations including ***Arithmetic operation***, as well as ***Logical operations*** along with bit ***Shift operations***. The use of this structured design approach simplifies scalability, improves flexibility, and reduces overall complexity. The complete system is implemented and verified using CircuitVerse to ensure correct functionality for all operations.

The design is implemented and simulated using CircuitVerse.

---

## Problem Statement
Design a scalable ALU capable of performing multiple arithmetic and logical operations efficiently using a modular approach.

Traditional ALU designs can become complex when scaling to higher bit widths. This project focuses on reducing complexity using hierarchical design.

---

## Objectives
- To design a 1-bit ALU capable of multiple operations  
- To construct a 4-bit ALU using 1-bit ALU blocks  
- To construct an 8-bit ALU using 4-bit ALU blocks  
- To implement both arithmetic and logical operations  
- To verify the design using simulation  

---

## Key Features
- Hierarchical design (1-bit → 4-bit → 8-bit)  
- Modular and scalable architecture  
- Supports multiple arithmetic and logic operations  
- Efficient use of combinational circuits  
- Easy to extend for higher bit-width systems  

---

## Operations Performed
Each 1-bit ALU is capable of performing the following operations:

1. Full Adder  
2. NAND Operation  
3. XNOR Operation  
4. NOT Operation  
5. NOR Operation  
6. Right Shift (Bit A)  
7. Right Shift (Bit B)  
8. Full Subtractor  

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

## 📊 Results and Analysis
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

