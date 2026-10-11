# MyKnowledgeBase

个人知识库，用 [Obsidian](https://obsidian.md) 打开，按 [PARA](https://fortelabs.com/blog/para/) 方法组织，多台机器通过 GitHub 同步。

目前收录 **44 篇笔记** + 90 个附件，正在陆续整理中。

## 目录结构

| 目录 | 用途 |
| --- | --- |
| `000-📇Index/` | 入口与导航 —— 从 `首页.md` 开始 |
| `100-📖Projects/` | 有明确目标和期限的事，如「家庭健身计划 · 第一阶段 12 周」 |
| `200-👨‍💻Area/` | 持续精进的领域：Linux、工具与技巧、嵌入式、健身、Python |
| `300-📚Resource/` | 主题知识储备：AI 辅助编程、设计模式、算法、PARA 方法论 |
| `400-📦Archive/` | 不再活跃的内容 |
| `Attachment/` | 笔记图片等附件 |
| `.obsidian/` | Obsidian 配置与插件 |

空目录用 `.nofile` 占位（目前只剩 `400-📦Archive/` 需要），这样 git 才能跟踪到它。

## 用法

```bash
git clone https://github.com/ge-yf/MyKnowledgeBase.git
```

用 Obsidian 的「打开文件夹作为库」选中本目录即可。笔记之间用 `[[双链]]` 关联，入口页是 `000-📇Index/首页.md`。

## 内容速览

### Linux（`200-👨‍💻Area/Linux/`）

- **基础**：APUE、Linux 中的各种栈、Linux 进程间通信-pipe、互斥锁/同步锁/临界区/互斥量/信号量/自旋锁
- **常用操作**：Linux 手动挂载 U 盘、压缩与解压缩
- **环境配置**（`Linux软件配置/`）：Ubuntu、neovim、zsh、spacemacs、v2ray；`ArchLinux/` 下有 Install、Kitty、Hyprland、bluetooth、SoftwareConfig 等装机笔记
- **学习系列**：`wayland/Wayland入门教程`（01–04）、`你管这破玩意叫操作系统源码`（Linux 0.11 源码品读，00–04）

### 工具与技巧（`200-👨‍💻Area/工具与技巧/`）

Git、repo 命令、markdown 语法、Chrome 快捷键、Windows 快捷键

### 嵌入式（`200-👨‍💻Area/嵌入式/`）

SPI 通信、嵌入式开发进阶笔记

### 健身

`200-👨‍💻Area/健身/`：哑铃、运动消耗计算

### Resource（`300-📚Resource/`）

AI 辅助编程学习资源、The P.A.R.A Method、Tiago Forte、图解 23 种设计模式、算法-合并两个链表

## 同步与约定

- **多机同步**：几台机器同时编辑，靠 GitHub 合并。冲突时以**本机 PARA 目录结构 + 远程笔记内容**为准（不要把笔记搬回旧的 `@Inbox📌` 收集箱，该目录已废弃，内容已并入 `200-👨‍💻Area` 与 `300-📚Resource`）
- **不上库**：`.obsidian/workspace.json` 等本机窗口状态文件已写进 `.gitignore`，各机器自行维护，不参与同步
- **提交信息**：中文，简述改了什么（如 `refactor: Inbox 分类到 PARA、合并重复笔记`）

## 已启用插件

`obsidian-tasks-plugin`、`obsidian-minimal-settings`、`obsidian-hider`、`table-editor-obsidian`、`obsidian-kanban`、`obsidian-icon-folder`、`obsidian-image-layouts`

> `obsidian-plugin-todo`、`periodic-notes` 与 tasks / 核心日记功能重叠，已禁用。
