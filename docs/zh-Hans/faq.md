# 常见问题

[English](../en-US/faq.md) | 简体中文 | [繁體中文](../zh-Hant/faq.md)

## 基础问题

### Q: 这个项目是做什么的？

A: 在终端输出 `Hello, World!`。

### Q: 为什么用两种引号？

A: `'Hello, '` 使用单引号，`"World!"` 使用双引号。Python 中两者等价，混用仅用于展示语法灵活性。

### Q: 代码只有两行，需要这么大的仓库吗？

A: 需要。每一行都值得被 Git 管理。

---

## 环境问题

### Q: 我的 Python 版本低于 2.6 怎么办？

A: 请升级 Python。Python 2.5 及更早版本不支持此项目。

### Q: `python` 命令找不到，只有 `python3`？

A: 尝试使用 `python3 src/main.py` 运行，或将 Python 3 链接为 `python`。

### Q: Windows 上运行报编码错误？

A: 确保终端使用 UTF-8 编码：

```bash
chcp 65001
python src/main.py
```

### Q: 在 Docker 中能运行吗？

A: 可以。创建以下 Dockerfile：

```dockerfile
FROM python:2.7-slim
COPY src/main.py /app/main.py
CMD ["python", "/app/main.py"]
```

构建并运行：

```bash
docker build -t hello-world .
docker run hello-world
```

---

## 开发问题

### Q: 能添加单元测试吗？

A: 可以。使用标准库 `unittest` 或第三方 `pytest`。

### Q: 能用 `f-string` 重写吗？

A: `f-string` 需要 Python 3.6+。如果需要保持 2.6 兼容性，请使用 `str.format()` 或字符串拼接。

### Q: 能输出到文件而非终端吗？

A: 可以：

```python
with open('output.txt', 'w') as f:
    f.write('Hello, World!\n')
```
