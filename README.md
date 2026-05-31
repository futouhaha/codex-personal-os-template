# Codex Personal OS 中文模板

这是一套可以分享给朋友的 Codex 个人协作系统模板。

它不是某个人私有配置的原样备份，而是一个已经脱敏、模板化之后的版本。适合用来参考和迁移：

- 全局 `AGENTS.md` 入口文件
- 全局记忆文件夹
- 项目级 `AGENTS.md` 模板
- 项目记忆结构模板
- 任务路由、项目启动、复盘、浏览器安全、工具安装、Skill 策略等规则

如果你想让 Codex 更像一个长期协作搭档，而不是每次都从零开始理解你的偏好，这套模板可以作为起点。

## 目录结构

```text
global/
  AGENTS.md
  memory/
    00_INDEX.md
    01_WORKING_STYLE.md
    02_TASK_ROUTING.md
    03_PROJECT_ONBOARDING_PROTOCOL.md
    04_MEMORY_AND_RETROSPECTIVE_POLICY.md
    05_BROWSER_AND_SECURITY_POLICY.md
    06_TOOLING_AND_INSTALL_POLICY.md
    07_SKILL_STRATEGY.md
    08_CROSS_PROJECT_LEARNINGS.md
    09_REUSABLE_PROMPTS.md
    templates/
project-template/
  AGENTS.md
  docs/codex/
```

## 先改占位符

使用前，先把文件里的这些占位符替换成你自己的信息：

- `{{USER_NAME}}`：你的名字、昵称，或者你希望 Codex 怎么称呼你
- `{{user_name}}`：小写用户名，需要时使用
- `{{CODEX_PROJECTS_ROOT}}`：你准备用来放长期 Codex 项目的目录
- `{{CODEX_GLOBAL_MEMORY_DIR}}`：你复制后的全局记忆目录

例如：

```text
{{CODEX_PROJECTS_ROOT}} = /Users/yourname/Documents/04 Codex
{{CODEX_GLOBAL_MEMORY_DIR}} = /Users/yourname/Documents/04 Codex/_Global Codex Memory
```

路径不一定要和示例一样。关键是：`AGENTS.md` 里写的路径，必须和你电脑上真实存在的路径一致。

## 推荐安装方式

1. 把 `global/AGENTS.md` 复制到 Codex 的全局规则文件位置，通常是：

```text
~/.codex/AGENTS.md
```

2. 把 `global/memory/` 复制到你准备用来长期保存全局记忆的目录。

3. 打开 `~/.codex/AGENTS.md`，把里面的 `{{CODEX_GLOBAL_MEMORY_DIR}}` 改成你真实的全局记忆目录。

4. 如果你要开始一个长期项目，可以把 `project-template/AGENTS.md` 复制到项目根目录。

5. 再按需要创建项目记忆目录，例如：

```text
docs/codex/
```

6. 项目里的记忆文件可以参考 `global/memory/templates/` 里的模板来创建。

## 重要安全提醒

不要提交或分享这些东西：

- `~/.codex/auth.json`
- 本地日志、SQLite 状态文件、缓存文件
- API key、token、密码、`.env` 文件
- 账号页面截图、验证码、支付信息
- 没有检查过的个人原始记忆
- 私密聊天、私密文档、敏感个人信息

这套仓库适合分享“结构、规则和方法”，不适合分享“真实账号配置”和“未经处理的私人记忆”。

## 给朋友怎么用

可以直接把这个仓库链接发给朋友，然后告诉他：

1. 先读 `README.md` 和 `INSTALL.md`。
2. 不要直接照搬路径，先替换占位符。
3. 先从 `global/AGENTS.md` 和 `global/memory/00_INDEX.md` 看起。
4. 不要把别人的项目记忆原样复制成自己的长期记忆。
5. 真正开始一个项目之后，再建立这个项目自己的项目记忆。

最稳妥的方式是：先把这套模板当作“参考骨架”，再让 Codex 帮你根据自己的电脑路径、工作习惯和项目类型做一次适配。
