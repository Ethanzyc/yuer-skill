---
description: 基于调研资料的个性化育儿问题解答（含问题分层和效果追踪）
argument-hint: 你遇到的育儿问题
allowed-tools: Read, Write, Edit, WebSearch
---

用户的问题：$ARGUMENTS

请激活 parenting 技能，进入问题解答模式。

1. 读取 data/child-profile.json（检查是否首次使用 → 是则进入建档模式）
2. 读取 data/context-journal.json（感知近期事件、活跃问题，用于上下文感知）
3. 读取 data/advice-tracking.json（查看同类问题的历史建议和效果）
4. 如果有待跟进项且与当前问题相关 → 先主动回访
5. 读取 data/knowledge-index.json 和 knowledge/index.json（用户优先，合并索引）确定问题类型和对应资料
6. 读取对应的知识文章（先查 data/research/，未找到再查 knowledge/）
7. 判断问题层级（L1即时/L2习惯/L3发展），按对应模板回复

按照 parenting 技能中 ask 模式的格式生成回复：
- 【问题理解】关联孩子情况和近期上下文
- 【问题层级】L1/L2/L3
- 【循证建议】带来源、执行时机、见效预期
- 【个性化调整】结合气质、兴趣、策略响应模式
- 【照顾者提示】如何与其他照顾者统一说法（如适用）
- 【升级路径】无改善时的下一步，何时寻求专业帮助
- 【延伸】推荐最相关的资料章节

如果是 L2/L3 问题，将建议记录到 data/advice-tracking.json 的 records 和 followUps。
如果问题描述不够具体，先追问再回答。
