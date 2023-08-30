# 基本的なスイッチング操作

![Author](https://img.shields.io/badge/Author-aKuad-brightgreen)
![Created date](https://img.shields.io/badge/Created-2023%2F08%2F30-blue)
![Last Modified date](https://img.shields.io/badge/Last%20Modified-2023%2F08%2F30-blue)

## 基本となる操作手順

映像入出力フローの図を再掲します。

![ATEM Video flow diagram](./media/atem-videoio-draw.svg ':size=700')

スイッチングで中心となるのは、Program と Preview です。
基本となるスイッチング操作の手順は次の通り。

1. Preview 映像を選択する
2. Preview が目的の映像かを確かめる
3. Preview と Program をスイッチする

Preview で映像を確かめてから Program と切り替えることで、意図しないメイン出力になってしまうのを防ぐことができます。
なので、Program を直接操作して映像を切り替えるのは好ましくありません。

## 切り替え演出

切り替えの演出は、CUT と AUTO の 2つに区分されます。

CUT は、演出なく瞬時に映像を切り替えます。

![Transition image - CUT](./media/trans-cut.webp ':size=700')

AUTO は、指定の映像効果を指定時間かけて緩やかに映像を切り替えます。
下図は 'MIX' 効果のイメージです。

![Transition image - MIX](./media/trans-mix.webp ':size=700')

## 本体ボタンでの切り替え

![Machine interface](./media/interface-buttons.webp ':size=700')

白いボタン 1〜8 で Preview 映像の選択をします。
その右側にある 'CUT' 'AUTO' ボタンで切り替えを実行できます。

## ATEM Software Control (PC) での切り替え

![PC interface](./media/atem-sw-ui.webp ':size=700')

プレビューボタン CAM1〜8 で Preview 映像の選択をします。
その右側にある 'トランジションスタイル' の 'CUT' 'AUTO' ボタンで切り替えを実行できます。

また、'トランジションスタイル' 内の 'MIX' 'DIP' 'WIPE' は、映像効果の指定です。
'AUTO' を押す前に選びます。
