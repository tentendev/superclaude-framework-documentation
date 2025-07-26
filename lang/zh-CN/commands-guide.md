# SuperClaude 命令指南 🛠️

## 💡 不要想太多 - SuperClaude 会尝试帮助

**关于这 17 个命令的真相**：您不需要记住它们。只需从 `/sc:analyze` 或 `/sc:implement` 开始，看看会发生什么！

**通常的工作方式：**
- 在 Claude Code 中输入 `/` → 查看可用命令
- 使用基本命令如 `/sc:analyze`、`/sc:build`、`/sc:improve`
- **SuperClaude 会尝试为每种情况选择有用的工具和专家**
- 随着您的习惯，更多命令会变得有用

**自动激活相当不错** 🪄 - SuperClaude 尝试检测您正在尝试做的事情，并在不需要您管理的情况下激活相关专家（安全专家、性能优化器等）。通常运作良好！😊

---

## 快速「只需尝试这些」清单 🚀

**从这里开始**（无需阅读）：
```bash
/sc:index                    # 查看可用内容
/sc:analyze src/            # 尝试智能分析您的代码
/sc:workflow feature-100-prd.md  # 从 PRD 创建逐步实现工作流程
/sc:implement user-auth     # 创建功能和组件（替代 v2 /build）
/sc:build                   # 尝试智能项目构建
/sc:improve messy-file.js   # 尝试清理代码
/sc:troubleshoot "error"    # 尝试帮助解决问题
```

**这真的足以开始了。** 下面的所有内容都是当您对可用的其他工具感到好奇时提供的。🛠️

---

所有 16 个 SuperClaude 斜线命令的实用指南。我们会诚实地说明什么运作良好，什么仍然有些粗糙。

## 快速参考 📋

*（您真的不需要记住这个 - 只需选择听起来有用的）*

| 命令 | 目的 | 自动激活 | 最适合 |
|---------|---------|-----------------|----------|
| `/sc:analyze` | 智能代码分析 | 安全/性能专家 | 寻找问题、理解代码库 |
| `/sc:build` | 智能构建 | 前端/后端专家 | 编译、打包、部署准备 |
| `/sc:implement` | 功能实现 | 领域特定专家 | 创建功能、组件、API、服务 |
| `/sc:improve` | 自动代码清理 | 质量专家 | 重构、优化、质量修复 |
| `/sc:troubleshoot` | 问题调查 | 调试专家 | 调试、问题调查 |
| `/sc:test` | 智能测试 | QA 专家 | 运行测试、覆盖率分析 |
| `/sc:document` | 自动文档 | 写作专家 | README 文件、代码注释、指南 |
| `/sc:git` | 增强 git 工作流程 | DevOps 专家 | 智能提交、分支管理 |
| `/sc:design` | 系统设计帮助 | 架构专家 | 架构规划、API 设计 |
| `/sc:explain` | 学习助手 | 教学专家 | 学习概念、理解代码 |
| `/sc:cleanup` | 债务减少 | 重构专家 | 移除死代码、组织文件 |
| `/sc:load` | 上下文理解 | 分析专家 | 项目分析、代码库理解 |
| `/sc:estimate` | 智能估算 | 规划专家 | 时间/努力规划、复杂性分析 |
| `/sc:spawn` | 复杂工作流程 | 协调系统 | 多步骤操作、工作流程自动化 |
| `/sc:task` | 项目管理 | 规划系统 | 长期功能规划、任务跟踪 |
| `/sc:workflow` | 实现规划 | 工作流程系统 | 从 PRD 创建逐步工作流程 |
| `/sc:index` | 命令导航 | 帮助系统 | 为您的任务寻找正确的命令 |

**专业提示**：只需尝试听起来有用的。SuperClaude 通常会尝试为每种情况激活有用的专家和工具！🎯

## 开发命令 🔨

### `/workflow` - 实现工作流程生成器 🗺️
**功能**：分析 PRD 和功能需求，创建全面的逐步实现工作流程。

**有用的部分**：接受您的 PRD 并将其分解为结构化的实现计划，包含专家指导、依赖映射和任务协调！🎯

**何时使用**：
- 从 PRD 或规格开始新功能
- 需要清晰的实现路线图
- 想要实现策略的专家指导
- 规划具有多个依赖项的复杂功能

**魔法**：根据您的功能需求自动激活适当的专家角色（架构师、安全、前端、后端）和 MCP 服务器（Context7 用于模式、Sequential 用于复杂分析）。

**示例**：
```bash
/sc:workflow docs/feature-100-prd.md --strategy systematic --c7 --sequential
/sc:workflow "user authentication system" --persona security --output detailed
/sc:workflow payment-api --strategy mvp --risks --dependencies
```

**您得到的**：
- **路线图格式**：基于阶段的实现计划与时间线
- **任务格式**：组织的史诗、故事和可行动任务
- **详细格式**：逐步指示与时间估算
- **风险评估**：潜在问题和缓解策略
- **依赖映射**：内部和外部依赖项
- **专家指导**：领域特定的最佳实践和模式

### `/implement` - 功能实现
**功能**：实现功能、组件和功能，具有智能专家激活。

**有用的部分**：SuperClaude 根据您正在实现的内容自动激活正确的专家（前端、后端、安全）和工具！🎯

**何时使用**：
- 创建新功能或组件（替代 v2 的 `/build` 功能）
- 实现 API、服务或模块
- 使用现代框架构建 UI 组件
- 开发业务逻辑和集成

**基本语法**：
```bash
/sc:implement user authentication system      # 实现完整功能
/sc:implement --type component LoginForm      # 创建特定组件
/sc:implement --type api user-management      # 构建 API 端点
/sc:implement --framework react dashboard     # 框架特定实现
```

**有用的标志**：
- `--type component|api|service|feature|module` - 实现类型
- `--framework react|vue|express|django|etc` - 目标框架
- `--safe` - 保守实现方法
- `--iterative` - 逐步开发与验证
- `--with-tests` - 包含测试实现
- `--documentation` - 与代码一起生成文档

**实际示例**：
```bash
/sc:implement user authentication --type feature --with-tests
/sc:implement dashboard component --type component --framework react
/sc:implement REST API for orders --type api --safe
/sc:implement payment processing --type service --iterative
/sc:implement search functionality --framework vue --documentation
```

**自动激活模式**：
- **前端**：UI 组件、React/Vue/Angular → 前端角色 + Magic MCP
- **后端**：API、服务、数据库 → 后端角色 + Context7
- **安全**：认证、支付、敏感数据 → 安全角色 + 验证
- **复杂功能**：多步骤实现 → Sequential MCP + 架构师角色

---

### `/build` - 项目构建
**功能**：使用智能错误处理构建、编译和打包项目。

**简单方法**：只需输入 `/sc:build`，SuperClaude 会尝试弄清楚您的构建系统！🎯

**何时使用**：
- 您需要编译/打包您的项目（只需尝试 `/sc:build`）
- 构建过程失败，您想要帮助调试
- 设置构建优化（它会尝试检测您需要什么）
- 为部署做准备

**基本语法**：
```bash
/sc:build                          # 构建当前项目
/sc:build --type prod              # 生产构建
/sc:build --clean                  # 清理构建（移除旧文件）
/sc:build --optimize               # 启用优化
/sc:build src/                     # 构建特定目录
```

**有用的标志**：
- `--type dev|prod|test` - 构建类型
- `--clean` - 构建前清理
- `--optimize` - 启用构建优化
- `--verbose` - 显示详细构建输出

**实际示例**：
```bash
/sc:build --type prod --optimize   # 生产构建与优化
/sc:build --clean --verbose        # 清理构建与详细输出
/sc:build src/components           # 只构建组件文件夹
```

**注意事项**：
- 最适合常见构建工具（npm、webpack 等）
- 可能会在非常自定义的构建设置上有困难
- 检查您的构建工具是否在 PATH 中