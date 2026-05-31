# 安装说明

这份说明是给第一次迁移这套 Codex 个人协作系统的人看的。目标不是让你一次性理解所有文件，而是先把最小可用版本装起来。

## 1. 选择本地目录

推荐把长期 Codex 项目和全局记忆放在一个稳定目录里，例如：

```text
~/Documents/04 Codex/
  _Global Codex Memory/
  <project-name>/
```

你也可以使用别的目录。唯一要注意的是：`~/.codex/AGENTS.md` 里写的全局记忆路径，必须和电脑上的真实路径一致。

## 2. 安装全局规则

复制这个文件：

```text
global/AGENTS.md
```

到 Codex 的全局规则文件位置：

```text
~/.codex/AGENTS.md
```

然后把文件里的这个占位符：

```text
{{CODEX_GLOBAL_MEMORY_DIR}}
```

替换成你自己的全局记忆目录，例如：

```text
/Users/yourname/Documents/04 Codex/_Global Codex Memory
```

## 3. 安装全局记忆

复制这个文件夹：

```text
global/memory/
```

到你选择的长期记忆目录，例如：

```text
~/Documents/04 Codex/_Global Codex Memory/
```

复制完成后，建议先打开 `00_INDEX.md` 看一遍。它是全局记忆的目录说明。

## 4. 开始一个新项目

每个长期项目建议这样做：

1. 创建一个项目文件夹。
2. 把 `project-template/AGENTS.md` 复制到项目根目录。
3. 创建项目记忆目录，例如 `docs/codex/`。
4. 根据 `global/memory/templates/` 里的模板，创建这个项目自己的记忆文件。

项目级 `AGENTS.md` 只负责当前项目，不要把所有全局规则都塞进去。

## 5. 推荐第一次使用时这样问 Codex

安装好以后，在项目目录里打开 Codex，然后说：

```text
请先读取当前项目的 AGENTS.md，并帮我初始化项目记忆结构。写入任何文件前，请先说明你计划创建哪些文件、为什么创建，并等待我确认。
```

这样可以避免 Codex 在你还没确认前直接改规则或写记忆。

## 6. 后续维护原则

维护记忆时建议遵守这几条：

- 项目事实写进项目记忆。
- 跨项目反复出现、长期稳定的经验，才写进全局记忆。
- 账号、密码、token、API key、验证码、支付信息不要写进记忆。
- 私密聊天、敏感个人信息、未经整理的原始材料不要写进记忆。
- 不确定该不该写时，先让 Codex 提出“记忆更新建议”，你确认后再写。

这套系统的重点不是“记很多东西”，而是让 Codex 在合适的时候读取合适的规则，并且知道哪些事情必须先问你。
