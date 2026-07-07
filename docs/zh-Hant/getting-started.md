# 快速入門指南

[English](../en-US/getting-started.md) | [简体中文](../zh-Hans/getting-started.md) | 繁體中文

本文件將幫助你從零開始執行 HelloWorld-Python 專案。

## 前提條件

你需要安裝 Python 2.6 或更高版本（Python 2.x 和 3.x 均可執行）。

### 檢查 Python 版本

```bash
python --version
# 或
python3 --version
```

如果輸出版本號 >= 2.6，即符合需求。如果尚未安裝 Python，請前往 [python.org](https://www.python.org/downloads/) 下載安裝。

## 安裝

本專案不依賴任何第三方函式庫，無需執行 `pip install` 等操作。

### 複製儲存庫

```bash
git clone https://github.com/WinTerminal/HelloWorld-Python.git
cd HelloWorld-Python
```

## 執行

```bash
python src/main.py
```

預期輸出：

```
Hello, World!
```

## 原始碼說明

專案的唯一原始碼檔案位於 `src/main.py`：

```python
#!/usr/bin/env python
print('Hello, ' + "World!")
```

### 逐行解釋

| 行號 | 程式碼 | 說明 |
|------|--------|------|
| 1 | `#!/usr/bin/env python` | Shebang 宣告，告訴作業系統使用 PATH 中的 Python 直譯器 |
| 2 | `print('Hello, ' + "World!")` | 使用 `+` 運算元串接兩個字串，透過 `print()` 輸出到主控台 |

### 關鍵概念

- **`print()` 函式**：Python 內建函式，將內容輸出到標準輸出（終端機）
- **字串串接**：使用 `+` 運算元將兩個字串連接為一個新字串
- **Shebang**：`#!/usr/bin/env python` 使腳本可透過 `./src/main.py` 直接執行（需先執行 `chmod +x`）

## 下一步

- 嘗試修改字串內容，觀察輸出變化
- 學習更多 [Python 基礎語法](https://docs.python.org/3/tutorial/)
