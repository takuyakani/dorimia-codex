# 📚 ドリミア大典 モバイル閲覧パッケージ

このディレクトリは、スマートフォン等でインターネット経由で常時閲覧できるようにビルドされた『ドリミア大典』の静的Webサイトパッケージです。

## 特徴
- **暗号化保護**: 大典データ (`codex_data.enc`) は AES-256-GCM で暗号化されています。
- **閲覧合言葉**: ページ初回表示時に設定した合言葉を入力してください（端末に記憶可能）。
- **スマホ最適化**: スマートフォンでの片手操作・横スクロールカテゴリ・全画面羊皮紙詳細表示に対応。

## GitHub Pages での公開手順（無料・常時稼働）

1. GitHub で新規リポジトリを作成します（例: `dorimia-codex`）。
   - ※大典データは暗号化されているため、パブリックリポジトリでも平文の世界観データが第三者に漏れることはありません。
2. この `dist_codex/` ディレクトリの中身をリポジトリにプッシュします。
   ```bash
   cd dist_codex
   git init
   git add .
   git commit -m "Deploy Dorimia Codex for mobile"
   git branch -M main
   git remote add origin https://github.com/<あなたのユーザー名>/dorimia-codex.git
   git push -u origin main
   ```
3. GitHub リポジトリの **Settings > Pages** を開きます。
4. **Build and deployment** の Source で **Deploy from a branch** を選択し、Branch を `main` / `/(root)` に設定して「Save」を押します。
5. 数分後に発行されるURL（例: `https://<あなたのユーザー名>.github.io/dorimia-codex/`）にスマートフォンのSafariやChromeからアクセスします。
6. 設定した合言葉を入力すると、いつでも大典が閲覧可能になります！
   - ※スマホのブラウザで「ホーム画面に追加」を行うと、アプリのように全画面起動できます。
