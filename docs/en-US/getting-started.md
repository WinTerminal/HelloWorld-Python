# Getting Started

[English](getting-started.md) | [简体中文](../zh-Hans/getting-started.md) | [繁體中文](../zh-Hant/getting-started.md)

This guide will help you run the HelloWorld-Python project from scratch.

## Prerequisites

You need Python 2.6 or higher (both Python 2.x and 3.x work).

### Check Python version

```bash
python --version
# or
python3 --version
```

If the version is >= 2.6, you're good. If Python is not installed, visit [python.org](https://www.python.org/downloads/) to download it.

## Installation

This project has no third-party dependencies — no `pip install` needed.

### Clone the repository

```bash
git clone https://github.com/WinTerminal/HelloWorld-Python.git
cd HelloWorld-Python
```

## Run

```bash
python src/main.py
```

Expected output:

```
Hello, World!
```

## Source Code Walkthrough

The only source file is located at `src/main.py`:

```python
#!/usr/bin/env python
print('Hello, ' + "World!")
```

### Line-by-line Explanation

| Line | Code | Description |
|------|------|-------------|
| 1 | `#!/usr/bin/env python` | Shebang declaration, tells the OS to use the Python interpreter from PATH |
| 2 | `print('Hello, ' + "World!")` | Uses `+` to concatenate two strings, then outputs via `print()` to the console |

### Key Concepts

- **`print()` function**: Python built-in function that outputs content to stdout (the terminal)
- **String concatenation**: Using `+` to join two strings into a new string
- **Shebang**: `#!/usr/bin/env python` allows the script to be run directly via `./src/main.py` (requires `chmod +x` first)

## Next Steps

- Try modifying the string content and observe the output change
- Learn more [Python basics](https://docs.python.org/3/tutorial/)
