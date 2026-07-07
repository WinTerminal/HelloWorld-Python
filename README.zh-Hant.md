# HelloWorld-Python

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Python](https://img.shields.io/badge/python-2.6%2B-brightgreen.svg)

[简体中文](README.zh-Hans.md) | 繁體中文 | [English](README.md)

使用 Python 編寫的 Hello World 範例程式，適用於初學者快速上手。

## 預覽

| Linux | macOS | Windows |
|:-----:|:-----:|:-------:|
| ![Linux](preview-linux.png) | ![macOS](preview-macos.png) | ![Windows](preview-windows.png) |

## 特性

- 純標準庫實作，無需安裝任何第三方依賴
- 跨平台相容（Linux / macOS / Windows）
- 程式碼簡潔，適合 Python 入門學習
- Python 2.6 及以上版本均可執行

## 環境需求

| 依賴 | 版本需求 |
|------|---------|
| Python | >= 2.6 |
| 第三方函式庫 | 無 |

確認已安裝 Python：

```bash
python --version
# 或
python3 --version
```

## 快速開始

### 1. 複製專案

```bash
git clone https://github.com/WinTerminal/HelloWorld-Python.git
cd HelloWorld-Python
```

### 2. 執行程式

```bash
python src/main.py
```

### 3. 檢視輸出

```
Hello, World!
```

## 專案結構

```
HelloWorld-Python/
├── src/
│   └── main.py              # 程式進入點
├── docs/
│   ├── getting-started.md   # 快速入門指南
│   ├── architecture.md      # 架構設計文件
│   ├── api.md               # API 參考文件
│   ├── faq.md               # 常見問題
│   └── troubleshooting.md   # 疑難排解指南
├── readme/
│   └── README.md            # 專案說明文件
├── preview-linux.png        # Linux 平台執行畫面截圖
├── preview-macos.png        # macOS 平台執行畫面截圖
├── preview-windows.png      # Windows 平台執行畫面截圖
├── requirements.txt         # 依賴宣告（無）
├── LICENSE                  # MIT 授權條款
└── .gitignore               # Git 忽略規則
```

## 原始碼說明

`src/main.py` 是唯一的原始碼檔案，內容如下：

```python
#!/usr/bin/env python
print('Hello, ' + "World!")
```

- `#!/usr/bin/env python` — Shebang 行，指定使用系統預設 Python 直譯器執行
- `print('Hello, ' + "World!")` — 使用字串串接輸出 `Hello, World!`

## 常見問題

### Python 2 能執行嗎？

可以。`print('Hello, ' + "World!")` 在 Python 2.6+ 中同樣有效——括號在此處僅作為表達式分組，不會被當作函式呼叫。

### 執行時出現 `No such file or directory`

請確認目前工作目錄在專案根目錄下，並使用 `python src/main.py` 而非 `python main.py`。

## 相關文件

| 文件 | 說明 |
|------|------|
| [快速入門指南](docs/zh-Hant/getting-started.md) | 從零開始執行專案 |
| [架構設計文件](docs/zh-Hant/architecture.md) | 系統架構與資料流 |
| [API 參考文件](docs/zh-Hant/api.md) | 函式與操作說明 |
| [常見問題](docs/zh-Hant/faq.md) | FAQ |
| [疑難排解指南](docs/zh-Hant/troubleshooting.md) | 錯誤訊息速查與排查 |

## 有趣的事實

- `main.py` 只有 **2 行**，所有語言的文件加起來共 **1659 行** — 文件是程式碼的 **829.5 倍**。

| 檔案 | 行數 |
|------|-----:|
| `README.md` | 125 |
| `README.zh-Hans.md` | 125 |
| `README.zh-Hant.md` | 125 |

## 授權條款

本專案基於 MIT 授權條款開源 — 詳見 [LICENSE](LICENSE) 了解詳情。
