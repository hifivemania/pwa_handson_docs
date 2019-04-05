**本資料のURL**　https://github.com/hifivemania/pwa_handson_docs

## プロジェクトベースのダウンロード

ハンズオン用のプロジェクトベースは以下のURLでダウンロードできます。ダウンロードしたら解凍してください。

https://github.com/hifivemania/pwa_handson

解凍後、そのフォルダの中に以下のコマンドを実行します。Node.jsを事前にインストールしてください（※バージョンは8以上を使ってください）。

```
npm i
```

これで必要なライブラリがインストールされます。

### Webサーバを立ち上げる

ライブラリをインストールすると以下のコマンドでWebサーバが立ち上がります。

```
npm run start
```

Webサーバは http://localhost:3000/ または http://127.0.0.1:3000/ でアクセスできます。

## ファイル構成について

サンプルのプロジェクトは以下のような構成になっています（一部）。Monacaの場合は public を www と読み替えてください。

```
├── keygen.js（WebPush用のキーファイルを生成します）
├── public （Webブラウザからアクセスするファイルが入っています）
│   ├── icon.png（WebPush用のアイコンファイルです）
│   ├── index.html（TodoアプリのUIです）
│   ├── js（Webブラウザから読み込むJavaScriptファイル群です）
│   │   ├── app.js（Service Workerの処理が記述されています）
│   │   ├── app.push.js（WebPushに関する処理が記述されています）
│   │   └── todo.js（Todoアプリのコードです）
│   ├── manifest.json（アプリ用のマニフェストファイルです）
│   ├── sw.js（Service Workerです）
│   └── vendors（依存ライブラリです）
│       ├── bootstrap（UIフレームワークのBootstrapです）
│       │   ├── css
│       │   │   └── bootstrap.min.css
│       │   └── js
│       │       └── bootstrap.bundle.min.js
│       ├── hifive
│       │   ├── ejs-h5mod.js（テンプレートエンジンejsのファイルです）
│       │   ├── h5.css（hifive用のCSSです）
│       │   ├── h5.dev.js（HTML5用のMVCフレームワークです。こちらは開発用です）
│       │   ├── h5.js（HTML5用のMVCフレームワークです）
│       │   └── h5.js.map
│       └── jquery（jQueryです）
│           └── jquery.min.js
├── push.js（WebPushを配信します）
└── server.js （Webサーバを立てます）
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

各部は独立していますので、第2部から体験も可能です。では[第1章 アプリの説明](1.md)に進みましょう。
