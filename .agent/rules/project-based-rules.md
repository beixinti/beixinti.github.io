---
trigger: always_on
---

# Project basic rule

## 基本信息
这是一个基于 Alpine.js + Pico.css 的轻量级单页面（SPA）工具箱项目。 核心理念： 极简主义、零构建流程（No-Build）、引入即用。

## Rules
- 样式优先：严禁手写复杂 CSS。必须优先利用 Pico.css 的语义化 HTML 标签自动美化功能。
- 逻辑优先：优先使用 Alpine.js 的行内指令（如 x-data, x-on）处理简单逻辑，保持代码直观可见。
- 组件规范：所有的 UI 交互（如弹窗、选项卡）应优先参考 Pico.css 官方文档的 HTML 结构实现。

## 工作流程自动匹配
系统根据任务类型自动匹配以下流程：
- UI 视觉与布局修改： 匹配 ui-worker (负责 HTML 结构与 Pico 样式调优)。
- 交互逻辑与数据处理： 匹配 logic-worker (负责 Alpine.js 声明式逻辑开发)。

### 文件拆分说明
为了保证读取和操作的效率，一些文件按功能拆分成了子文件，请在需要的时候按标注位置读取子文件

### 核心项目文件
- 以下文件以项目根目录为基础展示路径
- `documents/PRD.md` - 产品需求文档，定义所有功能模块和技术要求

### 项目文件结构
/project-root
├── documents/          # 需求文档 (PRD.md) 与结构说明
├── design_drafts/      # 静态设计草图 (纯 HTML/Pico 样式实验)
└── app/                # 核心应用目录
    ├── index.html      # 入口文件 (在此引入 Pico 和 Alpine)
    └── js/             # 存放可选的外部逻辑脚本