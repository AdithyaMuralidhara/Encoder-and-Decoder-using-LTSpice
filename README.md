
# 3:8 Encoder and 8:3 Decoder Design using LTSpice

### Overview

This project demonstrates the design and simulation of a **3:8 Encoder** and **8:3 Decoder** (priority encoder) using **LTSpice**. The purpose is to understand how digital encoding and decoding circuits work using basic logic gates like AND, OR, and NOT.

### Tools Used

* **LTSpice**: Circuit simulation tool by Analog Devices
* **Logic Gates**: AND, OR, NOT (from the LTSpice digital library)
* **Pulse Voltage Sources**: Used as input signals for simulation

### 3:8 Encoder

A 3:8 encoder takes 8 input lines and converts the active input into a 3-bit binary output. It is used to reduce the number of data lines and simplify communication in digital systems. In this design:

* Only one input is HIGH at any time.
* Output changes based on which input is active.

![image](https://github.com/user-attachments/assets/87b148cd-920e-440b-bbb2-31a2b9991ef4)

![image](https://github.com/user-attachments/assets/a10a9bdf-cde5-4216-b5fa-59a4085735b3)

### 8:3 Decoder

When this decoder is enabled, it's one of the eight outputs will be active for each combination of inputs. The operation of this 3-line to 8-line decoder can be analyzed with the help of its function table which is given below.

![image](https://github.com/user-attachments/assets/72e8d89e-7cd4-4cf7-acd4-622af8bc4d40)

![image](https://github.com/user-attachments/assets/c8ba10d7-1abb-44e2-ad8e-7521f59e0461)

### Simulation Features

* Inputs are provided using pulse voltage sources.
* Outputs are verified using waveform analysis in LTSpice.
* Logic gates are connected as per truth tables.
* Design tested under different input combinations.

### Outcome

The simulation helped understand how encoding compresses multiple signals into a smaller binary output, and how decoding (priority encoding) selects the most important input from many. LTSpice was useful in visualizing real-time logic transitions and testing digital logic behavior without physical hardware.
