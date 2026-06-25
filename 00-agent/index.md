---
{
  "title": "宇宙開発コンプライアンスエンジン",
  "version": "0.1.0",
  "domain": "space-development",
  "laws": ["04-uchu", "01-kenpo/02-senso-no-ki", "02-doukou-hou"],
  "graph_ref": "../00-graph/terms.json"
}
---

# 宇宙開発コンプライアンスエンジン

法令を機械可読な**世界モデル**と**コンプライアンスルール**に変換し、
宇宙開発活動の合法性を自動判定する。

## 構成

| ファイル | 役割 |
|---------|------|
| world-model.json | 宇宙開発ドメインの世界モデル（エンティティ・状態・遷移） |
| compliance-rules.json | コンプライアンスルール（条件 → 制約） |
| agent-graph.json | エージェント行動グラフ（状態遷移 + 判定フロー） |

## 世界モデル → グラフ → コンプライアンス

```
法令条文 (自然言語)
  → 00-graph/terms.json (用語グラフ)
    → world-model.json (意味モデル)
      → compliance-rules.json (制約条件)
        → agent-graph.json (実行グラフ)
```

## 利用例

- 「超小型衛星を打ち上げたい」→ 必要な許可・手続きを自動判定
- 「宇宙開発は平和利用か」→ 憲法9条＋宇宙基本法3条を照合
