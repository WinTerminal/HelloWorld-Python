# FAQ

[English](faq.md) | [简体中文](../zh-Hans/faq.md) | [繁體中文](../zh-Hant/faq.md)

## General

### Q: What does this project do?

A: Outputs `Hello, World!` to the terminal.

### Q: Why are two types of quotes used?

A: `'Hello, '` uses single quotes, `"World!"` uses double quotes. Both are equivalent in Python; mixing them only demonstrates syntax flexibility.

### Q: The code is only 2 lines — does it really need such a large repository?

A: Yes. Every line deserves to be managed by Git.

---

## Environment

### Q: My Python version is below 2.6. What should I do?

A: Please upgrade Python. Python 2.5 and earlier versions are not supported.

### Q: `python` command not found, only `python3`?

A: Try running with `python3 src/main.py`, or symlink Python 3 as `python`.

### Q: Encoding error on Windows?

A: Make sure the terminal uses UTF-8 encoding:

```bash
chcp 65001
python src/main.py
```

### Q: Can it run in Docker?

A: Yes. Create the following Dockerfile:

```dockerfile
FROM python:2.7-slim
COPY src/main.py /app/main.py
CMD ["python", "/app/main.py"]
```

Build and run:

```bash
docker build -t hello-world .
docker run hello-world
```

---

## Development

### Q: Can I add unit tests?

A: Yes. Use the standard library `unittest` or third-party `pytest`.

### Q: Can I rewrite it with `f-string`?

A: `f-string` requires Python 3.6+. If you need to maintain 2.6 compatibility, use `str.format()` or string concatenation.

### Q: Can I output to a file instead of the terminal?

A: Yes:

```python
with open('output.txt', 'w') as f:
    f.write('Hello, World!\n')
```
