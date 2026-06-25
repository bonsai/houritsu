---
{
  "title": "宇宙NPO 関係グラフ（抄）",
  "nodes": 8,
  "edges": 9
}
---

# 宇宙NPO 関係グラフ

```json
{
  "nodes": [
    { "id": "04-uchu", "type": "law", "label": "宇宙基本法" },
    { "id": "npo-law", "type": "law", "label": "NPO法" },
    { "id": "jaxa", "type": "agency", "label": "JAXA" },
    { "id": "space-npo", "type": "organization", "label": "宇宙NPO" },
    { "id": "school", "type": "organization", "label": "教育機関" },
    { "id": "citizen", "type": "actor", "label": "市民" },
    { "id": "cabinet-office", "type": "ministry", "label": "内閣府" },
    { "id": "mext", "type": "ministry", "label": "文科省" }
  ],
  "edges": [
    { "source": "04-uchu", "target": "space-npo", "relation": "enables", "via": "第12条・第17条" },
    { "source": "npo-law", "target": "space-npo", "relation": "gives_legal_status" },
    { "source": "cabinet-office", "target": "npo-law", "relation": "administers" },
    { "source": "mext", "target": "jaxa", "relation": "supervises" },
    { "source": "jaxa", "target": "space-npo", "relation": "collaborates" },
    { "source": "space-npo", "target": "school", "relation": "provides_education" },
    { "source": "space-npo", "target": "citizen", "relation": "engages" },
    { "source": "space-npo", "target": "cabinet-office", "relation": "reports_to" },
    { "source": "citizen", "target": "space-npo", "relation": "donates" }
  ]
}
```
