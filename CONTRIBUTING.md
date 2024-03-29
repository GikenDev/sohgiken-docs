# 記事作成ガイドライン

現時点でどのような形式でページを作成しているかを記します。
何か提案があれば [Issue へ](https://github.com/GikenDev/sohgiken-docs/issues/new/choose)お願いします。

## ファイル構造

`docs` ディレクトリをルートに Web ページが構成されます。
ファイル構造は以下のようになっています。(便宜上アルファベット順になっていません)

```txt
docs/
|- README.md
|- index.html
|- _sidebar.md         ... コース一覧
|- pages/
   |- README.md        ... コース一覧と各コース概要
   |
   |- course-name1/
   |  |- media/        ... 画像ファイル等
   |  |- README.md     ... コース概要
   |  |- _sidebar.md   ... コース内ページ一覧
   |  |- page-name1.md
   |  |- page-name2.md
   |  |- ...
   |
   |- course-name2/
   |- ...
   |
   |- misc/            ... 単発ページ
      |- misc-page1_media/
      |- misc-page1.md
```

## ページ作成のフロー

デスクトップの Git クライアントの使用を想定した手順を示します。

1. 作成・編集内容についての Issue を立てる (少量の編集である場合, 既存リクエストに応える場合は不要)
2. リポジトリをクローンする (初回のみ)
3. 編集内容に関する適当な名前でブランチを作成し、チェックアウトする
4. ページの作成・編集を行い、コミット、プッシュをする
5. プッシュしたブランチで Pull Request を立て、他の編集者に知らせる (本文に 'Close #Issue番号' という一文を含める)
6. 問題なければマージをし、Pull Request を閉じる

> [!NOTE]
> より厳格なリポジトリ管理をする場合、リポジトリのフォークを挟むべきです。
> しかし本リポジトリは、限られた人数しか編集をせず、厳格な管理は必要でないと考えているため、フォークを挟まない工程を記しています。

必ずしも上と全く同じ手順である必要はなく、以下を満たしていれば OK です。

* Issue 作成をする (少量の編集であれば不要)
* Pull Request 作成をする
* (要するに) main ブランチへの直コミットをしない

## 編集チェックリスト

ファイル構造は既存ページを参考にしてください。

### 新規コース

* Author, Create, Last Modified バッジをページ先頭に付けた (README, _sidebar 除く)
* `docs/pages/README.md` にコース名 (リンク付)、概要を追加した
* `docs/_sidebar.md` にコース名 (リンク付) を追加した
* `docs/pages/<course-name>/README.md` を作成し、コースの概要が書かれている
* `docs/pages/<course-name>/_sidebar.md` を作成し、コース内ページ一覧が過不足なく書かれている

### 新規単発ページ

* Author, Create, Last Modified バッジをページ先頭に付けた
* `docs/pages/misc/README.md` にページ名 (リンク付) を追加した
* `docs/pages/misc/_sidebar.md` にページ名 (リンク付) を追加した

### 既存ページ編集

* Last Modified バッジの日付を更新した
* (タイトル変更時) _sidebar などの表示を更新した

## 作成者・日付バッジ

各ページの頭に、このようなバッジを貼ってあります。

![Author](https://img.shields.io/badge/Author-aKuad-brightgreen)
![Created date](https://img.shields.io/badge/Created-2023%2F04%2F05-blue)
![Last Modified date](https://img.shields.io/badge/Last%20Modified-2023%2F04%2F05-blue)

作成者が分かることで問い合わせをしやすくする、編集日が分かることで情報の古さが分かるようにする意図があります。

shields\.io というフリーのサービスを使用しており、以下のように書くだけでバッジを貼ることができます。

```md
![Author](https://img.shields.io/badge/Author-aKuad-brightgreen)
![Created date](https://img.shields.io/badge/Created-2023%2F04%2F05-blue)
![Last Modified date](https://img.shields.io/badge/Last%20Modified-2023%2F04%2F05-blue)
                                                                   ^~~~   ^~   ^~
この数字を変えることで 年/月/日 を指定できる
'%2F' は '/' と表示される
```

## 画像について

### 解像度

縦または横の解像度が 2000px 以上ある場合は、ある程度縮小して使用しています。

画面の解像度は普通はフル HD (1920 x 1080) 程度で、画像はその上にさらに小さく表示されます。
画像の解像度が余計に高いと、ファイルサイズが大きくなり、Web ページ表示の際に通信を圧迫してしまい、表示速度に影響を及ぼします。

よって 2000px 以上の解像度は普通は不要であるため、縮小しています。

### フォーマット

画像フォーマットは Webp または Svg を使用しています。

| ケース | フォーマット |
| --- | --- |
| Draw\.io など Svg 出力対応のソフトで書いた図 | Svg - SVGO で最適化処理 |
| 写真など | Webp - Lossy (Quality 80) |
| スクリーンショットや図 | Webp - Lossless |

Webp は比較的新しいフォーマットで、JPEG や PNG よりもファイルサイズを小さくできます。
モダンなブラウザはすでに表示に対応しているため、Web ページで問題なく使用できます。

Webp の作成や編集は、GIMP など高機能な画像エディタで、変換は Web 上でもできます。

Svg はベクター形式と呼ばれるフォーマットで、ピクセルにせず線や点の図形情報が保存されるため、解像度が落ちる心配がありません。

Svg ファイルは、SVGO というソフトで最適化 (品質をほぼ落とさずファイルサイズを削減) することができます。
コマンドラインで [`npm` からインストール](https://github.com/svg/svgo#installation)、または [Web 上でも利用できます。](https://svgomg.net/)

> [!NOTE]
> オンラインの変換サイトで変換をする場合、**「アップロードされることはありません (without uploading)」と明記されている**サイトを使用することをオススメします。
> アップロード/ダウンロードに時間がかからないため、それから管理者にファイルを覗かれる心配がないためです。

### 表示サイズ指定

画像の形状や解像度によっては、ページに非常に大きく表示され、画面を専有してしまう恐れがあります。

Docsify では、以下のように記述することで画像の表示サイズ (横幅) を指定できます。

```md
サイズ指定なし
![代替えテキスト](./media/image-name.webp)

サイズ指定あり
![代替えテキスト](./media/image-name.webp ':size=700')
```

以下にサイズ指定の目安を示します。

| ケース | サイズ |
| --- | --- |
| 縦に細長い画像やあまり目立たせる必要の無い画像 | `':size=300'` |
| 一般的な写真 | `':size=500'` |
| スクリーンショットや図など、細かい描画があるもの | `':size=700'` |
