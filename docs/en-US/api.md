# API Reference

[English](api.md) | [简体中文](../zh-Hans/api.md) | [繁體中文](../zh-Hant/api.md)

## Overview

HelloWorld-Python exposes the following API for external use.

---

## Functions

### `main()`

The main entry point function (not yet encapsulated as a function — see Roadmap).

#### Signature

```python
def main() -> None
```

#### Parameters

None.

#### Returns

None. Side effect: prints `Hello, World!` to stdout.

#### Example

```python
from src.main import main

main()
# Output: Hello, World!
```

---

## String Concatenation Operation

### `'Hello, ' + "World!"`

#### Type

```
str + str → str
```

#### Behavior

Joins the left operand and right operand end to end.

#### Example

```python
>>> 'Hello, ' + "World!"
'Hello, World!'
```

---

## Standard Library Function

### `print(*objects, sep=' ', end='\n', file=sys.stdout, flush=False)`

Prints objects to a text stream.

#### Parameters

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `*objects` | `any` | — | Objects to print |
| `sep` | `str` | `' '` | Separator between objects |
| `end` | `str` | `'\n'` | Character appended after the last object |
| `file` | `file` | `sys.stdout` | Output target |
| `flush` | `bool` | `False` | Whether to flush the buffer immediately |

#### Usage in This Project

```python
print('Hello, ' + "World!")
```

Equivalent to:

```python
print('Hello, World!', sep=' ', end='\n', file=sys.stdout, flush=False)
```
