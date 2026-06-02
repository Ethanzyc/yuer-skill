---
description: 个性化日常育儿指导（活动建议+发展关注+跟进回访）
allowed-tools: Read, Write, Edit, WebSearch
---

请激活 parenting 技能，进入日常指导模式。

1. 读取 data/child-profile.json（检查是否首次使用 → 是则进入建档模式）
2. 读取 data/context-journal.json（近期事件、活跃问题、季节因素）
3. 读取 data/advice-tracking.json（历史建议效果、待跟进项）
4. 如果有待跟进项 → 先主动回访上次建议的执行情况
5. 读取 knowledge/07-developmental-milestones-26-36m.md 中当前月龄对应的里程碑
6. 读取 knowledge/05-play-activities-design.md 中适合的活动
7. 读取 data/knowledge-index.json 和 knowledge/index.json（用户优先，合并索引）

按照 parenting 技能中 guide 模式的格式生成回复：
- 【跟进回访】如有待跟进项，先回访
- 【今日关注】当前月龄重要发展关注点
- 【推荐活动】2-3个适合的活动，结合孩子兴趣和策略响应模式
- 【发展观察】可以观察的一个发展指标，与活跃问题关联
- 【育儿小贴士】一条来自书籍的实用技巧
- 【主动提醒】月龄发展提醒 / 追踪跟进提醒 / 季节提醒（如有）

8. 如果对话中用户提到了新的育儿问题或困扰，执行 guide 模式的"问题捕获"步骤：
   - 按 ask 模式分层判断 L1/L2/L3
   - L2/L3 问题写入 `data/advice-tracking.json`（records + followUps）
   - 更新 `data/context-journal.json` 的 activeProblems
   - 如该问题不在两个知识索引中，触发知识自检（调研并补充到 `data/research/` 和 `data/knowledge-index.json`）
   - 回复末尾附上说明：已记录该问题，后续会持续跟进
