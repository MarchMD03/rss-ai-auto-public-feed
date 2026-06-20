# rss-ai-auto-public-feed

AIが選別・要約したIT記事を配信する、個人向けのRSSフィードです。

## 公開URL

```
https://marchmd03.github.io/rss-ai-auto-public-feed/personal-feed.xml
```

このURLをRSSリーダーに登録してください。

## 仕組み

- Routine などの自動化ツールが定期的に `personal-feed.xml` を生成し、`main` ブランチへ push します。
- GitHub Pages（Deploy from a branch / `main` / `/ (root)`）が再ビルドし、上記URLで配信します。
- `.nojekyll` を置いて Jekyll を無効化し、XML をそのまま配信しています。

## セットアップ手順

1. このリポジトリの `main` ブランチに最初のコミットを入れる（本コミット）。
2. Settings → Pages → Source: 「Deploy from a branch」→ Branch: `main` / フォルダ `/ (root)` → Save。
3. Routine の Repositories にこのリポジトリを追加し、push 権限を付与する。
4. テスト実行 → Routine が `personal-feed.xml` を `main` に push → Pages が再ビルド → 公開URLで配信。
