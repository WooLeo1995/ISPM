# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 仓库概述

这是一个 **Obsidian 知识库**，用于备考中国"软考高项"（高级信息系统项目管理师）认证考试。内容围绕教材 23 个章节构建，包含概念笔记、源材料和综合总结。

## 内容结构

| 目录 | 用途 |
|------|------|
| `sources/` | 23 篇教材章节原始笔记（第01章~第23章） |
| `concepts/` | 从源材料提取的关键概念笔记（29 篇） |
| `synthesis/` | 高级综合总结（PMBOK 知识体系、备考重点） |
| `entities/` `skills/` `references/` `journal/` `projects/` | 预留空目录 |
| `index.md` | 自动生成的维基索引，链接所有概念和源文件 |
| `log.md` | 库操作变更日志 |
| `hot.md` | 最近活动的语义快照（热缓存） |

## Frontmatter 规范

概念笔记使用 YAML frontmatter：

```yaml
---
title: 概念名称
tags:
  - 域标签
---
```

标签覆盖：成本管理、进度管理、范围管理、风险管理、质量管理、整合管理、沟通管理、资源管理、采购管理、干系人管理、敏捷、软考、PMBOK 等。新增笔记应使用已有标签体系。

## 链接约定

- 使用 `[[wikilink]]` 语法，不用 Markdown 标准链接
- 索引链接格式：`[[path|display]]`（如 `[[concepts/整合管理|整合管理]]`）
- 概念笔记交叉引用源章节：`[[../sources/第11章|第11章-成本管理]]`

## Agent 框架

`.agents/` 目录包含 28 个 obsidian-wiki 技能定义，用于知识摄取、交叉链接、标签分类、查询、可视化等。`skills-lock.json` 记录已安装技能版本。

## Obsidian 插件

- **obsidian-git**：仓库自动备份
- **claudian** (v2.0.11)：Claude Code 嵌入 Obsidian，权限模式 `yolo`，模型 Haiku
- **easy-typing-obsidian**：中文排版增强
- **editing-toolbar**：编辑工具栏

## Git 配置

- 远程：`git@github.com:WooLeo1995/ISPM.git`（SSH，端口 22）
- `.gitignore` 排除：`.obsidian/`、`.DS_Store`、`.claude/`、`.claudian/`
- 只跟踪笔记内容，不跟踪编辑器状态和插件数据
