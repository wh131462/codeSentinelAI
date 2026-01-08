# CodeSentinel AI Platform

> 基于 LLM 的智能研发效能与测试平台

CodeSentinel 是一个深度集成 GitLab 的智能研发效能平台，能够自动检测需求一致性、生成回归测试，并提供自愈修复方案。

## 核心功能

### 1. 文档智能 (Document Intelligence)
- PRD/API 文档自动解析与结构化
- 多维度文档质量评分（完整性、清晰度、可测性、一致性）
- AI 驱动的优化建议生成

### 2. 代码审查 (Code Review)
- 智能代码变更影响分析
- 安全漏洞、性能问题、代码规范自动检测
- 一键修复建议与补丁生成

### 3. 测试引擎 (Test Engine)
- 基于 PRD 自动生成测试用例
- Docker 沙箱隔离执行
- 覆盖率追踪与报告生成

### 4. 自动修复 (Auto-Fix)
- 根因分析 (RCA) 定位问题
- AI 生成修复补丁
- 自动验证修复效果

### 5. 洞察仪表盘 (Insights Dashboard)
- 全局质量趋势可视化
- 需求-代码追溯矩阵
- 团队效能指标分析

## 设计原型

本项目包含完整的设计原型系统，位于 `design/` 目录：

| 页面 | 文件 | 描述 |
|------|------|------|
| 首页 | `index.html` | 平台着陆页，项目快速入口 |
| 仪表盘 | `overview.html` | 全局数据概览、质量趋势图表 |
| 工作台 | `workspace.html` | 核心工作流程、AI 分析执行界面 |
| 需求映射 | `mapping.html` | 需求-代码追溯、覆盖率分析 |
| 流水线 | `pipeline.html` | 执行记录列表与详情查看 |
| 仓库配置 | `configuration.html` | Git 仓库连接配置 |
| PRD 评分 | `prd-score.html` | 文档质量 4 维度评分详情 |
| 测试报告 | `test-report.html` | 测试用例详情、覆盖率可视化 |
| 文档管理 | `documents.html` | 上传/管理需求文档 |
| 代码审查 | `code-review.html` | AI 代码审查结果详情 |
| 项目管理 | `projects.html` | 项目列表、健康状态监控 |
| 系统设置 | `settings.html` | 通用/AI/通知/集成/安全/团队设置 |

### 本地预览

直接在浏览器中打开 `design/index.html` 即可预览。

```bash
# macOS
open design/index.html

# Linux
xdg-open design/index.html

# Windows
start design/index.html
```

### 在线预览

访问 GitHub Pages: https://wh131462.github.io/codeSentinelAI/design/

## 技术栈

### 设计原型
- **React 18** - UI 组件库 (CDN)
- **Tailwind CSS** - 原子化 CSS 框架
- **Babel** - JSX 浏览器端编译

### 设计规范
- **主题**: 深色模式 (#000 背景)
- **主色**: Indigo (#6366f1)
- **辅助色**: Emerald (成功), Amber (警告), Rose (错误)
- **字体**: System UI 字体栈
- **图标**: 自定义 Lucide 风格 SVG 图标

## 目录结构

```
codeSentinelAI/
├── design/                    # 设计原型文件
│   ├── index.html            # 首页
│   ├── overview.html         # 仪表盘
│   ├── workspace.html        # 工作台
│   ├── mapping.html          # 需求映射
│   ├── pipeline.html         # 流水线
│   ├── configuration.html    # 仓库配置
│   ├── prd-score.html        # PRD 评分详情
│   ├── test-report.html      # 测试报告
│   ├── documents.html        # 文档管理
│   ├── code-review.html      # 代码审查
│   ├── projects.html         # 项目管理
│   └── settings.html         # 系统设置
├── .github/
│   └── workflows/
│       └── deploy-pages.yml  # GitHub Pages 部署配置
└── README.md                 # 项目说明文档
```

## 用户角色

平台支持三类核心用户角色：

| 角色 | 核心功能 | 典型场景 |
|------|---------|---------|
| **Dev** | 代码审查、自动修复、测试执行 | 提交代码后查看 AI 审查结果并应用修复 |
| **QA** | 测试报告、用例管理、覆盖率分析 | 查看自动生成的测试用例和执行报告 |
| **PM** | PRD 评分、需求追溯、文档管理 | 上传 PRD 并查看需求-代码覆盖情况 |

## 开发计划

- [x] 设计原型完成
- [ ] 后端 API 开发
- [ ] GitLab Webhook 集成
- [ ] LLM 模型接入
- [ ] Docker 沙箱环境搭建
- [ ] 生产环境部署

## 许可证

MIT License

---

**CodeSentinel** - 代码即需求，需求即代码
