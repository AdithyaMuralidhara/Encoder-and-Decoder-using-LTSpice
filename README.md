
# 8:3 Encoder and 3:8 Decoder Design using LTSpice

### Overview

This project demonstrates the design and simulation of a **8:3 Encoder** and **3:8 Decoder**  using **LTSpice**. The purpose is to understand how digital encoding and decoding circuits work using basic logic gates like AND, OR, and NOT.

### Tools Used

* **LTSpice**: Circuit simulation tool by Analog Devices
* **Logic Gates**: AND, OR, NOT
* **Pulse Voltage Sources**: Used as input signals for simulation

### 8:3 Encoder

An 8:3 encoder is a combinational circuit that takes 8 input lines (0–7) and produces a 3-bit binary output (A0,A1,A2).
It assumes only one input is HIGH at a time.
This circuit compresses multiple input lines into fewer output bits. Commonly used in applications like keypads, and signal compression.

  ## 8:3 Encoder Truth Table

| 7 | 6 | 5 | 4 | 3 | 2 | 1 | 0 | A2 | A1 | A0 |
|----|----|----|----|----|----|----|----|----|----|----|
| 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 0  | 0  |
| 0  | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 0  | 0  | 1  |
| 0  | 0  | 0  | 0  | 0  | 1  | 0  | 0  | 0  | 1  | 0  |
| 0  | 0  | 0  | 0  | 1  | 0  | 0  | 0  | 0  | 1  | 1  |
| 0  | 0  | 0  | 1  | 0  | 0  | 0  | 0  | 1  | 0  | 0  |
| 0  | 0  | 1  | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 1  |
| 0  | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 1  | 0  |
| 1  | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 1  | 1  |

  ## LTSpice Circuit
![image](https://github.com/user-attachments/assets/72e8d89e-7cd4-4cf7-acd4-622af8bc4d40)

  ## Output Waveform
![image](https://github.com/user-attachments/assets/c8ba10d7-1abb-44e2-ad8e-7521f59e0461)

### 3:8 Decoder

A 3:8 decoder is a combinational circuit that takes a 3-bit input (A, B, C) and activates one of 8 outputs (Z0–Z7) based on the binary value of the input. Exactly one output is HIGH at any time.
It performs the reverse operation of an encoder. Used in I/O selection, and control logic.

| A | B | C | Z0 | Z1 | Z2 | Z3 | Z4 | Z5 | Z6 | Z7 |
|---|---|---|----|----|----|----|----|----|----|----|
| 0 | 0 | 0 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |  1 |
| 0 | 0 | 1 |  0 |  0 |  0 |  0 |  0 |  0 |  1 |  0 |
| 0 | 1 | 0 |  0 |  0 |  0 |  0 |  0 |  1 |  0 |  0 |
| 0 | 1 | 1 |  0 |  0 |  0 |  0 |  1 |  0 |  0 |  0 |
| 1 | 0 | 0 |  0 |  0 |  0 |  1 |  0 |  0 |  0 |  0 |
| 1 | 0 | 1 |  0 |  0 |  1 |  0 |  0 |  0 |  0 |  0 |
| 1 | 1 | 0 |  0 |  1 |  0 |  0 |  0 |  0 |  0 |  0 |
| 1 | 1 | 1 |  1 |  0 |  0 |  0 |  0 |  0 |  0 |  0 |

  ## LTSpice Circuit
![image](https://github.com/user-attachments/assets/87b148cd-920e-440b-bbb2-31a2b9991ef4)

  ## Output Waveform
![image](https://github.com/user-attachments/assets/a10a9bdf-cde5-4216-b5fa-59a4085735b3)

### Simulation Features

* Inputs are provided using pulse voltage sources.
* Outputs are verified using waveform analysis in LTSpice.
* Logic gates are connected as per truth tables.
* Design tested under different input combinations.

### Outcome

The simulation helped understand how encoding compresses multiple signals into a smaller binary output, and how decoding (priority encoding) selects the most important input from many. LTSpice was useful in visualizing real-time logic transitions and testing digital logic behavior without physical hardware.
