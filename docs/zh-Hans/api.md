# API 参考文档

[English](../en-US/api.md) | 简体中文 | [繁體中文](../zh-Hant/api.md)

## 概述

HelloWorld-Python 暴露以下 API 供外部调用。

---

## 函数

### `main()`

程序主入口函数（当前未封装为函数，参见 Roadmap）。

#### 签名

```python
def main() -> None
```

#### 参数

无。

#### 返回值

无。副作用：向标准输出打印 `Hello, World!`。

#### 示例

```python
from src.main import main

main()
# 输出: Hello, World!
```

---

## 字符串拼接操作

### `'Hello, ' + "World!"`

#### 类型

```
str + str → str
```

#### 行为

将左操作数和右操作数首尾相连。

#### 示例

```python
>>> 'Hello, ' + "World!"
'Hello, World!'
```

---

## 标准库函数

### `print(*objects, sep=' ', end='\n', file=sys.stdout, flush=False)`

将对象打印到文本流。

#### 参数

| 参数 | 类型 | 默认值 | 说明 |
|------|------|--------|------|
| `*objects` | `any` | — | 要打印的对象 |
| `sep` | `str` | `' '` | 对象之间的分隔符 |
| `end` | `str` | `'\n'` | 追加在末尾的字符 |
| `file` | `file` | `sys.stdout` | 输出目标 |
| `flush` | `bool` | `False` | 是否立即刷新缓冲区 |

#### 本项目的调用方式

```python
print('Hello, ' + "World!")
```

等价于：

```python
print('Hello, World!', sep=' ', end='\n', file=sys.stdout, flush=False)
```
