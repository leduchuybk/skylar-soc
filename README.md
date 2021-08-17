1. Abstract

  Nowadays, the demand for high energy efficiency in Internet-of-thing (IOT) devices is increasing. Meanwhile, RISC-V is gaining its fame as a trusty ISA in both academy and industrial field sectors. Therefore, this project aims to explore the possibility of implementing RISC-V core in IOT applications. To support core in calculation, there are some hardware accelerators modules implemented inside system.

2. Features
Open-source RISC-V core CV32E40P from Open HWGroup
  32-bit 4-stage pipeline in-order RISC-V core
  Supported ISA:
    RV32IM[F]C
    Xpulp custom extensions to achieve higher code density, performance, and energy efficiency
  SOC architecture based on pulpissimo architecture includes
    APB bus
    Autonomous Input/Output subsystem (uDMA)
    Interrupt controller (Event unit)
    Hardware accelerators modules (HWPEs)
    I/O interfaces: SPI, UART, JTAG
    Energy saving module (FLL using opencores)
    64KB SRAM
    8kB ROM
  Optional features: Encrypted ROM bootloader using Advanced Encryption Standard 128 bit (AES128)
                     and physical unclonable function (PUF).
  Frequency range: 10MHz-100MHz
  Power density: 15µW/MHz

3. Contributors:
  Thanh-Dat Nguyen : RTL code, simulation, implementation, layout.
  Duc-Huy Le: RTL code, system integration, layout.
  Duy-Hieu Bui: advisor.