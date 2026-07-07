# API 參考文件

[English](../en-US/api.md) | [简体中文](../zh-Hans/api.md) | 繁體中文

## 概述

HelloWorld-Python 暴露以下 API 供外部呼叫。

---

## 函式

### `main()`

程式主進入點函式（目前尚未封裝為函式，請參見 Roadmap）。

#### 簽章

```python
def main() -> None
```

#### 參數

無。

#### 回傳值

無。副作用：向標準輸出列印 `Hello, World!`。

#### 範例

```python
from src.main import main

main()
# 輸出: Hello, World!
```

---

## 字串串接運算

### `'Hello, ' + "World!"`

#### 型別

```
str + str → str
```

#### 行為

將左運算元和右運算元首尾相連。

#### 範例

```python
>>> 'Hello, ' + "World!"
'Hello, World!'
```

---

## 標準庫函式

### `print(*objects, sep=' ', end='\n', file=sys.stdout, flush=False)`

將物件列印到文字串流。

#### 參數

| 參數 | 型別 | 預設值 | 說明 |
|------|------|--------|------|
| `*objects` | `any` | — | 要列印的物件 |
| `sep` | `str` | `' '` | 物件之間的分隔符 |
| `end` | `str` | `'\n'` | 追加在末尾的字元 |
| `file` | `file` | `sys.stdout` | 輸出目標 |
| `flush` | `bool` | `False` | 是否立即刷新緩衝區 |

#### 本專案的呼叫方式

```python
print('Hello, ' + "World!")
```

等同於：

```python
print('Hello, World!', sep=' ', end='\n', file=sys.stdout, flush=False)
```
