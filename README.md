# Vuepress Template

## 使い方

### セットアップ

- vuepressをglobalにインストール

```bash
npm i -g vuepress
vuepress -V
# 0.14.4
```

### 開発モード

- 開発モードで起動すると`localhost:8080`でプレビューできる

```bash
npm start # or yarn start
# open http://localhost:8080
```

- mdファイルを修正すると自動でブラウザがリロードされる

### 本番モード

- ビルドすると`docs/.vuepress/dist`にhtml/css/jsが生成される

```bash
npm run build # or yarn build
```

- `docs/.vuepress/dist`配下をWebサーバ等にデプロイする
