# 静止画を使う

![Author](https://img.shields.io/badge/Author-aKuad-brightgreen)
![Created date](https://img.shields.io/badge/Created-2023%2F09%2F03-blue)
![Last Modified date](https://img.shields.io/badge/Last%20Modified-2023%2F09%2F03-blue)

開演前や休憩時間中などに、用意した静止画を映したいことがあるかもしれません。
しかし、その映像を出すためにわざわざ PC など映像出力機器を用意するのは少々手間です。

そこで、ATEM スイッチャ内蔵の静止画メモリと Media Players を使う手があります。

## 静止画を登録する

このような静止画を使用したいとします。

![Still sample](./media/still-sample.webp ':size=300')

まずは ATEM Software Control 画面下の 'メディア' を開きます。

![ATEM Software Control - Media](./media/atem-sc-mediaplayer.webp ':size=700')

20枚の静止画スロットが開きます。
ここで現在登録している静止画を確認したり、変更したりできます。

![Media list](./media/still-list.webp ':size=700')

画面左のローカルライブラリから画像ファイルを選択、または画像ファイルをドラッグ&ドロップでスロットに画像をセットすることができます。

これで ATEM 内蔵メモリに静止画を登録できました。

## 静止画を送出する

静止画は 20枚まで登録できますが、同時に送出できるのはそのうち 2枚だけです。

まずは 'スイッチャー' 画面に戻ります。

![ATEM Software Control - Switcher](./media/atem-sc-switcher.webp)

右側の 'Media Players' メニューで、Media Player1 / 2 それぞれで 20枚中どの静止画を送出するかを選択します。

![Media player select](./media/still-select.webp ':size=700')

ATEM Software Control のプレビュー中の 'MP1' 'MP2' ボタンで、プレビューに静止画を送出。

![Media player preview - PC](./media/still-preview.webp ':size=700')

本体ボタンでは 'MP1' 'MP2' で選択できます。

![Media player preview - Body button](./media/still-body-button.webp ':size=700')

![Media player preview - Multiview](./media/still-multiview.webp ':size=700')

あとは Program と切り替えるだけです。
これで、HDMI や SDI の映像入力のように、静止画を送出できました。

?> テロップなどが描かれた静止画を他映像に合成し、より高度な演出をするには[映像を合成する](./video-composite.md)を参照
