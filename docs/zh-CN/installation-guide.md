# SuperClaude 安装指南 📦

## 🎯 其实没有看起来那么复杂！

**实话实说**：这份指南看起来很长，是因为我们想涵盖所有细节，但安装其实非常简单。大多数人只需要一个命令，2分钟就能完成！

### 步骤 1：安装包

**选项 A：从 PyPI 安装（推荐）**
```bash
uv add SuperClaude
```

**选项 B：从源代码安装**
```bash
git clone https://github.com/NomenAK/SuperClaude.git
cd SuperClaude
uv sync
```

### 🔧 UV / UVX 设置指南

SuperClaude v3 也支持通过 [`uv`](https://github.com/astral-sh/uv)（更快、更现代的 Python 包管理器）或 `uvx` 进行跨平台安装。

### 🌀 使用 `uv` 安装

确保已安装 `uv`：

```bash
curl -Ls https://astral.sh/uv/install.sh | sh
```

> 或者参考：[https://github.com/astral-sh/uv](https://github.com/astral-sh/uv)

当 `uv` 可用后，您可以这样安装 SuperClaude：

```bash
uv venv
source .venv/bin/activate
uv pip install SuperClaude
```

### ⚡ 使用 `uvx` 安装（跨平台 CLI）

如果您使用 `uvx`，只需执行：

```bash
uvx pip install SuperClaude
```

### ✅ 完成安装

安装后，继续执行常规的安装程序步骤：

```bash
python3 -m SuperClaude install
```

或使用 bash 风格的 CLI：

```bash
SuperClaude install
```

### 🧠 注意：

* `uv` 提供更好的缓存和性能
* 兼容 Python 3.8+ 并与 SuperClaude 完美配合

---

### ⚠️ 重要提示
**安装 SuperClaude 后，**
**您可以使用 `SuperClaude commands`、`python3 -m SuperClaude commands` 或 `python3 SuperClaude commands`**

**刚才发生了什么？** SuperClaude 尝试设置您需要的一切。通常不需要复杂的配置、寻找依赖项或设置烦恼！🎉

---

这是 SuperClaude v3 的完整安装指南。但请记住 - 大多数人根本不需要阅读快速开始以外的内容！😊

## 开始之前 🔍

### 您需要什么 💻

SuperClaude 可在 **Windows**、**macOS** 和 **Linux** 上运行。以下是您需要的：

**必需：**
- **Python 3.8 或更新版本** - 框架使用 Python 编写
- **Claude CLI** - SuperClaude 增强 Claude Code，所以您需要先安装它

**可选（但建议）：**
- **Node.js 16+** - 只有在您想要 MCP 服务器集成时才需要
- **Git** - 有助于开发工作流程

### 快速检查 🔍

在安装之前，让我们确保您具备基本条件：

```bash
# 检查 Python 版本（应为 3.8+）
python3 --version

# 检查是否已安装 Claude CLI
claude --version

# 检查 Node.js（可选，用于 MCP 服务器）
node --version
```

如果有任何失败，请参阅下方的[先决条件设置](#先决条件设置-🛠️)部分。

## 快速开始 🚀

**🏆「就是要能用」的方法（推荐给 90% 的用户）**

**选项 A：从 PyPI 安装（推荐）**
```bash
pip install SuperClaude

# 使用推荐设置安装
SuperClaude install --quick

# 就这样！🎉
```

**选项 B：从源代码安装**
```bash
# 克隆仓库
git clone <repository-url>
cd SuperClaude
pip install .

# 使用推荐设置安装
SuperClaude install --quick

# 就这样！🎉
```

**⚠️ 重要提示**
**安装 SuperClaude 后，**
**您可以使用 `SuperClaude commands`、`python3 -m SuperClaude commands` 或 `python3 SuperClaude commands`**

**您刚刚获得了什么：**
- ✅ 所有 16 个智能命令，自动激活专家
- ✅ 11 个专业人格，知道何时提供帮助
- ✅ 智能路由，自动判断复杂度
- ✅ 只花了您约 2 分钟时间和 ~50MB 磁盘空间

**真的，您已经完成了。** 打开 Claude Code，输入 `/help`，然后看着 SuperClaude 施展魔法。

**担心它会做什么？** 先看看会发生什么：
```bash
SuperClaude install --quick --dry-run
```

## 安装选项 🎯

我们提供三种安装配置文件供您选择：

### 🎯 最小安装
```bash
SuperClaude install --minimal
```
- **内容**：只有核心框架文件
- **时间**：~1 分钟
- **空间**：~20MB
- **适合**：测试、基本增强、最小设置
- **包含**：引导 Claude 的核心行为文档

### 🚀 快速安装（推荐）
```bash
SuperClaude install --quick
```
- **内容**：核心框架 + 16 个斜杠命令
- **时间**：~2 分钟
- **空间**：~50MB
- **适合**：大多数用户、一般开发
- **包含**：最小安装的所有内容 + 专门命令如 `/analyze`、`/build`、`/improve`

### 🔧 开发者安装
```bash
SuperClaude install --profile developer
```
- **内容**：包含 MCP 服务器集成的所有内容
- **时间**：~5 分钟
- **空间**：~100MB
- **适合**：高级用户、贡献者、高级工作流程
- **包含**：所有内容 + Context7、Sequential、Magic、Playwright 服务器

### 🎛️ 交互式安装
```bash
SuperClaude install
```
- 让您挑选和选择组件
- 显示每个组件功能的详细说明
- 如果您想要控制安装内容，这是好选择

## 逐步安装 📋

### 先决条件设置 🛠️

**缺少 Python？**
```bash
# Linux (Ubuntu/Debian)
sudo apt update && sudo apt install python3 python3-pip

# macOS
brew install python3

# Windows
# 从 https://python.org/downloads/ 下载
# 或打开命令提示符或 PowerShell
winget install python
```

**缺少 Claude CLI？**
- 访问 https://claude.ai/code 查看安装说明
- SuperClaude 增强 Claude Code，所以您需要先安装它

**缺少 Node.js？（可选）**
```bash
# Linux (Ubuntu/Debian)
sudo apt update && sudo apt install nodejs npm

# macOS
brew install node

# Windows
# 从 https://nodejs.org/ 下载
# 或打开命令提示符或 PowerShell
winget install nodejs
```

### 获取 SuperClaude 📥

**选项 1：从 PyPI 安装（推荐）**
```bash
pip install SuperClaude
```

**选项 2：下载最新版本**
```bash
# 下载并解压最新版本
# （将 URL 替换为实际的发布 URL）
curl -L <release-url> -o superclaude-v3.zip
unzip superclaude-v3.zip
cd superclaude-v3
pip install .
```

**选项 3：从 Git 克隆**
```bash
git clone <repository-url>
cd SuperClaude
pip install .
```

### 运行安装程序 🎬

安装程序相当智能，会引导您完成整个过程：

```bash
# 查看所有可用选项
SuperClaude install --help

# 快速安装（推荐）
SuperClaude install --quick

# 想先看看会发生什么？
SuperClaude install --quick --dry-run

# 安装所有内容
SuperClaude install --profile developer

# 静默安装（最少输出）
SuperClaude install --quick --quiet

# 强制安装（跳过确认）
python3 SuperClaude.py install --quick --force
```

### 安装期间 📱

以下是安装时会发生的事情：

1. **系统检查** - 验证您有必需的依赖项
2. **目录设置** - 创建 `~/.claude/` 目录结构
3. **核心文件** - 复制框架文档文件
4. **命令** - 安装斜杠命令定义（如果选择）
5. **MCP 服务器** - 下载并配置 MCP 服务器（如果选择）
6. **配置** - 使用您的偏好设置 `settings.json`
7. **验证** - 测试一切是否正常工作

安装程序会显示进度，如果出现任何问题会告诉您。

## 安装后 ✅

### 快速测试 🧪

让我们确保一切正常工作：

```bash
# 检查文件是否已安装
ls ~/.claude/

# 应该显示：CLAUDE.md、COMMANDS.md、settings.json 等
```

**使用 Claude Code 测试：**
1. 打开 Claude Code
2. 尝试输入 `/help` - 您应该看到 SuperClaude 命令
3. 尝试 `/analyze --help` - 应该显示命令选项

### 安装了什么 📂

SuperClaude 默认安装到 `~/.claude/`。以下是您会找到的内容：

```
~/.claude/
├── CLAUDE.md              # 主框架入口点
├── COMMANDS.md            # 可用的斜杠命令
├── FLAGS.md               # 命令标志和选项
├── PERSONAS.md            # 智能人格系统
├── PRINCIPLES.md          # 开发原则
├── RULES.md               # 操作规则
├── MCP.md                 # MCP 服务器集成
├── MODES.md               # 操作模式
├── ORCHESTRATOR.md        # 智能路由
├── settings.json          # 配置文件
└── commands/              # 单独的命令定义
    ├── analyze.md
    ├── build.md
    ├── improve.md
    └── ... （还有 13 个）
```

**每个文件的功能：**
- **CLAUDE.md** - 告诉 Claude Code 关于 SuperClaude 并加载其他文件
- **settings.json** - 配置（MCP 服务器、钩子等）
- **commands/** - 每个斜杠命令的详细定义

### 第一步 🎯

尝试这些命令来开始：

```bash
# 在 Claude Code 中，尝试这些：
/sc:help                    # 查看可用命令
/sc:analyze README.md       # 分析文件
/sc:build --help           # 查看构建选项
/sc:improve --help         # 查看改进选项
```

**如果感到不知所措，不要担心** - SuperClaude 会逐渐增强 Claude Code。您可以根据需要使用多少或少量功能。

## 管理您的安装 🛠️

### 更新 📅

保持 SuperClaude 最新：

```bash
# 检查更新
SuperClaude update

# 强制更新（覆盖本地更改）
SuperClaude update --force

# 只更新特定组件
SuperClaude update --components core,commands

# 查看会更新什么
SuperClaude update --dry-run
```

**何时更新：**
- 当新的 SuperClaude 版本发布时
- 如果您遇到问题（更新通常包含修复）
- 当新的 MCP 服务器可用时

### 备份 💾

在重大更改之前创建备份：

```bash
# 创建备份
SuperClaude backup --create

# 列出现有备份
SuperClaude backup --list

# 从备份恢复
SuperClaude backup --restore

# 使用自定义名称创建备份
SuperClaude backup --create --name "before-update"
```

**何时备份：**
- 更新 SuperClaude 之前
- 实验设置之前
- 卸载之前
- 如果您大量自定义，定期备份

### 卸载 🗑️

如果您需要移除 SuperClaude：

```bash
# 移除 SuperClaude（保留备份）
SuperClaude uninstall

# 完全移除（移除所有内容）
SuperClaude uninstall --complete

# 查看会移除什么
SuperClaude uninstall --dry-run
```

**会移除什么：**
- `~/.claude/` 中的所有文件
- MCP 服务器配置
- Claude Code 中的 SuperClaude 设置

**会保留什么：**
- 您的备份（除非您使用 `--complete`）
- Claude Code 本身（SuperClaude 不会碰它）
- 您的项目和其他文件

## 故障排除 🔧

### 常见问题 🚨

**「找不到 Python」**
```bash
# 尝试 python 而不是 python3
python --version

# 或检查是否已安装但不在 PATH 中
which python3
```

**「找不到 Claude CLI」**
- 确保先安装 Claude Code
- 尝试 `claude --version` 来验证
- 访问 https://claude.ai/code 获取安装帮助

**「权限被拒绝」**
```bash
# 尝试使用明确的 Python 路径
/usr/bin/python3 SuperClaude.py install --quick

# 或检查是否需要不同的权限
ls -la ~/.claude/
```

**「MCP 服务器无法安装」**
- 检查是否已安装 Node.js：`node --version`
- 检查 npm 是否可用：`npm --version`
- 先尝试不使用 MCP 安装：`--minimal` 或 `--quick`

**「安装中途失败」**
```bash
# 尝试使用详细输出来查看发生什么
SuperClaude install --quick --verbose

# 或先尝试模拟运行
SuperClaude install --quick --dry-run
```

### 平台特定问题 🖥️

**Windows：**
- 如果收到「找不到命令」，使用 `python` 而不是 `python3`
- 如果收到权限错误，以管理员身份运行命令提示符
- 确保 Python 在您的 PATH 中

**macOS：**
- 您可能需要在安全性与隐私设置中批准 SuperClaude
- 如果您没有 Python 3.8+，使用 `brew install python3`
- 尝试明确使用 `python3` 而不是 `python`

**Linux：**
- 确保您已安装 `python3-pip`
- 某些包安装可能需要 `sudo`
- 检查 `~/.local/bin` 是否在您的 PATH 中

### 仍有问题？🤔

**查看我们的故障排除资源：**
- GitHub Issues：https://github.com/NomenAK/SuperClaude/issues
- 寻找与您类似的现有问题
- 如果找不到解决方案，创建新问题

**报告错误时，请包含：**
- 您的操作系统和版本
- Python 版本（`python3 --version`）
- Claude CLI 版本（`claude --version`）
- 您执行的确切命令
- 完整的错误消息
- 您预期会发生什么

**获取帮助：**
- GitHub Discussions 用于一般问题
- 查看 README.md 获取最新更新
- 查看 ROADMAP.md 看看您的问题是否已知

## 高级选项 ⚙️

### 自定义安装目录

```bash
# 安装到自定义位置
SuperClaude install --quick --install-dir /custom/path

# 使用环境变量
export SUPERCLAUDE_DIR=/custom/path
SuperClaude install --quick
```

### 组件选择

```bash
# 查看可用组件
SuperClaude install --list-components

# 只安装特定组件
SuperClaude install --components core,commands

# 跳过某些组件
SuperClaude install --quick --skip mcp
```

### 开发设置

如果您计划贡献或修改 SuperClaude：

```bash
# 包含所有组件的开发者安装
SuperClaude install --profile developer

# 以开发模式安装（符号链接而非复制）
SuperClaude install --profile developer --dev-mode

# 为开发安装 git 钩子
SuperClaude install --profile developer --dev-hooks
```

## 接下来呢？🚀

**现在 SuperClaude 已安装（这很简单，对吧？）：**

1. **直接开始使用** - 尝试 `/analyze some-file.js` 或 `/build`，看看会发生什么 ✨
2. **不要担心学习** - SuperClaude 通常会自动判断您需要什么
3. **自由实验** - 像 `/improve` 和 `/troubleshoot` 这样的命令相当宽容
4. **如果好奇就阅读指南** - 当您想了解刚才发生了什么时，查看 `Docs/`
5. **提供反馈** - 让我们知道什么有效，什么无效

**真正的秘密**：SuperClaude 旨在增强您现有的工作流程，而无需您学习一堆新东西。就像使用普通的 Claude Code 一样使用它，但请注意它变得多么聪明！🎯

**仍然感到不确定？** 从 `/help` 和 `/analyze README.md` 开始 - 您会看到它实际上并不令人生畏。

---

## 最后说明 📝

- **安装需要 1-5 分钟**，取决于您选择的内容
- **所需磁盘空间：20-100MB**（不多！）
- **与现有工具一起工作** - 不会干扰您的设置
- **易于卸载**，如果您改变主意
- **社区支持** - 我们确实会阅读并回应问题
- ### ⚠️ 重要提示
**安装 SuperClaude 后，**
**您可以使用 `SuperClaude commands`、`python3 -m SuperClaude commands` 或 `python3 SuperClaude commands`**

感谢您尝试 SuperClaude！我们希望它能让您的开发工作流程更顺畅一些。🙂

---

*最后更新：2024年7月 - 如果本指南有任何错误或令人困惑的地方，请告诉我们！*