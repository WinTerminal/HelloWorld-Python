# 快速上手指南

[English](../en-US/getting-started.md) | 简体中文 | [繁體中文](../zh-Hant/getting-started.md)

本文档将帮助你从零开始运行 HelloWorld-Python 项目。

## 前提条件

你需要安装 Python 2.6 或更高版本（Python 2.x 和 3.x 均可）。

### 检查 Python 版本

```bash
python --version
# 或
python3 --version
```

如果输出版本号 >= 2.6，则满足要求。如果未安装 Python，请前往 [python.org](https://www.python.org/downloads/) 下载安装。

## 安装

本项目不依赖任何第三方库，无需执行 `pip install` 等操作。

### 克隆仓库

```bash
git clone https://github.com/WinTerminal/HelloWorld-Python.git
cd HelloWorld-Python
```

## 运行

```bash
python src/main.py
```

预期输出：

```
Hello, World!
```

## 源码解析

项目的唯一源文件位于 `src/main.py`：

```python
#!/usr/bin/env python
print('Hello, ' + "World!")
```

### 逐行解释

| 行号 | 代码 | 说明 |
|------|------|------|
| 1 | `#!/usr/bin/env python` | Shebang 声明，告诉操作系统使用 PATH 中的 Python 解释器 |
| 2 | `print('Hello, ' + "World!")` | 使用 `+` 运算符拼接两个字符串，通过 `print()` 输出到控制台 |

### 关键概念

- **`print()` 函数**：Python 内置函数，将内容输出到标准输出（终端）
- **字符串拼接**：使用 `+` 运算符将两个字符串连接为一个新字符串
- **Shebang**：`#!/usr/bin/env python` 使脚本可通过 `./src/main.py` 直接执行（需先 `chmod +x`）

## 下一步

- 尝试修改字符串内容，观察输出变化
- 学习更多 [Python 基础语法](https://docs.python.org/3/tutorial/)
