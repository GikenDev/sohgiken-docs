# オーディオ制御

![Author](https://img.shields.io/badge/Author-aKuad-brightgreen)
![Created date](https://img.shields.io/badge/Created-2023%2F09%2F09-blue)
![Last Modified date](https://img.shields.io/badge/Last%20Modified-2023%2F09%2F09-blue)

## HDMI / カメラ音声

HDMI と SDI は、映像とあわせて音声も伝送できます。
ATEM スイッチャ側も、その音声の入力に対応しています。

正面の Preview 選択ボタン上の 'ON' を押して有効化することで、当該の音声入力を Program に送出できます。

![HDMI/SDI audio ON](./media/audio-cam-on.webp ':size=700')

また、その下の 'AFV' (Audio Follow Video) を有効化すると、映像の切り替えに応じて 'ON' が自動で切り替わるようになります。

## XLR 入力

ステージ演出の現場では、出演者マイク音声や投影中の動画音声などを、オーディオミキサーで調整し、会場スピーカーで流す形が主です。
ステージの様子を録画する場合、それらの音声も加える必要が出てきます。

そこで、XLR 端子 (キャノンコネクタとも) の 'ANALOG AUDIO IN' という端子を利用できます。

![XLR input](./media/audio-analog-in.webp ':size=700')

?> XLR 端子は、プロ用途の機器において、ほぼ標準と言えるほど多く採用されている端子です。

XLR 入力の有効/無効は、ATEM Software Control 画面左下の歯車アイコンから開く設定の 'オーディオ' タブから変更できます。

![ATEM Software Control - Config](./media/atem-sc-config.webp ':size=700')

## マイク入力

本体正面の 6.3mm Phone 端子です。
これは、1人での配信での利用を想定した機能と言えます。
ステージ演出での利用にはあまり向きません。

![Mic in](./media/audio-mic-in.webp ':size=700')

有効/無効設定は、XLR 入力と同じ設定画面から変更できます。

## オーディオの制御

ATEM Software Control 画面下の 'オーディオ' から、オーディオミキサが開きます。

![ATEM Software Control - Audio](./media/atem-sc-audio.webp ':size=700')

ここでは 'ON' 'AFV' の切り替えに加え、音量の調整、イコライザ設定などができます。

ただし、ステージ演出の現場で、マイク入力などは別のミキサーで制御する場合、ATEM のミキサー機能を使うことはあまり無いでしょう。
