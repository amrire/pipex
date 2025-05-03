# pipex

## Description
**pipex** is a project written in C that mimics the behavior of shell pipelines (e.g., `ls | grep foo`). It is a great exercise in process creation, inter-process communication (IPC) using pipes, and file descriptor manipulation.

This project is intended for educational purposes, helping developers gain a deeper understanding of Unix system calls and how they can be used to build fundamental shell-like features.

---

## Features
- Replicates the behavior of shell pipes.
- Executes commands and connects their input/output streams.
- Handles multiple commands in a pipeline.
- Error handling for invalid commands, files, or arguments.

---

## Requirements
To compile and run this project, you'll need:
- A Unix-based operating system (Linux or macOS).
- A C compiler (preferably `gcc`).
- Make utility (to use the provided Makefile).

---

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/amrire/pipex.git
   cd pipex
   ```

2. Compile the project using the provided Makefile:
   ```bash
   make
   ```

3. The program will generate an executable called `pipex`.

---

## Usage
The general syntax for running **pipex** is:
```bash
./pipex infile "cmd1" "cmd2" ... "cmdn" outfile
```

### Example
```bash
./pipex input.txt "grep keyword" "wc -l" output.txt
```
This example will:
1. Read from `input.txt`.
2. Execute `grep keyword` and pass the output to `wc -l`.
3. Redirect the final output to `output.txt`.

---

## Files
- **src/**: Contains the source code.
- **include/**: Header files.
- **Makefile**: Automates the compilation of the project.
- **README.md**: Documentation for the project (you're reading this!).

---

## Learning Objectives
This project helps to:
- Understand and use Unix system calls such as `pipe`, `fork`, `execve`, and `dup2`.
- Learn how to handle file descriptors effectively.
- Debug and manage processes in a multi-process environment.
