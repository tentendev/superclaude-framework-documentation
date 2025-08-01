# 旗標指南：保持簡單

**重要提醒**：SuperClaude 的自動啟用功能運作良好！大多數情況下您不需要手動設定旗標。系統會根據您的需求自動選擇適當的工具和策略。

## 何時使用旗標

旗標就像是向 Claude 提供特定指示。雖然系統通常能夠理解您的需求，但有時候明確的指示會很有幫助：

- 當您想要特定的行為時（例如：「我需要超詳細的分析」）
- 當您想要覆蓋自動選擇時（例如：「這次不要使用 MCP 伺服器」）
- 當您有特定的效能需求時（例如：「保持簡潔」）

## 最實用的旗標

### 規劃與分析
- `--plan` - 執行前顯示執行計劃
- `--think` - 進行深入分析（約 4K tokens）
- `--think-hard` - 進行非常深入的分析（約 10K tokens）

### 效率與壓縮
- `--uc` / `--ultracompressed` - 使用更簡潔的回應（節省 30-50% tokens）
- `--answer-only` - 只提供答案，不建立任務或工作流程
- `--verbose` - 提供完整詳細的解釋

### MCP 伺服器控制
- `--no-mcp` - 停用所有 MCP 伺服器（加快 40-60% 速度）
- `--c7` - 啟用 Context7 來查詢文件
- `--seq` - 啟用 Sequential 進行複雜分析
- `--magic` - 啟用 Magic 生成 UI 元件

### 人格啟用
- `--persona-frontend` - UI/UX 專家模式
- `--persona-backend` - 後端與 API 專家模式
- `--persona-architect` - 系統架構專家模式
- `--persona-scribe=zh-TW` - 繁體中文專業寫作模式

## 常見模式

### 「我想要快速答案」
```
問題 --uc --answer-only
```

### 「幫我深入分析這個複雜問題」
```
/analyze 問題 --think-hard --seq
```

### 「建立 React 元件」
```
/build 元件名稱 --magic
```

### 「我不需要任何外部工具」
```
任務 --no-mcp --uc
```

## 記住：少即是多

SuperClaude 的自動偵測功能通常會做出正確的選擇。開始時不使用任何旗標，只在需要特定行為時才添加它們。

**專業提示**：如果您不確定，就讓系統自動處理。它真的很聰明！🎯