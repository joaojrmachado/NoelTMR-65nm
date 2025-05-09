# NoelTMR-65nm

> Fault-tolerant RISC-V Processor with AXI Interface for 65nm ASIC Tapeout

[![License](https://img.shields.io/github/license/joaojrmachado/NoelTMR-65nm)](LICENSE)
[![Build](https://img.shields.io/badge/build-passing-brightgreen.svg)]()
[![Contributors](https://img.shields.io/github/contributors/joaojrmachado/NoelTMR-65nm.svg)]()

---

## 📜 Overview

`NoelTMR-65nm` is a fault-tolerant RISC-V processor based on the NOEL5 core, enhanced with Triple Modular Redundancy (TMR) and Error Correction Codes (ECC) using Hamming Code. It includes an AXI-compliant memory interface and targets ASIC tapeout using TSMC 65nm technology.

The `NOEL-V` is a synthesizable VHDL model of a processor that implements the RISC-V architecture. The NOEL-V can be implemented as a dual-issue processor, allowing up to two instructions per cycle to be executed in parallel. Source: (NOEL-V)[]

### ✅ Key Features

- RISC-V RV32I processor (NOEL-V-based)
- Triple Modular Redundancy (TMR) for fault mitigation
- ECC (Hamming Code) applied to SRAM memory blocks
- AXI compliant interface for bus communication
- Fully synthesizable RTL
- Tapeout-ready for TSMC 65nm node



Projeto é um processador riscV Noel 5  com memoria tolerante a falhas com interface AXI
Chegar ate o tapeout 65 NM tsmc
Usar fluxo de trm automatizado para o processador
Inserir hamming code na memoria
Se der usar TMR no Axi
O problema aí vai ser a parte da memoria, mas vamos ter 4 meses pra resolver
A IHP tem tbm um pdk tolerante
Daria para tentar Fazer a sintese do Noel tbm no pdk da IHP e comparar dados de area, potencia, desempenho.


---

## 🔧 Project Structure

```bash
NoelTMR-65nm/
├── rtl/                # RTL modules (core, TMR, ECC, AXI)
├── tb/                 # Testbenches and verification logic
├── sim/                # Simulation scripts and waveforms
├── scripts/            # Helper scripts (lint, format, automation)
├── docs/               # Documentation, diagrams, architecture
├── syn/                # Synthesis files (e.g., Genus, Innovus)
├── .husky/             # Git hooks for commit linting
├── package.json        # Node project for commit tooling
├── commitlint.config.js
├── README.md
└── LICENSE
````

---

## 📦 Installation

> This project uses `Node.js` for commit validation and changelog automation.

```bash
git clone https://github.com/joaojrmachado/NoelTMR-65nm.git
cd NoelTMR-65nm
```

---

## 🚀 Getting Started

```bash
cd rtl/
make verilate          # or run synthesis with Vivado, Genus, etc.
```

> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque ac augue nec diam consequat bibendum.

---

## 📐 Tapeout Target

* **Technology:** TSMC 65nm GP
* **Standard Cells:** \[TBD]
* **Constraints:** Timing \[X ns], Area \[Y mm²], Power \[Z mW]
* **Toolchain:** Cadence Genus, Innovus, and/or Synopsys Design Compiler

---

## 📊 Reliability Strategy

| Component | Technique  | Description                        |
| --------: | ---------- | ---------------------------------- |
|       ALU | TMR        | Triple Modular Redundancy (Voting) |
|    Memory | ECC        | Hamming Code (SECDED)              |
|       AXI | (Optional) | TMR or Parity                      |

---

## 🧪 Testbench & Verification

* SystemVerilog assertions and functional coverage
* Randomized test scenarios
* Fault injection and fault masking metrics
* Simulation: Verilator, QuestaSim, or Xcelium

---

<!-- ## 📄 License -->

<!-- This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details. -->

<!-- --- -->

## 📚 References

* [RISC-V Foundation](https://riscv.org/)
* [NOEL-V by Cobham Gaisler](https://www.gaisler.com/index.php/products/processors/noel-v)
* [TSMC PDK Info (Generic)](#)

---

## 👨‍💻 Authors

João Machado – [@joaojrmachado](https://github.com/joaojrmachado)
Iuri Albandes – [@username](https://github.com/username)
Marina Dias – [@username](https://github.com/username)
Rafael Ferreira – [@username](https://github.com/username)
Fernanda Gusmão – [@username](https://github.com/username)


---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss the proposal.
