# Architecture

[English](architecture.md) | [简体中文](../zh-Hans/architecture.md) | [繁體中文](../zh-Hant/architecture.md)

## Overview

HelloWorld-Python adopts a minimalist architecture design, reducing complexity to the minimum.

## System Architecture Diagram

```
┌─────────────────────────────────────────┐
│              User Terminal              │
│  ┌───────────────────────────────────┐  │
│  │         stdin (Standard Input)    │  │
│  └───────────────┬───────────────────┘  │
│                  │                       │
│  ┌───────────────▼───────────────────┐  │
│  │         Python Interpreter        │  │
│  │  ┌─────────────────────────────┐  │  │
│  │  │     src/main.py             │  │  │
│  │  │  ┌───────────────────────┐  │  │  │
│  │  │  │  String Concat Engine  │  │  │  │
│  │  │  │  'Hello, ' + "World!" │  │  │  │
│  │  │  └───────────┬───────────┘  │  │  │
│  │  │              │              │  │  │
│  │  │  ┌───────────▼───────────┐  │  │  │
│  │  │  │  print() Output System │  │  │  │
│  │  │  └───────────┬───────────┘  │  │  │
│  │  └──────────────┼──────────────┘  │  │
│  └─────────────────┼─────────────────┘  │
│                    │                     │
│  ┌─────────────────▼─────────────────┐  │
│  │       stdout (Standard Output)    │  │
│  │       Hello, World!               │  │
│  └───────────────────────────────────┘  │
└─────────────────────────────────────────┘
```

## Core Modules

### String Concatenation Engine

Merges the two string literals `'Hello, '` and `"World!"` via the `+` operator.

- **Input**: `str` + `str`
- **Output**: single `str`
- **Time complexity**: O(n)
- **Space complexity**: O(n)

### print() Output System

Writes the concatenated string to the standard output stream.

- **Call**: `print(content)`
- **Target**: `sys.stdout`
- **Line ending**: automatically appends `\n`

## Data Flow

```
Literal 'Hello, ' ──┐
                    ├──▶ Concat ──▶ 'Hello, World!' ──▶ print() ──▶ stdout
Literal "World!"  ──┘
```

## Design Decisions

| Decision | Choice | Rationale |
|----------|--------|-----------|
| String quotes | Mix single and double quotes | Demonstrates Python syntax flexibility |
| Output method | `print()` | Most intuitive output approach |
| Dependencies | Zero dependencies | Maximizes portability |
| Lines of code | 2 lines | KISS principle |

## Extensibility

The current architecture supports the following extensions:

1. **Multi-language versions** — Replace string literals
2. **Function encapsulation** — Extract logic into `def main():`
3. **Parameterized output** — Add `sys.argv` for command-line arguments
4. **Logging system** — Replace `print()` with the `logging` module
