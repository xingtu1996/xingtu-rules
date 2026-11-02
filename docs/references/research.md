# 研究依据与局限

2026-11-02 核对原始论文摘要/元数据及官方资料。未复现论文实验，不构成作者、机构背书或本仓实测证明。

| 原始来源 | 发布日期 | 对 XRULE 的设计启示 | 证据局限 |
|---|---|---|---|
| [Liu 等：Lost in the Middle](https://arxiv.org/abs/2307.03172) | 2023-07-06 初稿 | 限制无关上下文，设计作用域与位置回归 | 问答/检索结果不直接证明 Rules 目录设计有效 |
| [Wallace 等：Instruction Hierarchy](https://arxiv.org/abs/2404.13208) | 2024-04-19 | 区分指令信任层级与仓库规则 | 模型训练研究，Markdown 不能获得系统权限 |
| [Shi、Zhang、Cui：Spatiotemporal Composability](https://arxiv.org/abs/2608.25512) | 2026-08-26 | 声明依赖、可撤销副作用，设计包与适配器边界 | 运行时组合理论，不是纯文本规则可逆性的证明 |
| [Yang 等：SWE-agent](https://arxiv.org/abs/2405.15793) | 2024-05-06 | 把工具接口与环境作为评测变量 | 软件修复任务研究不等于 Rules 效果试验 |
| [Jimenez 等：SWE-bench](https://arxiv.org/abs/2310.06770) | 2023-10-10 | 采用真实任务与可重复验收 | 基准成绩不代表作用域加载正确 |
| [Xia 等：Agentless](https://arxiv.org/abs/2407.01489) | 2024-07-01 | 先采用简单可解释流程，再按证据扩展 | 基准和模型条件有限，不代表复杂系统一概无效 |
| [NIST AI 600-1：Generative AI Profile](https://www.nist.gov/publications/artificial-intelligence-risk-management-framework-generative-artificial-intelligence) | 2024-07-26 | 风险记录、持续评估与治理留证 | 自愿风险框架，不是本仓认证或法律合规结论 |

本轮仅以已打开的原始来源支持上述有限推论；未把历史对话中的专家观点和未核验博客当成事实。后续应以规则有/无的配对任务、多次运行、误伤率及违规率验证收益，保留模型、版本、输入与失败记录。
