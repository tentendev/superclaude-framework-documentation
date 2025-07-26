# SuperClaude 安裝指南 📦

## 🎯 其實沒有看起來那麼複雜！

**實話實說**：這份指南看起來很長，是因為我們想涵蓋所有細節，但安裝其實非常簡單。大多數人只需要一個指令，2分鐘就能完成！

### 步驟 1：安裝套件

**選項 A：從 PyPI 安裝（推薦）**
```bash
uv add SuperClaude
```

**選項 B：從原始碼安裝**
```bash
git clone https://github.com/NomenAK/SuperClaude.git
cd SuperClaude
uv sync
```

### 🔧 UV / UVX 設定指南

SuperClaude v3 也支援透過 [`uv`](https://github.com/astral-sh/uv)（更快、更現代的 Python 套件管理器）或 `uvx` 進行跨平台安裝。

### 🌀 使用 `uv` 安裝

確保已安裝 `uv`：

```bash
curl -Ls https://astral.sh/uv/install.sh | sh
```

> 或者參考：[https://github.com/astral-sh/uv](https://github.com/astral-sh/uv)

當 `uv` 可用後，您可以這樣安裝 SuperClaude：

```bash
uv venv
source .venv/bin/activate
uv pip install SuperClaude
```

### ⚡ 使用 `uvx` 安裝（跨平台 CLI）

如果您使用 `uvx`，只需執行：

```bash
uvx pip install SuperClaude
```

### ✅ 完成安裝

安裝後，繼續執行一般的安裝程式步驟：

```bash
python3 -m SuperClaude install
```

或使用 bash 風格的 CLI：

```bash
SuperClaude install
```

### 🧠 注意：

* `uv` 提供更好的快取和效能
* 相容於 Python 3.8+ 並與 SuperClaude 完美配合

---

### ⚠️ 重要提示
**安裝 SuperClaude 後，**
**您可以使用 `SuperClaude commands`、`python3 -m SuperClaude commands` 或 `python3 SuperClaude commands`**

**剛才發生了什麼？** SuperClaude 嘗試設定您需要的一切。通常不需要複雜的配置、尋找相依套件或設定煩惱！🎉

---

這是 SuperClaude v3 的完整安裝指南。但請記住 - 大多數人根本不需要閱讀快速開始以外的內容！😊

## 開始之前 🔍

### 您需要什麼 💻

SuperClaude 可在 **Windows**、**macOS** 和 **Linux** 上運作。以下是您需要的：

**必需：**
- **Python 3.8 或更新版本** - 框架使用 Python 編寫
- **Claude CLI** - SuperClaude 增強 Claude Code，所以您需要先安裝它

**選用（但建議）：**
- **Node.js 16+** - 只有在您想要 MCP 伺服器整合時才需要
- **Git** - 有助於開發工作流程

### 快速檢查 🔍

在安裝之前，讓我們確保您具備基本條件：

```bash
# 檢查 Python 版本（應為 3.8+）
python3 --version

# 檢查是否已安裝 Claude CLI
claude --version

# 檢查 Node.js（選用，用於 MCP 伺服器）
node --version
```

如果有任何失敗，請參閱下方的[先決條件設定](#先決條件設定-🛠️)部分。

## 快速開始 🚀

**🏆「就是要能用」的方法（推薦給 90% 的使用者）**

**選項 A：從 PyPI 安裝（推薦）**
```bash
pip install SuperClaude

# 使用推薦設定安裝
SuperClaude install --quick

# 就這樣！🎉
```

**選項 B：從原始碼安裝**
```bash
# 複製儲存庫
git clone <repository-url>
cd SuperClaude
pip install .

# 使用推薦設定安裝
SuperClaude install --quick

# 就這樣！🎉
```

**⚠️ 重要提示**
**安裝 SuperClaude 後，**
**您可以使用 `SuperClaude commands`、`python3 -m SuperClaude commands` 或 `python3 SuperClaude commands`**

**您剛剛獲得了什麼：**
- ✅ 所有 16 個智慧指令，自動啟用專家
- ✅ 11 個專業人格，知道何時提供協助
- ✅ 智慧路由，自動判斷複雜度
- ✅ 只花了您約 2 分鐘時間和 ~50MB 磁碟空間

**真的，您已經完成了。** 開啟 Claude Code，輸入 `/help`，然後看著 SuperClaude 施展魔法。

**擔心它會做什麼？** 先看看會發生什麼：
```bash
SuperClaude install --quick --dry-run
```

## 安裝選項 🎯

我們提供三種安裝配置檔供您選擇：

### 🎯 最小安裝
```bash
SuperClaude install --minimal
```
- **內容**：只有核心框架檔案
- **時間**：~1 分鐘
- **空間**：~20MB
- **適合**：測試、基本增強、最小設定
- **包含**：引導 Claude 的核心行為文件

### 🚀 快速安裝（推薦）
```bash
SuperClaude install --quick
```
- **內容**：核心框架 + 16 個斜線指令
- **時間**：~2 分鐘
- **空間**：~50MB
- **適合**：大多數使用者、一般開發
- **包含**：最小安裝的所有內容 + 專門指令如 `/analyze`、`/build`、`/improve`

### 🔧 開發者安裝
```bash
SuperClaude install --profile developer
```
- **內容**：包含 MCP 伺服器整合的所有內容
- **時間**：~5 分鐘
- **空間**：~100MB
- **適合**：進階使用者、貢獻者、進階工作流程
- **包含**：所有內容 + Context7、Sequential、Magic、Playwright 伺服器

### 🎛️ 互動式安裝
```bash
SuperClaude install
```
- 讓您挑選和選擇元件
- 顯示每個元件功能的詳細說明
- 如果您想要控制安裝內容，這是好選擇

## 逐步安裝 📋

### 先決條件設定 🛠️

**缺少 Python？**
```bash
# Linux (Ubuntu/Debian)
sudo apt update && sudo apt install python3 python3-pip

# macOS
brew install python3

# Windows
# 從 https://python.org/downloads/ 下載
# 或開啟命令提示字元或 PowerShell
winget install python
```

**缺少 Claude CLI？**
- 前往 https://claude.ai/code 查看安裝說明
- SuperClaude 增強 Claude Code，所以您需要先安裝它

**缺少 Node.js？（選用）**
```bash
# Linux (Ubuntu/Debian)
sudo apt update && sudo apt install nodejs npm

# macOS
brew install node

# Windows
# 從 https://nodejs.org/ 下載
# 或開啟命令提示字元或 PowerShell
winget install nodejs
```

### 取得 SuperClaude 📥

**選項 1：從 PyPI 安裝（推薦）**
```bash
pip install SuperClaude
```

**選項 2：下載最新版本**
```bash
# 下載並解壓縮最新版本
# （將 URL 替換為實際的發布 URL）
curl -L <release-url> -o superclaude-v3.zip
unzip superclaude-v3.zip
cd superclaude-v3
pip install .
```

**選項 3：從 Git 複製**
```bash
git clone <repository-url>
cd SuperClaude
pip install .
```

### 執行安裝程式 🎬

安裝程式相當聰明，會引導您完成整個過程：

```bash
# 查看所有可用選項
SuperClaude install --help

# 快速安裝（推薦）
SuperClaude install --quick

# 想先看看會發生什麼？
SuperClaude install --quick --dry-run

# 安裝所有內容
SuperClaude install --profile developer

# 靜默安裝（最少輸出）
SuperClaude install --quick --quiet

# 強制安裝（跳過確認）
python3 SuperClaude.py install --quick --force
```

### 安裝期間 📱

以下是安裝時會發生的事情：

1. **系統檢查** - 驗證您有必需的相依套件
2. **目錄設定** - 建立 `~/.claude/` 目錄結構
3. **核心檔案** - 複製框架文件檔案
4. **指令** - 安裝斜線指令定義（如果選擇）
5. **MCP 伺服器** - 下載並配置 MCP 伺服器（如果選擇）
6. **配置** - 使用您的偏好設定 `settings.json`
7. **驗證** - 測試一切是否正常運作

安裝程式會顯示進度，如果出現任何問題會告訴您。

## 安裝後 ✅

### 快速測試 🧪

讓我們確保一切正常運作：

```bash
# 檢查檔案是否已安裝
ls ~/.claude/

# 應該顯示：CLAUDE.md、COMMANDS.md、settings.json 等
```

**使用 Claude Code 測試：**
1. 開啟 Claude Code
2. 嘗試輸入 `/help` - 您應該看到 SuperClaude 指令
3. 嘗試 `/analyze --help` - 應該顯示指令選項

### 安裝了什麼 📂

SuperClaude 預設安裝到 `~/.claude/`。以下是您會找到的內容：

```
~/.claude/
├── CLAUDE.md              # 主框架進入點
├── COMMANDS.md            # 可用的斜線指令
├── FLAGS.md               # 指令旗標和選項
├── PERSONAS.md            # 智慧人格系統
├── PRINCIPLES.md          # 開發原則
├── RULES.md               # 操作規則
├── MCP.md                 # MCP 伺服器整合
├── MODES.md               # 操作模式
├── ORCHESTRATOR.md        # 智慧路由
├── settings.json          # 配置檔案
└── commands/              # 個別指令定義
    ├── analyze.md
    ├── build.md
    ├── improve.md
    └── ... （還有 13 個）
```

**每個檔案的功能：**
- **CLAUDE.md** - 告訴 Claude Code 關於 SuperClaude 並載入其他檔案
- **settings.json** - 配置（MCP 伺服器、掛鉤等）
- **commands/** - 每個斜線指令的詳細定義

### 第一步 🎯

嘗試這些指令來開始：

```bash
# 在 Claude Code 中，嘗試這些：
/sc:help                    # 查看可用指令
/sc:analyze README.md       # 分析檔案
/sc:build --help           # 查看建構選項
/sc:improve --help         # 查看改進選項
```

**如果感到不知所措，不要擔心** - SuperClaude 會逐漸增強 Claude Code。您可以根據需要使用多少或少量功能。

## 管理您的安裝 🛠️

### 更新 📅

保持 SuperClaude 最新：

```bash
# 檢查更新
SuperClaude update

# 強制更新（覆蓋本地更改）
SuperClaude update --force

# 只更新特定元件
SuperClaude update --components core,commands

# 查看會更新什麼
SuperClaude update --dry-run
```

**何時更新：**
- 當新的 SuperClaude 版本發布時
- 如果您遇到問題（更新通常包含修復）
- 當新的 MCP 伺服器可用時

### 備份 💾

在重大更改之前建立備份：

```bash
# 建立備份
SuperClaude backup --create

# 列出現有備份
SuperClaude backup --list

# 從備份還原
SuperClaude backup --restore

# 使用自訂名稱建立備份
SuperClaude backup --create --name "before-update"
```

**何時備份：**
- 更新 SuperClaude 之前
- 實驗設定之前
- 解除安裝之前
- 如果您大量自訂，定期備份

### 解除安裝 🗑️

如果您需要移除 SuperClaude：

```bash
# 移除 SuperClaude（保留備份）
SuperClaude uninstall

# 完全移除（移除所有內容）
SuperClaude uninstall --complete

# 查看會移除什麼
SuperClaude uninstall --dry-run
```

**會移除什麼：**
- `~/.claude/` 中的所有檔案
- MCP 伺服器配置
- Claude Code 中的 SuperClaude 設定

**會保留什麼：**
- 您的備份（除非您使用 `--complete`）
- Claude Code 本身（SuperClaude 不會碰它）
- 您的專案和其他檔案

## 疑難排解 🔧

### 常見問題 🚨

**「找不到 Python」**
```bash
# 嘗試 python 而不是 python3
python --version

# 或檢查是否已安裝但不在 PATH 中
which python3
```

**「找不到 Claude CLI」**
- 確保先安裝 Claude Code
- 嘗試 `claude --version` 來驗證
- 前往 https://claude.ai/code 取得安裝協助

**「權限被拒絕」**
```bash
# 嘗試使用明確的 Python 路徑
/usr/bin/python3 SuperClaude.py install --quick

# 或檢查是否需要不同的權限
ls -la ~/.claude/
```

**「MCP 伺服器無法安裝」**
- 檢查是否已安裝 Node.js：`node --version`
- 檢查 npm 是否可用：`npm --version`
- 先嘗試不使用 MCP 安裝：`--minimal` 或 `--quick`

**「安裝中途失敗」**
```bash
# 嘗試使用詳細輸出來查看發生什麼
SuperClaude install --quick --verbose

# 或先嘗試模擬執行
SuperClaude install --quick --dry-run
```

### 平台特定問題 🖥️

**Windows：**
- 如果收到「找不到指令」，使用 `python` 而不是 `python3`
- 如果收到權限錯誤，以管理員身分執行命令提示字元
- 確保 Python 在您的 PATH 中

**macOS：**
- 您可能需要在安全性與隱私設定中核准 SuperClaude
- 如果您沒有 Python 3.8+，使用 `brew install python3`
- 嘗試明確使用 `python3` 而不是 `python`

**Linux：**
- 確保您已安裝 `python3-pip`
- 某些套件安裝可能需要 `sudo`
- 檢查 `~/.local/bin` 是否在您的 PATH 中

### 仍有問題？🤔

**查看我們的疑難排解資源：**
- GitHub Issues：https://github.com/NomenAK/SuperClaude/issues
- 尋找與您類似的現有問題
- 如果找不到解決方案，建立新問題

**報告錯誤時，請包含：**
- 您的作業系統和版本
- Python 版本（`python3 --version`）
- Claude CLI 版本（`claude --version`）
- 您執行的確切指令
- 完整的錯誤訊息
- 您預期會發生什麼

**取得協助：**
- GitHub Discussions 用於一般問題
- 查看 README.md 取得最新更新
- 查看 ROADMAP.md 看看您的問題是否已知

## 進階選項 ⚙️

### 自訂安裝目錄

```bash
# 安裝到自訂位置
SuperClaude install --quick --install-dir /custom/path

# 使用環境變數
export SUPERCLAUDE_DIR=/custom/path
SuperClaude install --quick
```

### 元件選擇

```bash
# 查看可用元件
SuperClaude install --list-components

# 只安裝特定元件
SuperClaude install --components core,commands

# 跳過某些元件
SuperClaude install --quick --skip mcp
```

### 開發設定

如果您計劃貢獻或修改 SuperClaude：

```bash
# 包含所有元件的開發者安裝
SuperClaude install --profile developer

# 以開發模式安裝（符號連結而非複製）
SuperClaude install --profile developer --dev-mode

# 為開發安裝 git 掛鉤
SuperClaude install --profile developer --dev-hooks
```

## 接下來呢？🚀

**現在 SuperClaude 已安裝（這很簡單，對吧？）：**

1. **直接開始使用** - 嘗試 `/analyze some-file.js` 或 `/build`，看看會發生什麼 ✨
2. **不要擔心學習** - SuperClaude 通常會自動判斷您需要什麼
3. **自由實驗** - 像 `/improve` 和 `/troubleshoot` 這樣的指令相當寬容
4. **如果好奇就閱讀指南** - 當您想了解剛才發生了什麼時，查看 `Docs/`
5. **提供回饋** - 讓我們知道什麼有效，什麼無效

**真正的秘密**：SuperClaude 旨在增強您現有的工作流程，而無需您學習一堆新東西。就像使用一般的 Claude Code 一樣使用它，但請注意它變得多麼聰明！🎯

**仍然感到不確定？** 從 `/help` 和 `/analyze README.md` 開始 - 您會看到它實際上並不令人生畏。

---

## 最後說明 📝

- **安裝需要 1-5 分鐘**，取決於您選擇的內容
- **所需磁碟空間：20-100MB**（不多！）
- **與現有工具一起運作** - 不會干擾您的設定
- **易於解除安裝**，如果您改變主意
- **社群支援** - 我們確實會閱讀並回應問題
- ### ⚠️ 重要提示
**安裝 SuperClaude 後，**
**您可以使用 `SuperClaude commands`、`python3 -m SuperClaude commands` 或 `python3 SuperClaude commands`**

感謝您嘗試 SuperClaude！我們希望它能讓您的開發工作流程更順暢一些。🙂

---

*最後更新：2024年7月 - 如果本指南有任何錯誤或令人困惑的地方，請告訴我們！*