# 快速开始

## 前提条件

- [Claude Code](https://claude.ai/code) CLI 已安装
- Node.js 18+ 已安装

## 步骤

### 1. Clone 项目

```bash
git clone <repo-url> yuer-skill
cd yuer-skill
```

### 2. 安装 Web 依赖

```bash
cd web
npm install
cd ..
```

### 3. 开始使用

在项目根目录启动 Claude Code：

```bash
claude
```

输入 `/yuer` 进入日常指导模式，或输入 `/yuer-ask 你遇到的育儿问题` 提问。

**首次使用**：系统会通过对话了解你的孩子，自动建立档案。你只需要像聊天一样回答问题，不需要手动填写任何文件。

### 4. 查看数据（可选）

启动 Web 页面查看可视化的孩子档案和建议追踪：

```bash
cd web
npm run dev
```

浏览器访问 `http://localhost:4321`

## 命令说明

| 命令 | 用途 |
|------|------|
| `/yuer` | 日常指导模式（活动推荐 + 发展关注 + 跟进回访） |
| `/yuer-ask 问题` | 问题解答模式（循证建议 + 效果追踪） |

## 数据文件

所有数据通过对话自动生成，存储在 `data/` 目录：

| 文件 | 内容 |
|------|------|
| `data/child-profile.json` | 孩子档案（基本信息、发展、气质、家庭） |
| `data/advice-tracking.json` | 建议追踪（策略效果、历史记录） |
| `data/context-journal.json` | 上下文日志（近期事件、活跃问题） |

## 知识库

内置育儿知识库在 `research/` 目录，涵盖：

- 6本经典育儿书的精读笔记
- 常见问题导航（情绪、饮食、睡眠、社交等）
- 活动设计指南
- 发展里程碑
- 如厕训练、戒奶嘴、恐惧脱敏等专题指南
- 管教方法对比分析

知识库会随着使用自动扩展：当你提出知识库未覆盖的问题时，系统会自动调研并补充。
