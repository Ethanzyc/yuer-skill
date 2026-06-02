# 数据结构参考

> 写入 JSON 数据前必须阅读此文件，确保 key 与前端 TypeScript 接口一致。
> 前端接口定义在 `web/src/pages/*.astro`

---

## `data/child-profile.json`

```json
{
  "child": {
    "name": "", "gender": "", "birthDate": "YYYY-MM-DD", "city": "",
    "personality": { "temperament": "", "interests": [], "description": "" },
    "developmentNotes": ""
  },
  "health": {
    "allergies": [],
    "sleepPattern": { "bedtime": "", "wakeup": "", "nap": "" },
    "diet": { "preferences": [], "challenges": [] },
    "notes": ""
  },
  "school": { "type": "", "schedule": "", "notes": "" },
  "siblings": [],
  "languageEnv": [],
  "family": {
    "primaryCaregiver": "",
    "caregivers": [{ "role": "", "time": "", "notes": "", "style": "", "relationship": "" }],
    "parentingStyle": "", "notes": ""
  },
  "strategyResponse": [{ "strategy": "", "type": "", "rating": 0, "notes": "", "evidence": "", "evaluatedAt": "" }],
  "behaviorPatterns": [{ "topic": "", "pattern": "", "observedAt": "" }],
  "currentConcerns": [],
  "parentingPhilosophy": { "preferredApproach": "", "booksReading": [] },
  "lastUpdated": "YYYY-MM-DD"
}
```

易错点：`family.caregivers` 是数组不是对象 | `child.personality` 不是根级 `temperament` | `languageEnv` 不是 `familyContext.languageEnvironment` | `siblings` 是数组不是字符串 | `parentingPhilosophy` 是对象不是字符串

---

## `data/advice-tracking.json`

```json
{
  "records": [{
    "id": "R001", "date": "YYYY-MM-DD", "topic": "", "level": "L1|L2|L3",
    "problemContext": "", "strategiesSuggested": [], "sources": [],
    "followUpDate": "YYYY-MM-DD", "status": "in-progress|pending|resolved|completed",
    "difficulty": "", "expectedTimeline": "", "outcome": "", "childReaction": "", "parentFeedback": ""
  }],
  "followUps": [{
    "id": "F001", "recordId": "R001", "topic": "", "questionToAsk": "", "dueDate": "YYYY-MM-DD", "status": "pending|completed"
  }],
  "strategySummary": [{
    "strategy": "", "usageCount": 0, "averageEffectiveness": null, "lastUsed": "YYYY-MM-DD", "source": ""
  }],
  "lastUpdated": "YYYY-MM-DD"
}
```

易错点：`topic` 不是 `problem` | `strategiesSuggested` 是数组不是 `advice` 字符串 | `sources` 是数组不是 `source` 字符串 | `dueDate` 不是 `checkDate` | `questionToAsk` 不是 `question` | 状态用 `in-progress` 不是 `in_progress`

---

## `data/knowledge-index.json`

```json
{
  "problemMap": [{ "keywords": [], "primaryResource": ".md", "section": "", "level": "L1|L2|L3" }],
  "bookIndex": [],
  "lastUpdated": "YYYY-MM-DD"
}
```

## `data/context-journal.json`

此文件前端不直接使用，结构可自定义。
