# 疑難排解指南

[English](../en-US/troubleshooting.md) | [简体中文](../zh-Hans/troubleshooting.md) | 繁體中文

## 錯誤訊息速查表

| 錯誤訊息 | 原因 | 解決方案 |
|---------|------|---------|
| `SyntaxError: Missing parentheses in call to 'print'` | 在 Python 3 中使用 Python 2 語法 | 本專案不涉及此問題（已使用括號） |
| `No such file or directory` | 檔案路徑錯誤 | 確認在專案根目錄下執行 |
| `Permission denied` | 腳本無執行權限 | 執行 `chmod +x src/main.py` |
| `python: command not found` | 未安裝 Python 或未加入 PATH | 安裝 Python 或使用 `python3` |
| `IndentationError` | 縮排不一致 | 檢查程式碼縮排，使用空格 |

## 常見情境排查

### 情境 1: 執行後無輸出

**症狀**：執行命令後終端機無任何輸出。

**排查步驟**：

1. 確認檔案存在：

```bash
ls -la src/main.py
```

2. 確認檔案內容：

```bash
cat src/main.py
```

3. 手動執行：

```bash
python -c "print('Hello, ' + 'World!')"
```

### 情境 2: 輸出亂碼

**症狀**：輸出包含 `???` 或方塊字元。

**解決方案**：

```bash
# Linux / macOS
export LANG=en_US.UTF-8
python src/main.py

# Windows
set PYTHONIOENCODING=utf-8
python src/main.py
```

### 情境 3: Python 版本衝突

**症狀**：系統有多個 Python 版本，執行了錯誤的版本。

**排查**：

```bash
which python
which python3
python --version
python3 --version
```

**解決**：使用完整路徑或虛擬環境。

## 日誌除錯

如需除錯，可在 `main.py` 中新增：

```python
import sys
print('Hello, ' + "World!", file=sys.stderr)  # 輸出到 stderr
```

## 取得協助

如以上方案無法解決問題，請在 GitHub 提交 Issue 並附上：

1. 作業系統及版本
2. Python 版本（`python --version`）
3. 完整的錯誤訊息
4. 執行的命令
