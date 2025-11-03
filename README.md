# PWM

[![Languages](https://img.shields.io/badge/C-97%25-blue)](https://github.com/Harveker/PWM)
[![Languages](https://img.shields.io/badge/Assembly-2.9%25-lightgrey)](https://github.com/Harveker/PWM)
[![Languages](https://img.shields.io/badge/CMake-0.1%25-lightgrey)](https://github.com/Harveker/PWM)

## Overview

**PWM** is a project written primarily in C, with small portions in Assembly and CMake.  
This repository implements functionality related to Pulse Width Modulation (PWM), a common technique used in embedded systems, motor controls, and signal generation.

## Features

- High-performance PWM signal generation in C
- Low-level hardware interaction (Assembly)
- Easy build and configuration with CMake

## Getting Started

### Prerequisites

- C compiler (e.g., GCC)
- CMake (for build configuration)
- [Optional] Assembler (if building/using assembly modules)

### Build Instructions

```bash
git clone https://github.com/Harveker/PWM.git
cd PWM
mkdir build
cd build
cmake ..
make
```

### Usage

Provide details here about how to run or use your project, including sample commands or configuration.

## Project Structure

- **src/** – Main C source files
- **asm/** – Assembly source files (if any)
- **CMakeLists.txt** – CMake build configuration

## Contributing

Pull requests are welcome. For significant changes, please open an issue first to discuss what you would like to change.

Please read [SECURITY.md](SECURITY.md) for security guidelines and best practices.

## Security & Privacy

This repository has been secured with:
- Comprehensive `.gitignore` to prevent accidental commits of sensitive files
- Privacy-focused IDE configuration without absolute paths
- Security guidelines in [SECURITY.md](SECURITY.md)

**Note**: Historical git commits may contain email addresses. See [GIT_HISTORY_CLEANUP.md](GIT_HISTORY_CLEANUP.md) for information on managing git history privacy.

## License

Specify the license here. (e.g., MIT, GPL-3.0, etc.)
