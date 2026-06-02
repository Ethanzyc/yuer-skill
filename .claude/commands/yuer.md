---
description: 个性化日常育儿指导（活动建议+发展关注+跟进回访）
allowed-tools: Read, Write, Edit, WebSearch
---

请激活 parenting 技能，进入日常指导模式。

1. 读取 data/child-profile.json（检查是否首次使用 → 是则进入建档模式）
2. 读取 data/context-journal.json（近期事件、活跃问题、季节因素）
3. 读取 data/advice-tracking.json（历史建议效果、待跟进项）
4. 如果有待跟进项 → 先主动回访上次建议的执行情况
5. 读取 research/07-developmental-milestones-26-36m.md 中当前月龄对应的里程碑
6. 读取 research/05-play-activities-design.md 中适合的活动
7. 读取 references/knowledge-index.json

按照 parenting 技能中 guide 模式的格式生成回复：
- 【跟进回访】如有待跟进项，先回访
- 【今日关注】当前月龄重要发展关注点
- 【推荐活动】2-3个适合的活动，结合孩子兴趣和策略响应模式
- 【发展观察】可以观察的一个发展指标，与活跃问题关联
- 【育儿小贴士】一条来自书籍的实用技巧
- 【主动提醒】月龄发展提醒 / 追踪跟进提醒 / 季节提醒（如有）
