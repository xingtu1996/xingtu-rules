# 行途技术 Rules · 规则工程化

> AI 协作规则（rules）方法论与可复用规则库，含 scoped / on-demand 分层实践。

![License: MIT](https://img.shields.io/badge/License-MIT-green.svg) ![Rules](https://img.shields.io/badge/rules-1-informational.svg) ![Layers](https://img.shields.io/badge/layers-2%20active%20%2B%201%20planned-yellow.svg)

## 🎯 这是什么

`xingtu-rules` 是行途技术开源矩阵的**规则资产仓**。沉淀"如何把团队规范 / 编码约定 / 流程要求变成 AI 可执行的 rules"方法论，并提供分层规则库：

- `rules/` — 全局通用规则
- `rules-scoped/` — 按场景/目录生效的规则（待填充）
- `rules-on-demand/` — 按需触发的规则（规划中，见 Roadmap）

## 🧩 DeepSeek Harness（DSH）兼容

DSH 默认 agent-instructions 读取 AGENTS.md/CLAUDE.md，但不解释 `.claude/rules/` 或 `@path`。本仓尚无已验证的 Rules 适配器；运行时 **NOT_RUN**。规则是上下文约束，不是强制权限。

## 📦 用法

```bash
# 查看规则
ls rules/

# 安装规则到项目
cp rules/<rule>.md .claude/rules/
```

## 📜 规则清单

| 规则 | 分层 | 说明 |
|------|------|------|
| rules/engineering-rules.md | L0 元规则 | 规则工程化框架：三层结构 / 编码规范 / 五问准则 / 生命周期 |

> 持续填充中：分层规则库（scoped / on-demand 实践）。

## 🤖 AI 可检索

新增资产采用八字段自描述契约；现有元规则尚未迁移，不能声称全库统一 frontmatter。

## 关于作者

我是**行途 XingTu**，一线技术人 + 仍在写代码。这些规则来自真实踩坑：每一条都对应一次事故或一次返工，不是凭空写的最佳实践。

- 🔔 公众号 **「行途技术手记」**：微信搜索关注，看 AI 工程化落地实战
- 🐙 GitHub：[@xingtu1996](https://github.com/xingtu1996)
- 📦 仓库：[xingtu1996/xingtu-rules](https://github.com/xingtu1996/xingtu-rules)

---


## 📄 许可证

本仓库采用 **MIT License**。规则、方法论、模板可自由使用、修改与商用，保留版权声明即可。署名：行途 XingTu / xingtu1996。

完整条款见 [LICENSE](./LICENSE)。

---

## 📁 目录结构

```
rules/           # 全局通用规则
rules/_TEMPLATE/ # 新规则模板
rules-scoped/    # 按场景/目录生效的规则
```

## 🗺 Roadmap

- [ ] 分层规则库填充（scoped / on-demand 实践）
- [ ] 规则方法论文档

---

## 深度内容与咨询

完整方法论深度篇与实战案例 → 《行途技术 AI 工程化手册》（出版筹备中）
深度答疑 / 定制陪跑 / 知识星球 → 公众号「行途技术手记」留言

---

## 👤 关于行途 XingTu

一线 builder，仍在写代码。专注 AI 工具链与工程化落地，分享可抄作业的实战经验。

- 𝕏 X：[@xingtu1996](https://x.com/xingtu1996)（AI工程化实战，build in public）
- GitHub：[github.com/xingtu1996](https://github.com/xingtu1996)
- 🌐 个人站：[xingtu1996.pages.dev](https://xingtu1996.pages.dev)
- 📱 公众号：「行途技术手记」（深度长文 + 可抄作业的实战经验）

## 工程资产定位与文档

本仓定位为可解释、自描述、可组合、可验证、可版本化的工程 Rules 资产库与模板。Rules 不替代项目入口、Skills、Hooks 或 SDD。复制文件前核对 Agent 版本、目标目录、作用域与同名文件，不覆盖已有配置。

- [项目自述](SELF.md)
- [架构与八字段契约](docs/architecture.md)
- [开源矩阵与组合](docs/ecosystem.md)
- [研究依据](docs/references/research.md)
- [官方加载机制](docs/references/coding-agents.md)
- [任务验证报告](docs/XRULE-001-report.md)
