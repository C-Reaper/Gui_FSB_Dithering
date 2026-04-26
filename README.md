# Project README

## Overview
The project "FSB Dithering" is a simple graphical application designed to demonstrate image dithering techniques. It uses a custom windowing library and provides real-time interaction to adjust the number of quantization levels (QuantiseN), which controls the complexity and visual effect of the dithering.

## Features
- **Real-time Dithering**: Allows users to interactively change the number of quantization levels to observe different dithering effects.
- **Custom Windowing Library**: Utilizes a custom C library for window management, handling graphics rendering and user input.
- **Cross-platform Support**: The project includes Makefile configurations for Linux, Windows, Wine (Linux cross-compilation for Windows), and WebAssembly (for browser execution).

## Project Structure
### Prerequisites
- **C/C++ Compiler and Debugger**: GCC is used across platforms.
- **Make utility**: For building the project.
- **Standard Development Tools**: Required for development and compilation.
- **Libraries**:
  - **Linux**: X11, PNG, JPEG (for image handling).
  - **Windows**: user32, gdi32, winmm (Windows API).
  - **Wine**: user32, gdi32, winmm (Linux cross-compilation for Windows).
  - **WebAssembly**: emcc (Emscripten Compiler).

## Build & Run
### Linux
To build and run the application on Linux:
1. Navigate to the project directory.
2. Use `make -f Makefile.linux all` to compile the project.
3. Execute the compiled binary using `make -f Makefile.linux exe`.

### Windows
For building and running on Windows, use one of the following commands:
- **All**: `make -f Makefile.windows all`
- **Debug**: `make -f Makefile.windows dg`
- **Run**: `make -f Makefile.windows exe`

### Wine (Linux Cross-Compilation for Windows)
To compile and run the application using Wine on Linux:
1. Navigate to the project directory.
2. Use `make -f Makefile.wine all` to compile the project.
3. Execute the compiled binary using `make -f Makefile.wine exe`.

### WebAssembly (Emscripten)
For building a web version of the application, use one of the following commands:
- **All**: `make -f Makefile.web all`
- **Debug**: `make -f Makefile.web dg`
- **Run**: Navigate to the build directory and open `index.html` in a browser.

The project's structure is clean, with specific directories for source code, build outputs, and configuration files. All required tools and libraries are clearly listed in the prerequisites section, ensuring that developers can set up their environment accordingly.