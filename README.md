# sohgiken-docs

総技研のノウハウなどについてのドキュメントをストックするものです。

docsify により、markdown で記述された文書を静的 Web ページとして GitHub Pages で公開しています。

<https://gikendev.github.io/sohgiken-docs/>

## プレビュー方法

### npm 及び docsify のインストール (初回のみ)

1. npm をインストールする (環境によって導入方法は様々, 詳細は公式ページで)
2. npm コマンドで docsify をインストールする

2\. について、必要に応じて `-g` オプションを付与し、全領域で docsify コマンドを利用できるようにします。

```sh
npm install -g docsify-cli
```

### docsify の起動

docsify インストール済みの状態で、以下を実行します。

1. 本リポジトリをクローンする (初回のみ)
2. `docsify serve` コマンドで、本リポジトリの docs ディレクトリを指定し、実行する
3. ブラウザで <http://localhost:3000> にアクセスする

2\. について、リポジトリのルートにカレントがあるとき、コマンド例は以下のようになります。

```sh
docsify serve ./docs
```
