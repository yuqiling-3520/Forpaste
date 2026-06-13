---
name: data-isolation-constraint
description: 用户要求所有数据与记忆只能存于项目文件夹内,禁止越界
metadata:
  type: feedback
---

用户明确要求:禁止访问 `D:\owner\godot_game\Forpaste` 以外的任何文件/数据,禁止将用户数据存储到该文件夹之外。记忆目录改设在项目内部 `.claude_memory/`。

**Why:** 用户希望数据严格隔离在本项目文件夹内,不外泄、不越界。

**How to apply:** 所有记忆写入 `D:/owner/godot_game/Forpaste/.claude_memory/`,不使用默认的 `C:\Users\...\memory\`。任何越界读取需先征得用户同意。
