# At-Pet Agent Plugins

[At-Pet](https://github.com/Ni-ShuWu/At-Pet) 桌宠的 Agent 插件集合。每个插件把一个 Agent 应用的事件接入桌宠，显示对应动画并处理权限请求。

## 目录结构

```
仓库根目录
 |
 |- Agent-plugin
    |
    |- claude-code      # atpet-claude-code-plugin
    |- opencode         # atpet-opencode-plugin
     |- opencode-v1      # atpet-opencode-v1-plugin
     |- github-copilot   # atpet-github-copilot-plugin
     |- openai-codex     # atpet-openai-codex-plugin
     |- workbuddy        # atpet-workbuddy-plugin
     |- command-code     # atpet-command-code-plugin
     |- zcode            # atpet-zcode-plugin
     |- deepseek-harness # atpet-deepseek-harness-plugin
     |- penguin-harness  # atpet-penguin-harness-plugin
```

每个插件目录内包含插件源码，以及可选的下载包或配置说明。插件命名格式为 `atpet-{agent_name}-plugin`。

## 插件列表

| Agent | 插件名 | 接入方式 |
| --- | --- | --- |
| Claude Code | `atpet-claude-code-plugin` | HTTP hooks |
| OpenCode | `atpet-opencode-plugin` | OpenCode V2 插件 |
| OpenCode V1 | `atpet-opencode-v1-plugin` | OpenCode V1 插件 |
| GitHub Copilot | `atpet-github-copilot-plugin` | Copilot hooks（命令行 + `bridge.mjs`） |
| OpenAI Codex | `atpet-openai-codex-plugin` | Codex hooks，含权限请求 |
| WorkBuddy | `atpet-workbuddy-plugin` | CodeBuddy 兼容 hooks |
| Command Code | `atpet-command-code-plugin` | `settings.json` hooks |
| ZCode | `atpet-zcode-plugin` | 插件 hooks |
| DeepSeek Harness | `atpet-deepseek-harness-plugin` | `dsh-hooks-codex` 桥接 |
| PenguinHarness | `atpet-penguin-harness-plugin` | 插件 hooks（`user_prompt`、`stop`） |

除 Claude Code 与 OpenCode 外，其他插件共用同一份桥接脚本 `bridge.mjs`（零依赖 Node），各自目录内保留一份，便于单独安装。

## 使用前提

- Windows 10/11。
- 已启动 At-Pet，本地 API 默认监听 `127.0.0.1:8765`。

详细安装步骤见各插件目录下的 README。

## 许可证

MIT
