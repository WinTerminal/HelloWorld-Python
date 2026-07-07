# Troubleshooting

[English](troubleshooting.md) | [简体中文](../zh-Hans/troubleshooting.md) | [繁體中文](../zh-Hant/troubleshooting.md)

## Error Message Quick Reference

| Error Message | Cause | Solution |
|---------------|-------|----------|
| `SyntaxError: Missing parentheses in call to 'print'` | Using Python 2 syntax in Python 3 | Not applicable to this project (parentheses are used) |
| `No such file or directory` | Incorrect file path | Make sure to run from the project root directory |
| `Permission denied` | Script lacks execute permission | Run `chmod +x src/main.py` |
| `python: command not found` | Python not installed or not in PATH | Install Python or use `python3` |
| `IndentationError` | Inconsistent indentation | Check code indentation, use spaces |

## Common Scenario Troubleshooting

### Scenario 1: No output after running

**Symptom**: No output appears in the terminal after executing the command.

**Steps to diagnose**:

1. Verify the file exists:

```bash
ls -la src/main.py
```

2. Check the file contents:

```bash
cat src/main.py
```

3. Run manually:

```bash
python -c "print('Hello, ' + 'World!')"
```

### Scenario 2: Garbled output

**Symptom**: Output contains `???` or block characters.

**Solution**:

```bash
# Linux / macOS
export LANG=en_US.UTF-8
python src/main.py

# Windows
set PYTHONIOENCODING=utf-8
python src/main.py
```

### Scenario 3: Python version conflict

**Symptom**: Multiple Python versions installed, wrong version is used.

**Diagnose**:

```bash
which python
which python3
python --version
python3 --version
```

**Solution**: Use the full path or a virtual environment.

## Debug Logging

For debugging, you can add to `main.py`:

```python
import sys
print('Hello, ' + "World!", file=sys.stderr)  # Output to stderr
```

## Getting Help

If the above solutions don't resolve the issue, please submit a GitHub Issue with:

1. Operating system and version
2. Python version (`python --version`)
3. Full error message
4. Command that was executed
