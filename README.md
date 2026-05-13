# ナレッジソサエティ Company

ナレッジソサエティ様の業務を Claude Code（パソコン上で動く Claude）で動かすための **会社フォルダ** です。

## このフォルダで何ができるか

- Claude Code を起動して、**秘書のように相談・壁打ち** ができる
- 業務領域（コンテンツ制作・SEO・アフィリ運用・自動化）ごとに、**Claude が役割を切り替えて** 対応してくれる
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

※ 上の URL は MTG 当日にご案内します。

## フォルダ構成

```
knowledge-society-company/
├── CLAUDE.md              ← 会社全体のルール（最重要）
├── README.md              ← このファイル
├── secretary/             ← 秘書（窓口・壁打ち相手）
│   └── CLAUDE.md
├── content/               ← 動画コンテンツ制作
│   └── CLAUDE.md
├── seo/                   ← ブログ SEO・サテライト
│   └── CLAUDE.md
├── affiliate/             ← 金融アフィリ運用
│   └── CLAUDE.md
└── automation/            ← 自動化スクリプト置き場
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
- `seo フォルダで、銀行手数料の比較記事 3 本分の構成案を出して`
- `先月のアフィリ成果を整理して`

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

## サポート

操作で詰まったら、Key_dev までご連絡ください。
毎週水曜 21:00 の定例 MTG で、運用上の改善も継続的に進めていきます。

---

*このフォルダは Key_dev が cc-Company（個人運用中の AI 組織システム）を、ナレッジソサエティ様の業務向けにスリム化してご提供しているものです。*
