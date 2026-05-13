# ナレッジソサエティ Company

ナレッジソサエティ様の業務を Claude Code（パソコン上で動く Claude）で動かすための **会社フォルダ** です。

## このフォルダで何ができるか

- Claude Code を起動して、**秘書のように相談・壁打ち** ができる
- 営業 / 制作 / 運用などの業務領域ごとに、**Claude が役割を切り替えて** 対応してくれる
- 必要なルールは Markdown ファイル（人間が読める普通の日本語）で書かれているので、**ご自身で編集してカスタマイズ** できる

## 必要なもの

事前に PC に入れておくもの（5/20 MTG で一緒にインストールします）:

- **Node.js**（土台のソフト）
- **Git**（このテンプレを取りに行くソフト）
- **Claude Code**（本体）
- **Claude プラン契約**（中級プラン以上）

## インストール（最短ルート）

PowerShell（Windows に最初から入っている、文字を打って操作する画面）で:

```
cd C:\
git clone https://github.com/iluma-sonic/knowledge-society-company.git company
cd company
claude
```

これで Claude Code が起動して、秘書として応答する状態になります。

## フォルダ構成

```
knowledge-society-company/
├── CLAUDE.md              ← 会社全体のルール（最重要）
├── README.md              ← このファイル
├── secretary/             ← 秘書（窓口・壁打ち相手）
│   └── CLAUDE.md
├── sales/                 ← 営業（提案・見積・受注管理）
│   └── CLAUDE.md
├── production/            ← 制作（記事・動画・SNS・資料）
│   └── CLAUDE.md
└── operations/            ← 運用（既存資産の運用・自動化）
    └── CLAUDE.md
```

## 使い方

### 起動

PowerShell で会社フォルダに移動して `claude` を実行:

```
cd C:\company
claude
```

### 話しかける

普通の日本語で OK です。例:

- `今日何やる？`
- `新規見込みリストを整理して`
- `この記事のタイトル案を 5 つ出して`
- `先月のレポートを整理して`

### 更新したい時

弊社（Key_dev）側でテンプレを改善したら、PowerShell で:

```
cd C:\company
git pull
```

最新版が反映されます。

### 自分で編集したい時

各フォルダの `CLAUDE.md` をテキストエディタで開いて、業務に合わせて書き換えて OK です。
「こういう時はこう動いてほしい」を書けば、Claude がその通りに振る舞います。

**最初はそのまま使い始めて、運用しながら少しずつ各部署の CLAUDE.md を育てていく** のがおすすめです。

## サポート

操作で詰まったら、Key_dev までご連絡ください。
毎週水曜 21:00 の定例 MTG で、運用上の改善も継続的に進めていきます。

---

*このフォルダは Key_dev が cc-Company（個人運用中の AI 組織システム）を、ナレッジソサエティ様の業務向けにスリム化してご提供しているものです。*
