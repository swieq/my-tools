# Domain Docs

## 布局

本仓库采用 single-context：
- 根目录 CONTEXT.md：领域术语和上下文。
- docs/adr/：架构决策记录。

## 探索代码前

读取 CONTEXT.md 和与当前任务有关的 ADR。
如果以后出现 CONTEXT-MAP.md，按照其中的指针读取相关上下文。

这些文件不存在时，直接继续，不提示缺失，也不预先创建。
由 domain-modeling 技能在术语或决策明确后按需创建。

## 使用领域术语

Issue 标题、重构建议、假设和测试名称应使用 CONTEXT.md
定义的术语，避免使用词汇表明确排除的同义词。

遇到未定义的概念，先检查是否误用了项目术语；
确有缺口时，记录为 domain-modeling 的输入。

## ADR 冲突

建议与现有 ADR 冲突时，明确指出对应 ADR 和重新讨论的理由，
不要静默覆盖已有决策。
