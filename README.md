# Stratum_x64
mini-OS/Kernel, scheduler multithread, abstraction hardware, minimal impact (and french, cocorico)


---

# Stratum OS

**Stratum** is a minimal, ultra-optimized operating system designed from the ground up to maximize performance and efficiency. It runs entirely on bare metal, providing direct control over hardware resources with minimal abstraction.

At its core, **CoreLang** is a multi-language interpreter that executes scripts natively, entirely within Stratum, leveraging native assembly-level operations for maximum speed.

---

## Features

### Stratum (OS)

* Bootloader and microkernel written in **x86/x64 assembly**.
* **Multithreading scheduler** implemented at the hardware level.
* Minimal hardware abstraction: memory management, screen, keyboard.
* Efficient context switching and preemption using CPU timers.
* Extremely lightweight: no unnecessary services or drivers.
* Designed for **maximal CPU, memory, and thread efficiency**.

### CoreLang (Interpreter)

* Multi-language interpreter running directly on Stratum.
* Initial support for:

  * Python-like minimal language
  * BASIC-like minimal language
  * C-like pseudo language
* Each interpreter executes **native bytecode**, fully optimized.
* Garbage collection and memory management tailored to Stratum.
* Threaded execution for concurrent scripts.

---

## Architecture Overview

```

┌───────────────────────────┐
│        Bootloader          │
└─────────────┬─────────────┘
              │
              ▼
┌───────────────────────────┐
│        Stratum Kernel      │
│ - CPU init & memory       │
│ - Multithread scheduler   │
│ - Minimal I/O drivers     │
└─────────────┬─────────────┘
              │
              ▼
┌───────────────────────────┐
│     CoreLang Interpreter   │
│ - Python-like              │
│ - BASIC-like               │
│ - C-like                   │
│ - Bytecode execution       │
└─────────────┬─────────────┘
              │
              ▼
┌───────────────────────────┐
│       Applications / Scripts │
└───────────────────────────┘

```

---

## Roadmap

**Phase 1 – Core OS & Interpreter**

* Bootloader and kernel initialization.
* Hardware detection and memory management.
* CoreLang multi-language interpreter with native bytecode.
* Multithread scheduler.

**Phase 2 – Extended Hardware Support**

* Network driver implementation.
* GPU / graphics acceleration drivers.
* Storage drivers (optional).

**Phase 3 – Optimization & Features**

* Performance benchmarking and tuning.
* Additional language support.
* Multi-core scaling and advanced scheduling.
* Garbage collection improvements.

---

## Goals

* Maximal **performance and minimal overhead**.
* Full control of **hardware resources** without relying on a traditional OS.
* Provide a platform to **run interpreted languages natively** with near-metal speed.
* Serve as a foundation for exploring **bare-metal language runtimes**.

---

## Getting Started

1. Clone this repository.
2. Assemble the bootloader and kernel using `nasm`.
3. Package the system into an ISO for testing in **QEMU** or on a USB using **Rufus**.
4. Run CoreLang scripts directly on Stratum.

---

## License

personnal project, but open-source soon

---



Do you want me to do that next?
