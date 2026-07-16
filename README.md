# Prompt-Engering

一份面向软件工程协作场景的 Claude Code / Codex 全局提示词，强调工程质量、真实性、安全边界、验证与学习。

## 使用方法

### Claude Code

将仓库中的 `CLAUDE.md` 放到 Claude Code 的全局配置目录。

#### Windows

```text
C:\Users\<你的用户名>\.claude\CLAUDE.md
```

#### macOS / Linux

```text
~/.claude/CLAUDE.md
```

Claude Code 会在不同项目中复用这份全局协作约定。项目自身的 `CLAUDE.md` 仍可补充项目特有的架构、命令与规范。

### Codex

将仓库中的 `AGENTS.md` 放到 Codex 的全局配置目录。

#### Windows

```text
C:\Users\<你的用户名>\.codex\AGENTS.md
```

#### macOS / Linux

```text
~/.codex/AGENTS.md
```

如果设置了 `CODEX_HOME`，请将文件放到 `%CODEX_HOME%\AGENTS.md`（Windows）或 `$CODEX_HOME/AGENTS.md`（macOS / Linux）。

也可以把 `AGENTS.md` 放在项目根目录，让规则只对该项目生效。Codex 会从项目根目录向当前工作目录逐层读取 `AGENTS.md`，更深层目录中的规则优先级更高。

## 设计重点

- 先理解上下文，再修改代码
- 优先简单、可靠、可维护的工程方案
- 不编造文件、API、执行结果或测试结果
- 对高风险和不可逆操作设置确认边界
- 复杂任务包含目标、分析、方案、风险与验证
- 在完成任务的同时解释关键工程知识

## License

[MIT](LICENSE)
