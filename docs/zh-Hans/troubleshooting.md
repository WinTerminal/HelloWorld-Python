# 故障排查指南

[English](../en-US/troubleshooting.md) | 简体中文 | [繁體中文](../zh-Hant/troubleshooting.md)

## 错误信息速查表

| 错误信息 | 原因 | 解决方案 |
|---------|------|---------|
| `SyntaxError: Missing parentheses in call to 'print'` | 使用了 Python 3 调用 Python 2 语法 | 本项目不涉及此问题（已使用括号） |
| `No such file or directory` | 文件路径错误 | 确认在项目根目录下执行 |
| `Permission denied` | 脚本无执行权限 | 执行 `chmod +x src/main.py` |
| `python: command not found` | 未安装 Python 或未加入 PATH | 安装 Python 或使用 `python3` |
| `IndentationError` | 缩进不一致 | 检查代码缩进，使用空格 |

## 常见场景排查

### 场景 1: 运行后无输出

**症状**：执行命令后终端无任何输出。

**排查步骤**：

1. 确认文件存在：

```bash
ls -la src/main.py
```

2. 确认文件内容：

```bash
cat src/main.py
```

3. 手动运行：

```bash
python -c "print('Hello, ' + 'World!')"
```

### 场景 2: 输出乱码

**症状**：输出包含 `???` 或方块字符。

**解决方案**：

```bash
# Linux / macOS
export LANG=en_US.UTF-8
python src/main.py

# Windows
set PYTHONIOENCODING=utf-8
python src/main.py
```

### 场景 3: Python 版本冲突

**症状**：系统有多个 Python 版本，运行了错误的版本。

**排查**：

```bash
which python
which python3
python --version
python3 --version
```

**解决**：使用完整路径或虚拟环境。

## 日志调试

如需调试，可在 `main.py` 中添加：

```python
import sys
print('Hello, ' + "World!", file=sys.stderr)  # 输出到 stderr
```

## 获取帮助

如以上方案无法解决问题，请在 GitHub 提交 Issue 并附上：

1. 操作系统及版本
2. Python 版本（`python --version`）
3. 完整的错误信息
4. 执行的命令
