# Coding Agent 官方加载机制

核验日期 2026-11-02。下表为官方文档阅读结果，全部真实运行时测试 **NOT_RUN**；未锁定发行版本的产品只代表当日文档，不承诺旧版行为。字段契约不能直接充当平台加载配置。

| 产品与官方来源 | 入口、范围与优先级 | 版本与限制 |
|---|---|---|
| [Claude Code](https://code.claude.com/docs/en/memory) | CLAUDE.md 分层加载；`.claude/rules/*.md` 无 paths 可常驻，有 paths 按匹配加载；AGENTS.md 支持受配置控制 | 直接读取 AGENTS.md 要求 >=2.1.277；默认存在适用 CLAUDE.md 时优先后者，可配置两者；2.1.281 前部分会话受限，内置插件禁用也会影响。路径规则不是目录分类即自动生效 |
| [Codex](https://learn.chatgpt.com/docs/agent-configuration/agents-md) | 全局与项目根至工作目录发现；每目录优先 AGENTS.override.md，再 AGENTS.md，再配置 fallback；更深指导后组合 | 默认 project_doc_max_bytes 32 KiB；本轮未锁 CLI 版本，不原生承诺 `.claude/rules` 或 `@path` |
| [Cursor](https://cursor.com/docs/rules) | `.cursor/rules/*.mdc`：alwaysApply、globs、description 控制常驻/匹配/智能/手动；另支持 AGENTS.md | `.md` 放 rules 目录不视作 MDC；不推定多规则冲突必有通用覆盖次序，需测试；发行版未锁定 |
| [Copilot](https://docs.github.com/en/copilot/concepts/prompting-and-context/custom-instructions) | 仓库 `.github/copilot-instructions.md` 与路径 `.github/instructions/*.instructions.md`；AGENTS.md 支持依客户端/功能 | 多数客户端组合适用指令，无通用优先级；GitHub.com Chat 有专门顺序，不能推广到 CLI/IDE；版本未锁 |
| [Gemini CLI](https://geminicli.com/docs/cli/gemini-md/) | GEMINI.md 层级上下文，支持文件导入，可配置文件名 | 上下文组合不等同权限覆盖；不能推定 Claude paths 可复用，版本未锁 |
| [Cline](https://docs.cline.bot/customization/cline-rules) | `.clinerules/`、`.cline/rules/`、AGENTS.md；条件规则根据当前工作上下文匹配，开关可禁用 | 不能把 paths 直接当所有平台统一语义；跨来源冲突顺序待实测；版本未锁 |
| [DSH agent-instructions](https://github.com/deepseek-ai/deepseek-harness/blob/master/packages/context/agent-instructions/README.md) | 默认 AGENTS.md/CLAUDE.md 候选链与项目 local overlay；dsh-base 默认启用，profile 可禁用；首次请求加载，文件工具触达后刷新 | 明确不解释 `.claude/rules/`、小写候选或 `@path`；shell cd 不触发嵌套发现；master 文档快照，非发行兼容承诺 |

[DSH 架构](https://github.com/deepseek-ai/deepseek-harness/blob/master/docs/architecture.md) 的插件、服务、Profile/Bundle 与 Cordis 生命周期可启发适配层；本仓没有因此自动成为运行时插件。

待实测统一用例：适用路径加载；范围外不加载；两规则冲突；配置/插件缺失；嵌套指令刷新；卸载恢复。保存产品版本、源 SHA、加载日志和行为结果。文档支持与本仓实测是两个维度。
