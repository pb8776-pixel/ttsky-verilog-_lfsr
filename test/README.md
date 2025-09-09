# 8 Bit LFSR  

# 8-bit Linear Feedback Shift Register (LFSR)

## 📌 Overview
This project implements an **8-bit Linear Feedback Shift Register (LFSR)** in Verilog.  
An LFSR is a shift register where the input bit is a linear function (XOR) of selected previous bits (taps). It is widely used for:
- Pseudo-Random Number Generation (PRNG)
- Built-In Self Test (BIST) pattern generation
- Data scrambling in communication systems
- Spread-spectrum sequence generation

The design is written in Verilog, tested with a simple testbench, and can be simulated using **Icarus Verilog** and **GTKWave**.

---

## ⚙️ Features
- 8-bit LFSR with maximal-length sequence
- Uses a **primitive polynomial** for taps
- Deterministic and repeatable pseudo-random sequence
- Supports reset with non-zero seed
- Synthesis-friendly RTL code

---

## 🔑 Polynomial Used
The implemented 8-bit LFSR uses the primitive polynomial:

\[
P(x) = x^8 + x^6 + x^5 + x^4 + 1
\]

Which corresponds to taps at bits **[7, 5, 4, 3]** (0-based indexing).

This polynomial ensures a **maximum-length sequence** of \(2^8 - 1 = 255\) unique states before repeating.

