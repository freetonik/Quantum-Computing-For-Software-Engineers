# Quantum Computing For Software Engineers

[![Unitary Foundation](https://img.shields.io/badge/Supported%20By-UNITARY%20FOUNDATION-brightgreen.svg?style=for-the-badge)](https://unitary.foundation)
<img src="https://mirrors.creativecommons.org/presskit/buttons/88x31/png/by-sa.png" style='height:28px; width:auto;'>

![](./images/cover.jpg)

How to start a career in the quantum computing industry as a software engineer. This book is work in progress, projected completion date is November 2025. Draft outline:

## Groundwork

1. Quantum Physics 101
2. What quantum computing is and isn't
3. Myths and hype
4. Types (modalities) of QCs

## Levels of Abstraction of a Superconducting Quantum Computer

1. Crafting a qubit with superconductivity
1. Calibration
1. High level: quantum algorithms
1. Quantum circuits and classical computing
1. Pulse-level
1. Control instruments
1. QPU

## Full vertical stack

1. SDKs and formats (Qiskit, Cirq, CUDA, QASM, QIR, etc.)
2. "Backends"
3. Transpilation
4. Routing
5. Optimization
6. Circuit-to-pulse compilation
7. Native instrument instructions
8. Readout

## Current Challenges

1. Simulating and running on real hardware
2. Error rates
3. Scalability
4. Noise and decoherence
5. NISQ vs QEC

## Software evolution

1. Why Python
2. Why no Python
3. Role of Rust
4. Role of LLVM, IR and MLIR

---

Building:

```
pandoc book.md -o book.pdf --from markdown --template eisvogel --listings
```