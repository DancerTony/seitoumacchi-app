# 政党マッチ度診断（13項目+自由記入）（PWA 配布パッケージ）

このフォルダをそのまま **静的ホスティング**（HTTPS）に置くと、URLで動くPWAになります（「ホーム画面に追加」可）。

## 中身
- `index.html` : アプリ本体（元HTMLをPWA対応にしたもの）
- `manifest.json` : PWA設定
- `service-worker.js` : オフライン用キャッシュ
- `icons/` : アイコン（192/512 + maskable）

## すぐ公開する方法（おすすめ）
### 1) GitHub Pages
1. GitHubで新規リポジトリ作成（Public推奨）
2. このフォルダ内のファイルをリポジトリ直下にアップロード
3. Settings → Pages → Branch を `main` / root にして Save
4. 表示されたURLにアクセス → 端末で「ホーム画面に追加」

### 2) Netlify（ドラッグ&ドロップ）
1. Netlifyにログイン
2. Sites → Add new site → Deploy manually
3. **このフォルダをZIPのまま** ドロップ（またはフォルダ内をドロップ）
4. 表示URLにアクセス

### 3) ローカル確認（簡易サーバ）
- Python:
  ```bash
  python -m http.server 8000
  ```
  http://localhost:8000 へアクセス

※ PWA（Service Worker）は `file://` 直開きでは動きません。必ずサーバ経由で確認してください。
