# EVENTIDE OS � System Architecture

## 1. Overview

EVENTIDE OS is a custom operating system developed from scratch.
The initial release focuses on a simple bootable 32-bit x86 system
with a basic command-line interface.

## 2. Initial Technical Decisions

| Component | Technology |
|---|---|
| Architecture | 32-bit x86 |
| Kernel Language | C |
| Low-level Programming | Assembly |
| Bootloader | GRUB |
| Boot Protocol | Multiboot |
| Assembler | NASM |
| Compiler | i686-elf GCC |
| Emulator | QEMU |
| Build System | GNU Make |

## 3. Boot Sequence

1. The computer starts through its firmware.
2. GRUB loads the EVENTIDE OS kernel.
3. GRUB transfers control to the kernel using the Multiboot protocol.
4. The kernel initializes essential hardware and system components.
5. The kernel starts the basic command-line interface.

## 4. Project Structure

- `boot/` � Bootloader configuration and related files.
- `kernel/` � Main kernel implementation.
- `arch/x86/` � x86 architecture-specific implementation.
- `drivers/` � Hardware drivers.
- `include/` � Shared C header files.
- `shell/` � Basic command-line interface.
- `memory/` � Memory management.
- `filesystem/` � Initial filesystem experiments.
- `docs/` � Technical documentation.
- `scripts/` � Build and development scripts.

## 5. Initial Release Scope

EVENTIDE OS v1.0 aims to provide:

- A bootable kernel.
- Basic screen output.
- Keyboard input.
- A simple command-line shell.
- A small set of built-in commands.
- A reproducible build and QEMU testing process.

Advanced memory management, multitasking, a full filesystem,
networking and graphical interfaces are future development goals.

## 6. Development Philosophy

- Build incrementally.
- Keep the initial implementation small and understandable.
- Test every major milestone in QEMU.
- Document important architectural decisions.
- Maintain a clean and traceable Git history.
