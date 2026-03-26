# PM Flow — 从想法到交付的 AI 产品工作流

> 🚀 一站式敏捷产品经理工作流 Skill，基于 Claude Code / Cursor / Trae 等 AI IDE 使用。
> 从模糊想法到「竞品分析 + 高保真原型 + PRD」的完整交付链路。

## 特性

- **智能需求采集** — 六维雷达图评估 + 自适应追问，而非机械模板
- **竞品分析环节** — 自动生成竞品对比简报，避免闭门造车
- **高保真 HTML 原型** — Tailwind CSS + Focus 模式沙盒锁定
- **PRD 内嵌原型切片** — 通过 iframe 切片实现「所见即逻辑」的交互式文档
- **统一设计规范** — 配色、字体、间距、组件全部标准化
- **版本迭代管理** — 物理隔离 + 版本切换器 + 变更日志联动

## 八步工作流

```
需求发现 → 竞品分析 → 项目初始化 → 初版PRD → 原型设计 → 流程图 → 最终PRD → 版本管理
```

1. **需求发现** — 六维雷达评估 + 自适应深度追问
2. **竞品分析** — 竞品对比简报 + 市场验证建议
3. **项目初始化** — 标准化目录架构搭建
4. **初版 PRD** — 详细 HTML 格式，包含用户旅程和功能清单
5. **原型设计** — 高保真单文件 HTML，Focus 模式支持
6. **流程图** — Mermaid 语法，含异常分支和时序图
7. **最终 PRD** — 内嵌原型切片的完整交互式文档
8. **版本管理** — 多版本隔离 + 版本切换器

## 安装

### 方式一：npx skills（推荐）

```bash
npx skills add xy2512/pm-workflow-skill -g
```

### 方式二：手动安装

1. 克隆仓库：
```bash
git clone https://github.com/xy2512/pm-workflow-skill.git
```

2. 复制 `pm-flow/` 文件夹到你的 IDE skills 目录：

| IDE | 路径 |
|---|---|
| Claude Code | `~/.claude/skills/pm-flow/` |
| Trae / Cursor | `~/.trae/skills/pm-flow/` |
| WorkBuddy | `{workspace}/.workbuddy/skills/pm-flow/` |

## 文件结构

```
pm-flow/
├── SKILL.md                              # 核心指令文件
├── references/
│   ├── prd_structure.md                  # PRD 完整章节规范
│   ├── html_design_spec.md               # HTML 页面设计规范
│   └── competitive_analysis_template.md  # 竞品分析模板
└── assets/
    └── prd_template.html                 # HTML PRD 基础模板
```

## 使用方式

安装后，在 AI 对话框中描述你的产品想法，Skill 会自动触发并引导你完成全流程。

示例触发语：
- 「我想做一个装修工人打卡小程序」
- 「帮我梳理一个外卖配送后台的需求」
- 「我需要做一个企业内部的知识库系统」


## License

MIT
