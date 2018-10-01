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

### ファイルの配置

#### mdファイル

- `docs`配下に配置する
- 必要に応じてディレクトリをきることも可能

#### サイドメニュー

- `docs/.vuepress/config.js`に定義する
- サンプル参照
    - [/docs/.vuepress/config.js](./docs/.vuepress/config.js)

#### 画像の配置

- `docs/.vuepress/public/`配下に配置することでmdファイルから使用することができる

```
// ここに画像があるとする
docs/.vuepress/public/images/logo.png
```

```md
// mdファイルからこのようにしてpublic配下のファイルを呼ぶことができる
![logo](/images/logo.png)
```

#### テーマの変更

- `docs/.vuepress/override.styl`でテーマカラーを変更することができる

```styl
// サンプル
$accentColor = #28A6CF
$textColor = #2c3e50
$borderColor = #eaecef
$codeBgColor = #282c34
```