# Photo Shelf 公開用

生写真の所持枚数、収集対象、ほしいもの、入手予定、提供可能枚数を管理するVite + Reactアプリです。

## 重要
- データは利用者ごとに、その端末・ブラウザの localStorage に保存されます。
- 別端末へ自動同期されません。
- ブラウザのサイトデータを削除すると消える可能性があります。
- 定期的に「バックアップ」から軽量版JSONを保存してください。

## ローカル実行
```bash
npm install
npm run dev
```

## 本番ビルド
```bash
npm run build
npm run preview
```
成果物は `dist/` に生成されます。

## Azure Static Web Apps
1. GitHubの新規リポジトリへ全ファイルをアップロードします。
2. Azure Portalで Static Web App を作成し、リポジトリと `main` ブランチを接続します。
3. Build Presets は React、App location は `/`、Output location は `dist`、API location は空欄です。
4. Azureが作成したデプロイトークンを、GitHub Actionsのシークレット `AZURE_STATIC_WEB_APPS_API_TOKEN` に設定します。
5. `main` へpushすると自動公開されます。

初回データは空です。各利用者が自分の端末で登録します。
