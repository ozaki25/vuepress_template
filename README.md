# Vuepress Template

## 使い方

### 雛形のクローン

```bash
git clone git@github.com:ozaki25/vuepress_template.git your-text-name
cd your-text-name
rm -rf .git README.md
git init
git add .
git commit -m "init"
```

### 開発モード

- 開発モードで起動すると`localhost:8080`でプレビューできる

```bash
npm i # or yarn
npm start # or yarn start
# open http://localhost:8080
```

- `docs`配下のmdファイルを修正すると自動でブラウザがリロードされる

### 本番モード

- ビルドすると`public`にhtml, css, jsが生成される

```bash
npm run build # or yarn build
```

- `public`配下をWebサーバ等にデプロイすればコンテンツを公開できる
- nowのセットアップができていれば`now`コマンドで即座にデプロイできる

```bash
now
```

- buildした成果物をローカルで動作確認するには`http-server`が便利

```bash
npm i -g http-server
http-server ./public
# open http://localhost:8080
```

### ファイルの配置

#### mdファイル

- `docs`配下に配置する
- 必要に応じてディレクトリをきることも可能

#### サイドメニューの設定

- `docs/.vuepress/config.js`に定義する
- サンプル参照
    - [/docs/.vuepress/config.js](./docs/.vuepress/config.js#L4)

#### 画像の配置

- 画像ファイルは`docs/.vuepress/public/`配下に配置することでmdファイルから使用することができる

```
// ここに画像があるとする
docs/.vuepress/public/images/logo.png
```

```md
// mdファイルからこのようにしてpublic配下のファイルを呼ぶことができる
![logo](/images/logo.png)
```

#### テーマの変更

- `docs/.vuepress/styles/palette.styl`でテーマカラーを変更することができる

```styl
// サンプル
$accentColor = #28A6CF
$textColor = #2c3e50
$borderColor = #eaecef
$codeBgColor = #282c34
```

### その他

- 公式サイトが充実しているのでそちらを参照
    - [https://vuepress.vuejs.org/](https://vuepress.vuejs.org/)
