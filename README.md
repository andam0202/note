# note記事管理リポジトリ

このリポジトリは、noteブログサービスに投稿する記事を管理するためのものです。

## amazon アソシエイト

id 
toyoasen0202-22

## ディレクトリ構造

```
note/
├── articles/
│   ├── drafts/          # 下書き記事
│   ├── published/       # 公開済み記事
│   └── templates/       # 記事テンプレート
├── assets/
│   └── images/          # 画像ファイル
└── README.md
```

## 記事の作成フロー

1. `articles/templates/note-template.md` をコピーして新しい記事を作成
2. `articles/drafts/` フォルダで記事を執筆・編集
3. noteに投稿後、`articles/published/` フォルダに移動
4. 必要に応じて画像は `assets/images/` に保存

## noteのMarkdown対応について

noteは限定的なMarkdown記法に対応しています：

### 対応している記法
- `## 大見出し` (h2)
- `### 小見出し` (h3)  
- `**強調**`
- `> 引用`
- コードブロック (```言語名)
- リスト

### 制限事項
- h1タイトルは記事タイトル入力欄を使用
- h2は存在せず、記事内見出しはh3から始まる
- 一般的なMarkdownの一部機能は未対応

## 使用方法

### 新しい記事の作成
```bash
cp articles/templates/note-template.md articles/drafts/新しい記事.md
```

### 記事の公開後
```bash
mv articles/drafts/記事名.md articles/published/記事名.md
```