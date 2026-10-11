# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 这是什么

个人 Obsidian 知识库（笔记仓库，不是软件工程）：Markdown 笔记 + `.obsidian/` 配置 + `Attachment/` 附件，靠 git + GitHub 在多台机器之间同步。

- **没有**构建、依赖、lint、测试；这里的"开发"就是增删改 Markdown 笔记和 `.obsidian/` 配置
- 面向人的说明在 `README.md`，内容入口是 `000-📇Index/首页.md`
- 提交历史里那些 `update` 多来自另一台机器上的 Obsidian

## 目录约定（PARA）

`000-📇Index`（导航）→ `100-📖Projects` / `200-👨‍💻Area` / `300-📚Resource` / `400-📦Archive`，附件进 `Attachment/`，配置在 `.obsidian/`。空目录用 `.nofile` 占位（目前只剩 `400-📦Archive/` 为空需要它），否则 git 跟踪不到。

`@Inbox📌` 收集箱**已废弃**（内容已并入 PARA）。不要在笔记、首页、README 里重新引入"先进 Inbox 再归类"的流程，也不要新建该目录。

## ⚠️ 头号坑：emoji 目录名含零宽连接符 U+200D

`200-👨‍💻Area` 的 emoji 是 U+1F468 + **U+200D** + U+1F4BB（字节 `\xf0\x9f\x91\xa8\xe2\x80\x8d\xf0\x9f\x92\xbb`）。模型/tool 输出的同名 emoji 常常**不带** U+200D，直接拿去拼路径就会在库里造出一份肉眼同名的重复目录 —— commit `fc3a75b` 修的就是这个（40 篇笔记当时落在错误的那份里；Obsidian、`首页.md`、icon-folder 插件配置用的都是带 ZWJ 的版本）。

做法：

- 脚本里显式构造：Python `'\U0001F468\u200d\U0001F4BB'`；bash `$'\xf0\x9f\x91\xa8\xe2\x80\x8d\xf0\x9f\x92\xbb'`
- 写文档、提交信息时先放占位符，再用脚本注入正确字节（README.md / CLAUDE.md 都是这么写的）
- 改完按字节核对：`path.encode('utf-8')` 应等于上面的字节串；重名目录用 `git -c core.quotepath=false ls-files` 一眼可见
- 📇📖📚📦📌 是单码点 emoji，没有这个问题

## 常用命令

环境是 Windows + Git Bash，非 ASCII 路径到处都是：

```bash
# 列文件/看状态：不加 -c 的话非 ASCII 路径会被转义成 "...\360\237..."（辨认得了，但不好处理）
git -c core.quotepath=false status --short
git -c core.quotepath=false ls-files

# 合并或批量改笔记后：确认没有冲突标记残留
git grep -n -E "^(<<<<<<<|>>>>>>>|=======)$" -- .

# .obsidian 下的 JSON 合法性（插件会自己改写这些文件）
python -c "import json,glob;[json.load(open(f,encoding='utf-8')) for f in glob.glob('.obsidian/*.json')]"
```

批量处理路径**用 Python**（`subprocess` + `decode('utf-8','surrogateescape')`），不要 `for f in $(git ...)`——转义和空格会把路径拆错。`git mv` 到尚不存在的目标子目录会报 `No such file or directory`（真实原因是目标目录缺失），先 `os.makedirs` 再搬。

`core.autocrlf=true`，看到 "LF will be replaced by CRLF" 警告是正常的。

## 多机同步与冲突解决

几台机器同时编辑同一批笔记，**冲突是常态**。典型根因：一台机器把笔记搬进 PARA 新目录（rename），另一台还在旧路径上写内容（modify），于是出现 rename/modify、目录重命名、删除/修改等一堆冲突。

已与用户确认的原则：**保留本机的 PARA 路径，采纳远程的笔记内容**；旧 `@Inbox📌` 路径一律删除。远程的目录决定（例如把 `spacemacs.md` 挪进 `Emacs/`）不必照搬——内容不丢、不留重复副本优先。

解决后**必须核对两侧内容都在**：用 `git ls-tree -r <rev>` 取出 merge-base / HEAD / MERGE_HEAD 的 blob 哈希，确认最终索引里每个文件都能找到同内容文件，或确认它属于某一侧的有意删除。只跑 `git status` 看不出"内容被悄悄丢掉"。

## 其它约定

- **提交信息用中文**，前缀跟历史一致：`docs:` / `fix:` / `chore:` / `refactor:`；结尾附 `Co-Authored-By: Claude Code <noreply@anthropic.com>`
- 大量搬动笔记时在提交信息里写明"文件名与内容零改动"，方便事后核对
- **不要主动 push**，用户自己决定何时推
- `.obsidian/workspace.json`、`.obsidian/workspace` 等本机状态文件已在 `.gitignore` 里，**保持不跟踪**
- 用户经常开着 Obsidian，它会实时改写 `.obsidian/` 下的配置（例如目录删掉后 icon-folder 自动更新 `data.json`）。`git status` 里冒出来的这类改动，与本次操作相关就一起提交
- 笔记之间靠 `[[双链]]` 按**文件名**解析：移动目录不会断链，**改文件名会**，重命名笔记前先 `git grep` 一下引用
