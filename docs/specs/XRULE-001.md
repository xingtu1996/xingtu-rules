# XRULE-001 v3/v4

状态：running；日期：2026-11-02；主仓：xingtu1996/xingtu-rules。

目标：将 Rules 定义为可解释、自描述、可组合、可验证、可版本化的工程资产；修正确定性加载承诺。仅修改本仓文档，其他仓只读，不实现运行时插件。

验收：README 与 SELF 边界一致；八字段契约、架构、矩阵组合、官方机制和研究依据独立成文；静态链接与 diff 检查；运行时未执行均 NOT_RUN；独立分支 Draft PR，不合并。私有规范不导出，样例可为零。

基线：401aed91957fe21bddd61ce4d1e678cc8211c824；分支 docs/XRULE-001-v4-contract。回退：关闭 Draft PR；未合并无需恢复 main。未来合并后以 revert 专属提交回退，不重置共享分支。
