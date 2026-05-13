# ナレッジソサエティ Company

ナレッジソサエティ様の業務を **Claude デスクトップアプリ + フォルダ連携** で動かすための **会社フォルダ** です。

## このフォルダで何ができるか

- Claude デスクトップアプリのチャット画面で、**秘書のように相談・壁打ち** ができる
- 営業 / 制作 / 運用などの業務領域ごとに、**Claude が役割を切り替えて** 対応してくれる
- 必要なルールは Markdown ファイル（人間が読める普通の日本語）で書かれているので、**ご自身で編集してカスタマイズ** できる

## 必要なもの

事前に PC に入れておくもの（5/20 MTG で一緒にインストールします）:

- **Node.js**（フォルダ連携の土台）
- **Git**（このテンプレを取りに行くソフト、1 回だけ使用）
- **Claude デスクトップアプリ**（既にお持ち）
- **Claude プラン契約**（中級プラン以上）

## 導入の流れ

### 1. テンプレを取得（PowerShell 1 回だけ）

```
cd C:\
git clone https://github.com/iluma-sonic/knowledge-society-company.git company
```

→ `C:\company` に会社フォルダが展開されます。

### 2. Claude デスクトップアプリにフォルダを認識させる

`%APPDATA%\Claude\claude_desktop_config.json` を開いて、以下を貼り付け:

```json
{
  "mcpServers": {
    "company": {
      "command": "npx",
      "args": [
        "-y",
        "@modelcontextprotocol/server-filesystem",
        "C:\\company"
      ]
    }
  }
}
```

→ Claude デスクトップアプリを再起動すれば、フォルダが認識されます。

### 3. デスクトップアプリで動作確認

チャット画面で:

```
company フォルダの中身を一覧で見せてください
```

→ 部署フォルダが見えれば連携成功。

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

### 普段の作業

Claude デスクトップアプリのチャット画面に、自然な日本語で話しかけるだけ。

例:

- `あなたはナレッジソサエティの秘書です。company フォルダの secretary/CLAUDE.md を読んで対応してください。`
- `production フォルダの中に新しい記事ネタリストを作って`
- `先月のレポートを整理して`

### テンプレを更新したい時

弊社（Key_dev）側でテンプレを改善したら、PowerShell で 1 行:

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
