# 常見問題

[English](../en-US/faq.md) | [简体中文](../zh-Hans/faq.md) | 繁體中文

## 基礎問題

### Q: 這個專案是做什麼的？

A: 在終端機輸出 `Hello, World!`。

### Q: 為什麼用兩種引號？

A: `'Hello, '` 使用單引號，`"World!"` 使用雙引號。Python 中兩者等價，混用僅用於展示語法靈活度。

### Q: 程式碼只有兩行，需要這麼大的儲存庫嗎？

A: 需要。每一行都值得被 Git 管理。

---

## 環境問題

### Q: 我的 Python 版本低於 2.6 怎麼辦？

A: 請升級 Python。Python 2.5 及更早版本不支援此專案。

### Q: `python` 命令找不到，只有 `python3`？

A: 嘗試使用 `python3 src/main.py` 執行，或將 Python 3 連結為 `python`。

### Q: Windows 上執行報編碼錯誤？

A: 確保終端機使用 UTF-8 編碼：

```bash
chcp 65001
python src/main.py
```

### Q: 在 Docker 中能執行嗎？

A: 可以。建立以下 Dockerfile：

```dockerfile
FROM python:2.7-slim
COPY src/main.py /app/main.py
CMD ["python", "/app/main.py"]
```

建構並執行：

```bash
docker build -t hello-world .
docker run hello-world
```

---

## 開發問題

### Q: 能新增單元測試嗎？

A: 可以。使用標準庫 `unittest` 或第三方 `pytest`。

### Q: 能用 `f-string` 重寫嗎？

A: `f-string` 需要 Python 3.6+。如果需要維持 2.6 相容性，請使用 `str.format()` 或字串串接。

### Q: 能輸出到檔案而非終端機嗎？

A: 可以：

```python
with open('output.txt', 'w') as f:
    f.write('Hello, World!\n')
```
