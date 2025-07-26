# SuperClaude 指令指南 🛠️

## 💡 不要想太多 - SuperClaude 會嘗試幫助

**關於這 17 個指令的真相**：您不需要記住它們。只需從 `/sc:analyze` 或 `/sc:implement` 開始，看看會發生什麼！

**通常的工作方式：**
- 在 Claude Code 中輸入 `/` → 查看可用指令
- 使用基本指令如 `/sc:analyze`、`/sc:build`、`/sc:improve`
- **SuperClaude 會嘗試為每種情況選擇有用的工具和專家**
- 隨著您的習慣，更多指令會變得有用

**自動啟動相當不錯** 🪄 - SuperClaude 嘗試檢測您正在嘗試做的事情，並在不需要您管理的情況下啟動相關專家（安全專家、效能最佳化器等）。通常運作良好！😊

---

## 快速「只需嘗試這些」清單 🚀

**從這裡開始**（無需閱讀）：
```bash
/sc:index                    # 查看可用內容
/sc:analyze src/            # 嘗試智慧分析您的程式碼
/sc:workflow feature-100-prd.md  # 從 PRD 建立逐步實作工作流程
/sc:implement user-auth     # 建立功能和元件（替代 v2 /build）
/sc:build                   # 嘗試智慧專案建構
/sc:improve messy-file.js   # 嘗試清理程式碼
/sc:troubleshoot "error"    # 嘗試幫助解決問題
```

**這真的足以開始了。** 下面的所有內容都是當您對可用的其他工具感到好奇時提供的。🛠️

---

所有 16 個 SuperClaude 斜線指令的實用指南。我們會誠實地說明什麼運作良好，什麼仍然有些粗糙。

## 快速參考 📋

*（您真的不需要記住這個 - 只需選擇聽起來有用的）*

| 指令 | 目的 | 自動啟動 | 最適合 |
|---------|---------|-----------------|----------|
| `/sc:analyze` | 智慧程式碼分析 | 安全/效能專家 | 尋找問題、理解程式碼庫 |
| `/sc:build` | 智慧建構 | 前端/後端專家 | 編譯、打包、部署準備 |
| `/sc:implement` | 功能實作 | 領域特定專家 | 建立功能、元件、API、服務 |
| `/sc:improve` | 自動程式碼清理 | 品質專家 | 重構、最佳化、品質修復 |
| `/sc:troubleshoot` | 問題調查 | 除錯專家 | 除錯、問題調查 |
| `/sc:test` | 智慧測試 | QA 專家 | 執行測試、覆蓋率分析 |
| `/sc:document` | 自動文件 | 寫作專家 | README 文件、程式碼註釋、指南 |
| `/sc:git` | 增強 git 工作流程 | DevOps 專家 | 智慧提交、分支管理 |
| `/sc:design` | 系統設計幫助 | 架構專家 | 架構規劃、API 設計 |
| `/sc:explain` | 學習助手 | 教學專家 | 學習概念、理解程式碼 |
| `/sc:cleanup` | 債務減少 | 重構專家 | 移除死程式碼、組織文件 |
| `/sc:load` | 上下文理解 | 分析專家 | 專案分析、程式碼庫理解 |
| `/sc:estimate` | 智慧估算 | 規劃專家 | 時間/努力規劃、複雜性分析 |
| `/sc:spawn` | 複雜工作流程 | 協調系統 | 多步驟操作、工作流程自動化 |
| `/sc:task` | 專案管理 | 規劃系統 | 長期功能規劃、任務追蹤 |
| `/sc:workflow` | 實作規劃 | 工作流程系統 | 從 PRD 建立逐步工作流程 |
| `/sc:index` | 指令導覽 | 幫助系統 | 為您的任務尋找正確的指令 |

**專業提示**：只需嘗試聽起來有用的。SuperClaude 通常會嘗試為每種情況啟動有用的專家和工具！🎯

## 開發指令 🔨

### `/workflow` - 實作工作流程生成器 🗺️
**功能**：分析 PRD 和功能需求，建立全面的逐步實作工作流程。

**有用的部分**：接受您的 PRD 並將其分解為結構化的實作計劃，包含專家指導、依賴映射和任務協調！🎯

**何時使用**：
- 從 PRD 或規格開始新功能
- 需要清晰的實作路線圖
- 想要實作策略的專家指導
- 規劃具有多個依賴項的複雜功能

**魔法**：根據您的功能需求自動啟動適當的專家角色（架構師、安全、前端、後端）和 MCP 伺服器（Context7 用於模式、Sequential 用於複雜分析）。

**範例**：
```bash
/sc:workflow docs/feature-100-prd.md --strategy systematic --c7 --sequential
/sc:workflow "user authentication system" --persona security --output detailed
/sc:workflow payment-api --strategy mvp --risks --dependencies
```

**您得到的**：
- **路線圖格式**：基於階段的實作計劃與時間線
- **任務格式**：組織的史詩、故事和可行動任務
- **詳細格式**：逐步指示與時間估算
- **風險評估**：潛在問題和緩解策略
- **依賴映射**：內部和外部依賴項
- **專家指導**：領域特定的最佳實踐和模式

### `/implement` - 功能實作
**功能**：實作功能、元件和功能，具有智慧專家啟動。

**有用的部分**：SuperClaude 根據您正在實作的內容自動啟動正確的專家（前端、後端、安全）和工具！🎯

**何時使用**：
- 建立新功能或元件（替代 v2 的 `/build` 功能）
- 實作 API、服務或模組
- 使用現代框架建構 UI 元件
- 開發業務邏輯和整合

**基本語法**：
```bash
/sc:implement user authentication system      # 實作完整功能
/sc:implement --type component LoginForm      # 建立特定元件
/sc:implement --type api user-management      # 建構 API 端點
/sc:implement --framework react dashboard     # 框架特定實作
```

**有用的標誌**：
- `--type component|api|service|feature|module` - 實作類型
- `--framework react|vue|express|django|etc` - 目標框架
- `--safe` - 保守實作方法
- `--iterative` - 逐步開發與驗證
- `--with-tests` - 包含測試實作
- `--documentation` - 與程式碼一起生成文件

**實際範例**：
```bash
/sc:implement user authentication --type feature --with-tests
/sc:implement dashboard component --type component --framework react
/sc:implement REST API for orders --type api --safe
/sc:implement payment processing --type service --iterative
/sc:implement search functionality --framework vue --documentation
```

**自動啟動模式**：
- **前端**：UI 元件、React/Vue/Angular → 前端角色 + Magic MCP
- **後端**：API、服務、資料庫 → 後端角色 + Context7
- **安全**：認證、付款、敏感資料 → 安全角色 + 驗證
- **複雜功能**：多步驟實作 → Sequential MCP + 架構師角色

---

### `/build` - 專案建構
**功能**：使用智慧錯誤處理建構、編譯和打包專案。

**簡單方法**：只需輸入 `/sc:build`，SuperClaude 會嘗試弄清楚您的建構系統！🎯

**何時使用**：
- 您需要編譯/打包您的專案（只需嘗試 `/sc:build`）
- 建構過程失敗，您想要幫助除錯
- 設定建構最佳化（它會嘗試檢測您需要什麼）
- 為部署做準備

**基本語法**：
```bash
/sc:build                          # 建構當前專案
/sc:build --type prod              # 生產建構
/sc:build --clean                  # 清理建構（移除舊文件）
/sc:build --optimize               # 啟用最佳化
/sc:build src/                     # 建構特定目錄
```

**有用的標誌**：
- `--type dev|prod|test` - 建構類型
- `--clean` - 建構前清理
- `--optimize` - 啟用建構最佳化
- `--verbose` - 顯示詳細建構輸出

**實際範例**：
```bash
/sc:build --type prod --optimize   # 生產建構與最佳化
/sc:build --clean --verbose        # 清理建構與詳細輸出
/sc:build src/components           # 只建構元件資料夾
```

**注意事項**：
- 最適合常見建構工具（npm、webpack 等）
- 可能會在非常自訂的建構設定上有困難
- 檢查您的建構工具是否在 PATH 中