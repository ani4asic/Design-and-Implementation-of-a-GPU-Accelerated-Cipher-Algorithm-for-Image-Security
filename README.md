# Design-and-Implementation-of-a-GPU-Accelerated-Cipher-Algorithm-for-Image-Security

> A hardware-accelerated image encryption framework implementing a lightweight Feistel-inspired one-round cipher for secure RGB image transmission. The project combines FPGA-based cryptographic processing, GPU-accelerated parallel execution, and ESP32 wireless communication to achieve secure, low-latency image transfer.

![FPGA](https://img.shields.io/badge/Platform-Xilinx%20Vivado-blue)
![GPU](https://img.shields.io/badge/GPU-CUDA-green)
![Communication](https://img.shields.io/badge/Wireless-ESP32-orange)

---

# Overview

Traditional encryption algorithms such as AES and DES provide strong security but often require multiple encryption rounds, increasing computational complexity and execution time. These characteristics make them less suitable for applications requiring low-latency image processing, such as surveillance, medical imaging, autonomous systems, and embedded multimedia devices.

This project proposes a **hardware-accelerated one-round cipher** that balances security and computational efficiency through a lightweight cryptographic architecture.

Unlike conventional software-only implementations, the proposed framework combines

- FPGA-based encryption
- GPU-accelerated parallel image processing
- ESP32 wireless communication

to build a complete secure image transmission system capable of real-time operation.

---

# Project Objectives

The primary objectives of this work were to

- Design a lightweight one-round image encryption algorithm
- Minimize computational complexity while maintaining security
- Accelerate encryption and decryption using GPU parallel processing
- Implement the encryption architecture in Verilog using Vivado
- Enable secure wireless image transfer using ESP32 modules
- Evaluate encryption quality using statistical security metrics

---

# System Architecture

```
                    RGB Image
                         │
                         ▼
              RGB Channel Separation
                         │
          ┌──────────────┼──────────────┐
          │              │              │
          ▼              ▼              ▼
         Red           Green          Blue
          │              │              │
          └──────────────┼──────────────┘
                         │
              One-Round Cipher Engine
          (Confusion + Diffusion + S-Box)
                         │
                         ▼
                 Encrypted RGB Image
                         │
              GPU Parallel Processing
                         │
                         ▼
              ESP32 Wireless Transfer
                         │
                         ▼
                Image Reception
                         │
                         ▼
                Decryption Engine
                         │
                         ▼
                Original RGB Image
```

---

# Key Features

- Lightweight Feistel-inspired One-Round Cipher
- FPGA implementation using Verilog HDL
- Confusion-Diffusion encryption architecture
- S-Box based nonlinear substitution
- GPU-accelerated encryption and decryption
- Parallel RGB channel processing
- ESP32 Wi-Fi based secure image transmission
- Low-latency image processing
- Hardware-oriented cryptographic design
- Statistical security validation

---

# Encryption Methodology

The proposed cipher operates on RGB image data by first separating each image into its Red, Green, and Blue channels.

Each channel undergoes two primary cryptographic stages:

### 1. Confusion

Pixel positions are rearranged to eliminate spatial correlation between neighboring pixels.

### 2. Diffusion

Pixel intensity values are modified using XOR-based transformations together with secret keys, initialization vectors, and nonlinear S-Box substitutions.

The cipher follows a lightweight Feistel-inspired architecture, allowing identical algorithmic structures for encryption and decryption while reducing hardware complexity.

---

# FPGA Implementation

The encryption engine was implemented using **Verilog HDL** and integrated in **Xilinx Vivado**.

The FPGA design includes:

- Input Memory Module
- RGB Split Module
- Parallel Encryption Cores
- RGB Combine Module
- Output Interface

Independent encryption cores simultaneously process the Red, Green, and Blue channels, enabling efficient hardware parallelism.

---

# GPU Acceleration

To improve execution speed, encryption and decryption were accelerated using GPU-based parallel computing.

The GPU implementation exploits pixel-level parallelism by assigning encryption operations to multiple CUDA threads, significantly reducing execution time for high-resolution images.

GPU acceleration enables

- Parallel encryption
- Parallel decryption
- Reduced latency
- Improved throughput

making the system suitable for real-time multimedia applications.

---

# Secure Wireless Transmission

Encrypted images are transmitted wirelessly using **ESP32 Wi-Fi modules**.

The ESP32 operates as

- Wireless Access Point
- Embedded Web Server
- Local File Storage Interface

The encrypted image is packetized, transmitted over Wi-Fi, reassembled at the receiver, and decrypted using the same secret key.

---

# Security Evaluation

The proposed encryption algorithm was evaluated using multiple security metrics.

### Entropy Analysis

Entropy measurements demonstrated high randomness in encrypted images, indicating strong resistance against statistical attacks.

### Avalanche Effect

Minor variations in plaintext produced significant changes in ciphertext, confirming effective diffusion characteristics.

### Functional Verification

The decrypted image matched the original input image, validating the correctness of the encryption and decryption process.

---

# Applications

- Secure Multimedia Communication
- Medical Image Transmission
- Surveillance Systems
- IoT Security
- Embedded Vision Systems
- Edge Computing
- FPGA-Based Cryptography
- Secure Wireless Image Transfer

---

# Technologies Used

### Languages

- Verilog HDL
- CUDA
- C/C++

### Hardware

- FPGA
- ESP32

### Development Tools

- Xilinx Vivado
- NVIDIA CUDA Toolkit

---

# Skills Demonstrated

- FPGA Design
- RTL Design
- Verilog HDL
- Hardware Acceleration
- CUDA Programming
- GPU Computing
- Parallel Processing
- Image Encryption
- Cryptography
- Embedded Systems
- ESP32
- Wireless Communication
- Computer Architecture
- Hardware-Software Co-Design

---

# Repository Contents

```
.
├── Project_Work_2_Final_Report.pdf
└── README.md
```

The repository currently contains the complete project report describing the system architecture, encryption methodology, FPGA implementation, GPU acceleration, ESP32 communication framework, implementation details, experimental results, and performance evaluation.

---

# Results

The proposed architecture successfully demonstrated

- Hardware implementation of a lightweight one-round cipher
- GPU-accelerated image encryption and decryption
- Secure wireless image transfer using ESP32
- Correct reconstruction of the original image after decryption
- High entropy and strong avalanche characteristics
- Low-latency image processing suitable for real-time applications

---

# Documentation

📄 **Project Report**

The complete implementation details, architectural diagrams, methodology, experimental setup, and evaluation results are available in:

**Project_Work_2_Final_Report.pdf**

---

# License

This repository is intended for educational and research purposes.
