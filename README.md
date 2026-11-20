# EVENTIDE OS

### Precision at the Edge of the Unknown.

**EVENTIDE OS** is an experimental operating system built from scratch to explore low-level programming, computer architecture, kernel development, and operating system fundamentals.

The project aims to develop a simple, bootable 32-bit operating system with a basic command-line interface as its first milestone: **EVENTIDE OS v1.0**.

> Built from the ground up. Designed to understand what happens beneath the software we use every day.

---

## Project Vision

Most developers work with operating systems without understanding the layers that make them function.

EVENTIDE OS is an attempt to explore those layers by building an operating system step by step.

The project focuses on:

- Understanding computer architecture and boot processes.
- Developing a custom kernel using C and Assembly.
- Working directly with hardware-level concepts.
- Implementing basic memory and interrupt management.
- Building a simple command-line shell.
- Creating a bootable operating system that can run in an emulator.

## Initial Release — v1.0

The first release will focus on a minimal but functional bootable operating system.

### Planned Features

- [ ] Bootable 32-bit x86 kernel.
- [ ] GRUB bootloader integration.
- [ ] Basic kernel initialization.
- [ ] Screen output.
- [ ] Keyboard input.
- [ ] Interrupt handling.
- [ ] Basic command-line shell.
- [ ] Built-in shell commands.
- [ ] Bootable ISO image.
- [ ] QEMU testing.

Advanced features such as multitasking, networking, a complete filesystem, and a graphical interface are planned for future releases.

---

## Technology Stack

| Component | Technology |
|---|---|
| Kernel Development | C |
| Low-level Programming | x86 Assembly |
| Architecture | 32-bit x86 |
| Bootloader | GRUB |
| Boot Protocol | Multiboot |
| Assembler | NASM |
| Cross Compiler | i686-elf GCC |
| Binary Utilities | GNU Binutils |
| Build System | GNU Make |
| Emulator | QEMU |
| Development Environment | Ubuntu Linux |
| Virtualization | Oracle VirtualBox |
| Version Control | Git & GitHub |

### Why a Cross-Compiler?

A normal GCC compiler targets the operating system on which it runs.

EVENTIDE OS requires a compiler that generates code for our own bare-metal target rather than depending on the host Linux environment.

We are therefore building a dedicated `i686-elf` cross-compiler using GNU Binutils and GCC.

---

## System Architecture

The initial boot sequence is:

```text
Computer Firmware
       |
       v
    GRUB
       |
       v
 EVENTIDE Kernel
       |
       v
 Kernel Initialization
       |
       v
 Basic Hardware Setup
       |
       v
  Command-Line Shell
       |
       v
  User Commands
```

### Project Structure

```text
EVENTIDE-OS/
│
├── boot/
│   └── Bootloader configuration
│
├── kernel/
│   └── Kernel implementation
│
├── arch/
│   └── x86/
│       └── Architecture-specific code
│
├── drivers/
│   └── Hardware drivers
│
├── include/
│   └── Shared header files
│
├── shell/
│   └── Command-line interface
│
├── memory/
│   └── Memory management
│
├── filesystem/
│   └── Filesystem implementation
│
├── docs/
│   ├── ARCHITECTURE.md
│   └── ROADMAP.md
│
├── scripts/
│   └── Build and utility scripts
│
├── .gitignore
├── LICENSE
└── README.md
```

---

## Development Environment

EVENTIDE OS is currently being developed using Ubuntu Linux inside Oracle VirtualBox on a Windows host.

### Required Tools

- Ubuntu Linux
- GCC and GNU Make
- NASM
- GNU Binutils
- GRUB utilities
- Xorriso
- Mtools
- QEMU
- i686-elf cross-compiler

### Ubuntu Dependencies

Install the basic development tools:

```bash
sudo apt update

sudo apt install -y \
  build-essential \
  nasm \
  grub-pc-bin \
  grub-common \
  xorriso \
  mtools \
  qemu-system-x86 \
  bison \
  flex \
  libgmp3-dev \
  libmpc-dev \
  libmpfr-dev \
  texinfo \
  wget \
  tar \
  xz-utils \
  python3
```

### Cross-Compiler Configuration

The planned cross-compiler target and installation prefix are:

```bash
export PREFIX="$HOME/opt/cross"
export TARGET=i686-elf
export PATH="$PREFIX/bin:$PATH"
```

These variables configure the development environment for the custom compiler toolchain.

The Binutils and GCC build process is currently in progress.

---

## Development Roadmap

The initial development target is a 14-day bootable OS project.

| Phase | Development Milestone |
|---|---|
| Day 1 | Repository, architecture and documentation |
| Day 2 | Development environment and cross-compiler |
| Day 3 | Bootloader configuration |
| Day 4 | Initial kernel implementation |
| Day 5 | Screen output |
| Day 6 | Keyboard input |
| Day 7 | Interrupt handling |
| Day 8 | Basic shell |
| Day 9 | Shell commands |
| Day 10 | Basic memory management |
| Day 11 | System utilities |
| Day 12 | Integration and debugging |
| Day 13 | Bootable ISO and testing |
| Day 14 | Documentation and v1.0 release |

For detailed progress, see [docs/ROADMAP.md](docs/ROADMAP.md).

---

## Current Development Status

**Status: Early Development**

Completed:

- [x] GitHub repository created.
- [x] Local development environment connected to GitHub.
- [x] Initial project directory structure created.
- [x] `.gitignore` configured.
- [x] System architecture documented.
- [x] Development roadmap documented.
- [x] Ubuntu environment prepared in VirtualBox.
- [x] GCC and GNU Make installed.
- [x] NASM, GRUB, QEMU and supporting tools installed.
- [x] Cross-compiler workspace configured.
- [x] GNU Binutils source downloaded and extracted.

In Progress:

- [ ] GNU Binutils configuration and compilation.
- [ ] i686-elf GCC cross-compiler.
- [ ] Initial kernel implementation.

No bootable kernel or ISO has been released yet.

---

## Development Philosophy

EVENTIDE OS follows a few core principles:

1. **Understand Before Implementing** — Learn the underlying concepts while writing the code.
2. **Build Incrementally** — Develop and test one component at a time.
3. **Keep It Simple** — Prioritize a working minimal OS before advanced features.
4. **Document Everything** — Maintain clear technical documentation.
5. **Consistency Matters** — Maintain meaningful Git commits and track development progress.

---

## Future Possibilities

Beyond v1.0, EVENTIDE OS may explore:

- Improved memory management.
- Process management and multitasking.
- Filesystem support.
- Additional hardware drivers.
- Networking capabilities.
- System calls and user-mode programs.
- Graphical user interface.

These are long-term goals, not features currently implemented.

---

## Contributing

EVENTIDE OS is currently an individual learning and development project.

Suggestions, discussions, and technical feedback are welcome.

## License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

---

## Project Information

**Project:** EVENTIDE OS  
**Developer:** Purushottam Pelapkar  
**Repository:** [github.com/purushottam08-nova/EVENTIDE-OS](https://github.com/purushottam08-nova/EVENTIDE-OS)

**Precision at the Edge of the Unknown.**