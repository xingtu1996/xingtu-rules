# XingTu Rules · 规则工程化

> AI 协作规则（rules）方法论与可复用规则库，含 scoped / on-demand 分层实践。

![CC BY-NC-SA 4.0](https://img.shields.io/badge/license-CC%20BY--NC--SA%204.0-lightgrey.svg)

## 🎯 这是什么

`xingtu-rules` 是行途开源矩阵的**规则资产仓**。沉淀"如何把团队规范 / 编码约定 / 流程要求变成 AI 可执行的 rules"方法论，并提供分层规则库：

- `rules/` — 全局通用规则
- `rules-scoped/` — 按场景/目录生效的规则
- `rules-on-demand/` — 按需触发的规则

## 🧩 DeepSeek Harness（DSH）兼容

本仓 rules 采用 AI 可执行的规则工程化格式（分层 / 按场景 / 按需触发），DeepSeek Harness 的插件模型可把 `rules/` 作为规则资产加载，约束 Agent 行为，无需改写。

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

每个规则文件遵循统一 frontmatter（name + description + 适用场景），供 AI 工具检索。

## 📄 许可证

本仓库为**方法论/内容型资产**，采用 **CC BY-NC-SA 4.0**（署名-非商业使用-相同方式共享）授权。

- **署名**：转载/引用需保留作者署名（行途 / xingtu1996）及出处
- **非商业**：禁止用于商业用途（包括但不限于：商用课程、商业出版物、付费产品）
- **相同方式共享**：演绎作品须以相同协议发布

完整条款见 [LICENSE](./LICENSE)。商业使用 / 出版合作请联系作者。

---

> AI 辅助创作 · 内容基于真实工程实践

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

完整方法论深度篇与实战案例 → 《行途 AI 工程化手册》（出版筹备中）
深度答疑 / 定制陪跑 / 知识星球 → xingtutech@163.com
