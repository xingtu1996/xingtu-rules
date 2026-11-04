# XRULE-002｜工作空间锚定（Workspace Anchoring）

> 版本：v1.0 | 生效日期：2026-11-04 | 优先级：P0（Worker 启动必查）

## 规则

Worker（Codex CLI / Qwen Worker / 任何 CLI 宿主）启动时，**第一件事不是读文件，是确认 cwd**：

```
pwd 输出 === <行途工作空间根>
```

不是就立即 `cd <行途工作空间根>`，不要在当前目录执行任何任务。

## 为什么是 P0

Chat（豆包办公 / Qwen Chat）把项目规则作为系统提示强制注入，Worker 一开口就知道 DESIGN.md 三原色、发布包五闸门、叙事骨架。
Worker 是文件读取式——cwd 不对 = 没读项目 AGENTS.md = 零行途上下文 = 色值漂移、结构混乱、逻辑同平面罗列。

2026-11-03 公众号《主题修订审阅》v5 在 `~/Documents/Codex/2026-11-03/` 下生成，返工 5 次才被发现根因。

## 三层防护

| 层 | 位置 | 作用 |
|---|---|---|
| L1 默认工作区指路牌 | `~/Documents/Codex/AGENTS.md` | Worker 默认启动目录，读 AGENTS.md 被拦住 |
| L2 入职提示词 | `xingtu-learn/40-work-driven/W-03-worker-onboard-prompt.md` | Chat→Worker 转换时贴给 Worker |
| L3 全局硬规则 | `~/.codex/AGENTS.md` 末尾 | Codex 全局入口强制指针 |

## 信息源与路径

| 项 | 路径 |
|---|---|
| 项目根 AGENTS.md | `<行途工作空间根>/AGENTS.md` |
| 视觉 SSoT | `<行途工作空间根>/DESIGN.md` |
| 发布包规划 skill | `<行途工作空间根>/.agents/skills/publish-pack-planning/` |
| 踩坑记录 | `xingtu-learn/40-work-driven/W-03-Chat转Worker工作空间漂移.md` |
| 默认工作区 | `~/Documents/Codex/` |

## 换设备/路径变更时

本规则路径写死为 `<行途工作空间根>/`。换设备或路径变更时，**三处同步更新**：
1. 本文件（XRULE-002）
2. 项目根 `AGENTS.md` §工作空间锚定
3. 全局 `~/.codex/AGENTS.md`

不更新 = 新设备/新路径下 Worker 又会漂移。
