# 本資料のURL

https://github.com/hifivemania/pwa_handson_docs

# 下準備

このハンズオンではNode.jsを用います。各自、最初にインストールしてください。

https://nodejs.org/ja/download/

## プロジェクトベースのダウンロード

ハンズオン用のプロジェクトベースは以下のURLでダウンロードできます。ダウンロードしたら解凍してください。

https://github.com/hifivemania/pwa_handson

解凍後、そのフォルダの中に以下のコマンドを実行します。

```
npm i
```

これで必要なライブラリがインストールされます。

## Webサーバを立ち上げる

ライブラリをインストールすると以下のコマンドでWebサーバが立ち上がります。

```
npm run start
```

Webサーバは http://localhost:3000/ または http://127.0.0.1:3000/ でアクセスできます。

## ファイル構成について

サンプルのプロジェクトは以下のような構成になっています。

```
├── keygen.js （WebPush用のキーファイルを生成します）
├── package.json
├── public （Webブラウザからアクセスするファイルが入っています）
│   ├── icon.png （WebPush用のアイコンファイルです）
│   ├── index.html （TodoアプリのUIです）
│   ├── js（Webブラウザから読み込むJavaScriptファイル群です）
│   │   ├── app.js（Service Workerの処理が記述されています）
│   │   ├── app.push.js（WebPushに関する処理が記述されています）
│   │   └── todo.js （Todoアプリのコードです）
│   ├── manifest.json（アプリ用のマニフェストファイルです）
│   ├── sw.js（Service Workerです）
│   └── vendors（依存ライブラリです）
│       ├── ejs-h5mod.js（テンプレートエンジンejsのファイルです）
│       ├── h5.css（hifive用のCSSです）
│       ├── h5.js（HTML5用のMVCフレームワークです）
│       └── jquery.min.js（jQueryです）
├── push.js（WebPushを配信します）
└── server.js （Webサーバを立てます）
```

## 最初に行ってほしいこと

`public/js/todo.js` を開いて、TODOの値を適当なものに変更してください。データが他の人とかぶらないようにするための処理です。

```js
// これを必ず変更してください
var TODO = 'TODO';
```

## ハンズオンの内容について

資料は大きく分けて3部構成になります。[第1章 アプリの説明](1.md)は共通です。

### 第1部 アプリ化を体験する

- [第2章 マニフェストファイルを作る](2.md)
- [第3章 Service Workerのインストールと有効化](3.md)
- [第4章 Service Workerを使った表示高速化、オフライン対応について](4.md)

### 第2部　Todoアプリのオフライン化

- [第5章 Todoの表示処理をオフライン対応させる](5.md)
- [第6章 Todoの投稿処理をオフライン対応](6.md)

### 第3部 WebPush通知を体験する

- [第7章 Webリモートプッシュ通知を実装する](7.md)

各部は独立していますので、いきなり第2部から体験も可能です。

では[第1章 アプリの説明](1.md)に進みましょう。
