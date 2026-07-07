# HelloWorld-Python

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Python](https://img.shields.io/badge/python-2.6%2B-brightgreen.svg)

简体中文 | [繁體中文](README.zh-Hant.md) | [English](README.md)

用 Python 编写的 Hello World 示例程序，适用于初学者快速上手。

## 预览

| Linux | macOS | Windows |
|:-----:|:-----:|:-------:|
| ![Linux](preview-linux.png) | ![macOS](preview-macos.png) | ![Windows](preview-windows.png) |

## 特性

- 纯标准库实现，无需安装任何第三方依赖
- 跨平台兼容（Linux / macOS / Windows）
- 代码简洁，适合 Python 入门学习
- Python 2.6 及以上版本均可运行

## 环境要求

| 依赖 | 版本要求 |
|------|---------|
| Python | >= 2.6 |
| 第三方库 | 无 |

确认已安装 Python：

```bash
python --version
# 或
python3 --version
```

## 快速开始

### 1. 克隆项目

```bash
git clone https://github.com/WinTerminal/HelloWorld-Python.git
cd HelloWorld-Python
```

### 2. 运行程序

```bash
python src/main.py
```

### 3. 查看输出

```
Hello, World!
```

## 项目结构

```
HelloWorld-Python/
├── src/
│   └── main.py              # 程序入口
├── docs/
│   ├── getting-started.md   # 快速上手指南
│   ├── architecture.md      # 架构设计文档
│   ├── api.md               # API 参考文档
│   ├── faq.md               # 常见问题
│   └── troubleshooting.md   # 故障排查指南
├── readme/
│   └── README.md            # 项目说明文档
├── preview-linux.png        # Linux 平台运行截图
├── preview-macos.png        # macOS 平台运行截图
├── preview-windows.png      # Windows 平台运行截图
├── requirements.txt         # 依赖声明（无）
├── LICENSE                  # MIT 许可证
└── .gitignore               # Git 忽略规则
```

## 源码说明

`src/main.py` 是唯一的源文件，内容如下：

```python
#!/usr/bin/env python
print('Hello, ' + "World!")
```

- `#!/usr/bin/env python` — Shebang 行，指定使用系统默认 Python 解释器运行
- `print('Hello, ' + "World!")` — 使用字符串拼接输出 `Hello, World!`

## 常见问题

### Python 2 能运行吗？

可以。`print('Hello, ' + "World!")` 在 Python 2.6+ 中同样有效——括号在此处仅作为表达式分组，不会被当作函数调用。

### 运行时出现 `No such file or directory`

请确认当前工作目录在项目根目录下，并使用 `python src/main.py` 而非 `python main.py`。

## 相关文档

| 文档 | 说明 |
|------|------|
| [快速上手指南](docs/zh-Hans/getting-started.md) | 从零开始运行项目 |
| [架构设计文档](docs/zh-Hans/architecture.md) | 系统架构与数据流 |
| [API 参考文档](docs/zh-Hans/api.md) | 函数与操作说明 |
| [常见问题](docs/zh-Hans/faq.md) | FAQ |
| [故障排查指南](docs/zh-Hans/troubleshooting.md) | 错误信息速查与排查 |

## 有趣的事实

- `main.py` 只有 **2 行**，所有语言的文档加起来共 **1659 行** — 文档是代码的 **829.5 倍**。

| 文件 | 行数 |
|------|-----:|
| `README.md` | 125 |
| `README.zh-Hans.md` | 125 |
| `README.zh-Hant.md` | 125 |

## 许可证

本项目基于 MIT 许可证开源 — 详见 [LICENSE](LICENSE) 了解详情。
