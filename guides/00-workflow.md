# Workflow: 殴り書きから公開まで

このリポジトリでLinkedIn投稿を作る全工程。
1投稿あたりの目標時間: **30分**(慣れてきたら20分)。

---

## Overview
殴り書き → 軸選び → テンプレ選び → 箇条書き → 文章化 → 削る → 装飾 → 公開
inbox/   guides/01  templates/   drafting/   drafting/  scheduled/  published/

各ステップでフォルダが変わる。物理的にファイルを移動することで「今どこにいるか」が分かる。

---

## Step 1: 殴り書きを `inbox/` に保存

- iPad音声入力 → Notion Inbox にメモ
- ターミナル or Notion MCP で `inbox/YYYY-MM-DD-topic.md` として保存
- この段階では整形しない。生のまま残す

ファイル名規則: `YYYY-MM-DD-{topic-kebab-case}.md`
例: `2026-04-25-germany-exam-fail.md`

---

## Step 2: 軸を選ぶ (5分)

`guides/01-finding-the-angle.md` を参照。

殴り書きから「言えること」を箇条書きで全部出す。
5つの軸フレームから1つに絞る。
残りの話題は別投稿用に Notion Inbox に追加。

---

## Step 3: テンプレを選ぶ (1分)

軸が決まると、対応するテンプレが自動的に決まる。
`guides/01-finding-the-angle.md` の「軸×テンプレ マッピング」を参照。

```bash
cp templates/0X-xxx.md drafting/YYYY-MM-DD-topic.md
```

---

## Step 4: 箇条書きで埋める (10分)

`drafting/` のファイルを開く。
各セクション(Hook, Background, ...)を**箇条書きで**埋める。
**完成文章にしようとしない**。これが速度のコツ。

例:
```markdown
## 📌 Background
- ドイツ修士の評価は試験1本(日本との違い)
- 2回落ちたら退学リスク
- 自分は計算言語学が好きで得意だと思ってた
```

---

## Step 5: 文章化 (5分)

箇条書きを文章に。1段落 = 1-2文 のリズムで書く。
この段階でも装飾はしない。

---

## Step 6: 削る (5分)

`guides/02-decoration-and-length.md` を参照。

- 1500文字以内に収める
- 「ちなみに」「補足」を全部削る
- 1セクションに主張は1つだけ

削る作業が一番効く。書く時間より削る時間の方が大事。

---

## Step 7: 装飾 (3分)

`guides/02-decoration-and-length.md` を参照。

- セクション頭に絵文字1個ずつ
- 改行を1段落=1-2文に
- ハッシュタグを末尾に3-5個

装飾完成版を `scheduled/YYYY-MM-DD-topic.md` に移動。

```bash
mv drafting/YYYY-MM-DD-topic.md scheduled/
```

---

## Step 8: 公開 (1分)

LinkedInに手動で投稿。
URLを Notion の Pipeline Database に記録。
ファイルを `published/` に移動。

```bash
mv scheduled/YYYY-MM-DD-topic.md published/
```

Notion DBの該当エントリで:
- Status: ✅ Published
- Published URL: 投稿URLを貼る

---

## 媒体別の二次展開 (Step 8の後)

LinkedIn版の原稿を元に、他媒体用に変換。

| 元: LinkedIn (1300文字・英文) | → 変換先 |
|---|---|
| 留学・体験系 | Note (日本語フル版・3000-5000字) |
| 技術系 | Zenn (日本語) / Medium (英語) |
| Resource Drop | 自分のブログ + PDF |

変換は最初は手動、慣れたら Claude API スクリプトで自動化。

---

## 時間配分まとめ

| Step | 時間 | 内容 |
|---|---|---|
| 1 | (随時) | 殴り書き保存 |
| 2 | 5分 | 軸選び |
| 3 | 1分 | テンプレ選び |
| 4 | 10分 | 箇条書きで埋める |
| 5 | 5分 | 文章化 |
| 6 | 5分 | 削る |
| 7 | 3分 | 装飾 |
| 8 | 1分 | 公開・記録 |
| **合計** | **30分** | |

