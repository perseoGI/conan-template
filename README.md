# Conan C++ Project Template

A modern C++ project demonstrating cross-platform builds with Conan package manager, featuring zlib compression utilities and comprehensive testing with Google Test.

## 🚀 Features

- **Modern C++17** codebase with trailing return types, `auto`, and `[[nodiscard]]`
- **Cross-platform CI/CD** with GitHub Actions
- **Multi-architecture builds** (x86_64 and armv8)
- **Conan package management** for dependency management
- **Google Test integration** for unit testing
- **Compression utilities** using zlib
- **Logging** with spdlog

## 📋 Prerequisites

- **Conan** 2.x
- **C++17 compatible compiler**:
  - GCC 7+
  - Clang 5+
  - MSVC 2017+
- **Python** 3.7+ (for Conan)

## 🛠️ Building the Project

### Install Dependencies

```bash
# Install Conan if you haven't already
pip install conan

# Detect your Conan profile
conan profile detect --force
```

### Build

```bash
# Build the project (installs dependencies and compiles)
conan build . --build=missing
```

### Run the Application

```bash
# Linux/macOS
./build/Release/myapp

# Windows
.\build\Release\myapp.exe
```

### Run Tests

```bash
# Linux/macOS
./build/Release/myapp_tests

# Windows
.\build\Release\myapp_tests.exe
```
