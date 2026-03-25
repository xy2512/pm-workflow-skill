# HTML 页面设计规范

本文档定义了 PM Flow 产出物（PRD 和原型）的统一视觉设计规范。

---

## 配色方案

### 主色系

| 用途 | 色值 | 预览 |
|---|---|---|
| 主色 (Primary) | `#2563EB` | 🟦 蓝色 |
| 主色悬停 | `#1D4ED8` | 🟦 深蓝 |
| 成功 (Success) | `#10B981` | 🟩 绿色 |
| 警告 (Warning) | `#F59E0B` | 🟨 橙色 |
| 错误 (Error) | `#EF4444` | 🟥 红色 |

### 中性色

| 用途 | 色值 |
|---|---|
| 页面背景 | `#F8FAFC` |
| 卡片背景 | `#FFFFFF` |
| 主文字 | `#1E293B` |
| 副文字 | `#64748B` |
| 辅助文字 | `#94A3B8` |
| 边框 | `#E2E8F0` |
| 分割线 | `#F1F5F9` |

---

## 字体规范

| 层级 | 字号 | 字重 | 行高 | 用途 |
|---|---|---|---|---|
| H1 | 28px | Bold (700) | 1.3 | 页面标题 |
| H2 | 22px | Semibold (600) | 1.4 | 章节标题 |
| H3 | 18px | Semibold (600) | 1.4 | 模块标题 |
| H4 | 16px | Medium (500) | 1.5 | 子标题 |
| Body | 14px | Regular (400) | 1.6 | 正文 |
| Caption | 12px | Regular (400) | 1.5 | 辅助说明 |

**字体族**：`-apple-system, BlinkMacSystemFont, 'Segoe UI', 'PingFang SC', 'Hiragino Sans GB', 'Microsoft YaHei', sans-serif`

---

## 间距规范

| 名称 | 数值 | 用途 |
|---|---|---|
| xs | 4px | 图标与文字间距 |
| sm | 8px | 紧凑元素间距 |
| md | 16px | 卡片内间距 |
| lg | 24px | 章节间距 |
| xl | 32px | 大区块间距 |
| 2xl | 48px | 页面顶部/底部间距 |

---

## 布局规范

### PRD 页面布局

```
┌──────────────────────────────────────────────┐
│  Header: 产品名 | 版本号 | 版本切换菜单        │
├──────────┬───────────────────────────────────┤
│          │                                   │
│  TOC     │  Content Area                     │
│  导航栏  │  (max-width: 900px, 居中)          │
│  (fixed) │                                   │
│  220px   │                                   │
│          │                                   │
│          │                                   │
│          │                                   │
│          │                                   │
│          │                                   │
└──────────┴───────────────────────────────────┘
```

- TOC 导航栏：固定定位（`position: fixed`），左侧 220px 宽度
- 内容区域：`margin-left: 220px; max-width: 900px; padding: 48px 32px;`
- 滚动时 TOC 高亮当前章节

### 移动端响应式

- 屏幕宽度 < 768px 时，TOC 收起为汉堡菜单
- 内容区域全宽，左右 padding 16px
- 表格支持横向滚动

---

## 组件规范

### 表格

- 表头背景：`#F1F5F9`，文字 13px Medium，颜色 `#475569`
- 单元格内边距：`10px 16px`
- 奇偶行交替：偶数行背景 `#FAFBFC`
- 边框：仅水平边框，颜色 `#E2E8F0`

### 代码块

- 背景：`#1E293B`
- 文字：`#E2E8F0`，14px 等宽字体
- 内边距：`16px 20px`
- 圆角：`8px`

### 引用块

- 左边框：`3px solid #2563EB`
- 背景：`#EFF6FF`
- 文字颜色：`#1E40AF`
- 内边距：`12px 16px`

### 标签/Badge

- P0：`#EF4444` 红色背景，白色文字
- P1：`#F59E0B` 橙色背景，白色文字
- P2：`#94A3B8` 灰色背景，白色文字

### 功能模块卡片

- 白色背景，圆角 `12px`
- 阴影：`0 1px 3px rgba(0,0,0,0.1)`
- 内边距：`24px`
- 标题区底部有 `2px solid #E2E8F0` 分割线

---

## Tailwind CSS CDN 引用

在 HTML 文件的 `<head>` 中添加：

```html
<script src="https://cdn.tailwindcss.com"></script>
```

如需自定义配色：

```html
<script>
  tailwind.config = {
    theme: {
      extend: {
        colors: {
          primary: '#2563EB',
          'primary-hover': '#1D4ED8',
        }
      }
    }
  }
</script>
```
