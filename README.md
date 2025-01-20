# ArsenicOS (TriHydroArsenicOS)

ArsenicOS is a hobbyist operating system inspired by the work of nanobyte_dev and his popular "How to make an OS" series. The project is designed as a learning experience, exploring low-level systems programming, kernel design, and hardware interfacing. This README outlines the goals, features, build instructions, and roadmap for the project.

---

## Vision

ArsenicOS aims to:

- Provide a lightweight and modular kernel.
- Serve as a learning tool for understanding operating systems development.
- Implement features incrementally, allowing flexibility and experimentation.
- Maintain clean and well-documented code.

---

## Features

### Current Features:
- **16-bit Real Mode Bootloader**: A custom bootloader that initializes the system.
- **Minimal Kernel**: A basic kernel written in C++ and assembly (NASM).
- **Text Output**: Basic VGA text rendering to display information.
- **Hardware Interfacing**: Initial implementation of low-level hardware drivers.

### Planned Features:
- **32-bit Protected Mode Support**: Transition from Real Mode for enhanced performance and memory access.
- **Memory Management**: Implementation of a basic memory manager with paging.
- **Filesystem Support**: Integration of a custom or standard filesystem like FAT12/16.
- **Task Scheduling**: Basic multitasking with a round-robin scheduler.
- **Shell Interface**: A simple command-line interface for user interaction.
- **User Mode**: Separation of user and kernel space for stability and security.

---

## Project Structure

```
ArsenicOS/
├── src/
├───── bootloader/
├───── kernel/
├── build/
├── Makefile
```

---

## Build Instructions

### Prerequisites:
- **NASM**: An assembler for the bootloader and low-level code.
- **QEMU**: Emulator for testing the OS.
- **Make**: For automating the build process.

### Steps:
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/ArsenicOS.git
   cd ArsenicOS
   ```

2. Build the OS:
   ```bash
   make
   ```

3. Run the OS in QEMU:
   ```bash
   qemu-system-i386 -fda build/main_floppy.bin
   ```

---

## Contributions

Contributions are welcome! If you'd like to improve ArsenicOS or add new features:

1. Fork the repository and create a new branch.
2. Make your changes and ensure they adhere to the coding standards.
3. Submit a pull request with a detailed description of your changes.

---

## Resources and Credits

- **nanobyte_dev**: Inspiration and guidance through the "How to make an OS" series.
- **OSDev Wiki**: Comprehensive resource for operating system development.
- **Bare Metal Programming**: Community and tutorials for low-level development.

---

## License

ArsenicOS is licensed under the GNUv3 License. See `LICENSE` for more details.

---

## Roadmap

| Milestone              | Status       | Description                                  |
|------------------------|--------------|----------------------------------------------|
| Bootloader             | Completed    | Develop a basic bootloader in 16-bit assembly. |
| Basic Kernel           | In Progress  | Implement a kernel with VGA text output.      |
| Protected Mode         | Planned      | Add 32-bit protected mode support.           |
| Memory Management      | Planned      | Introduce paging and memory allocation.      |
| Shell Interface        | Planned      | Design and implement a basic shell.          |
| Multitasking           | Planned      | Add basic task scheduling capabilities.       |

---

Thank you for checking out ArsenicOS! We hope this project inspires and educates you as much as it does us.
