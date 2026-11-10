#  EVENTIDE OS

### Precision at the Edge of the Unknown.

**EVENTIDE OS** is an experimental operating system developed from scratch to explore the fundamentals of operating systems, kernel development, computer architecture, and low-level programming.

The goal is to understand how computers work beneath the applications we use every day by building our own operating system, one component at a time.

---

##  Project Vision

Most of us use operating systems without understanding what happens behind the screen.

EVENTIDE OS is an attempt to change that.

This project aims to build a custom, lightweight operating system with its own kernel, memory management, device drivers, command-line interface, filesystem, and eventually a graphical user interface.

It is both a hands-on systems programming project and a journey into the fundamentals of computer science.

##  Objectives

- Build a bootable operating system from scratch.
- Understand the boot process and kernel architecture.
- Implement low-level hardware interaction.
- Develop basic memory and process management.
- Create a custom command-line shell.
- Explore filesystem implementation.
- Gradually introduce graphical capabilities.
- Maintain an open-source development workflow.

##  Technology Stack

| Technology | Purpose |
|---|---|
| C | Kernel development |
| Assembly | Low-level hardware interaction |
| GRUB | Bootloader |
| GCC Cross Compiler | Kernel compilation |
| NASM | Assembly development |
| QEMU | Virtual machine testing |
| Make | Build automation |
| Git & GitHub | Version control |

*The technology stack may evolve as development progresses.*

##  Planned Architecture

```text
EVENTIDE-OS/
│
├── boot/              # Bootloader configuration
├── kernel/            # Core kernel implementation
├── drivers/           # Hardware drivers
├── arch/              # Architecture-specific code
├── memory/            # Memory management
├── interrupts/        # Interrupt handling
├── shell/             # Command-line interface
├── filesystem/        # Filesystem implementation
├── include/           # Header files
├── scripts/           # Build and utility scripts
├── docs/              # Technical documentation
│
├── Makefile
├── README.md
└── .gitignore
```

*This is the intended project structure, not a claim that all components have been implemented.*

##  Development Roadmap

- [ ] Phase 1 — Project foundation and development environment
- [ ] Phase 2 — Bootloader integration and first kernel boot
- [ ] Phase 3 — Basic kernel functionality and screen output
- [ ] Phase 4 — Keyboard input and interrupt handling
- [ ] Phase 5 — Memory management
- [ ] Phase 6 — Command-line shell
- [ ] Phase 7 — Filesystem and process management
- [ ] Phase 8 — Graphics and desktop environment
- [ ] Phase 9 — Testing, optimization, and release

##  Development Philosophy

EVENTIDE OS follows a learn-by-building approach.

Every subsystem will be developed incrementally, tested independently wherever possible, and documented to explain its design and implementation.

The focus is not simply to make an operating system boot, but to understand why and how each component works.

##  Learning Goals

Through this project, I aim to gain practical experience in:

- Operating System Design
- Kernel Development
- Computer Architecture
- Systems Programming
- Memory Management
- Hardware and Software Interaction
- Low-Level Debugging
- Open-Source Collaboration

##  Contributions

EVENTIDE OS is an experimental open-source learning project.

Suggestions, discussions, bug reports, and contributions are welcome as the project matures.

##  License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

<p align="center">
  **EVENTIDE OS**
  <br/>
  *Exploring the universe beneath the interface.*
</p>
