# 主な端子と映像入出力フロー

![Author](https://img.shields.io/badge/Author-aKuad-brightgreen)
![Created date](https://img.shields.io/badge/Created-2023%2F08%2F20-blue)
![Last Modified date](https://img.shields.io/badge/Last%20Modified-2023%2F09%2F10-blue)

まず、ATEM スイッチャにどのような端子があるか確認してみましょう。

![ATEM Interface connectors](./media/interface-conn.webp ':size=700')

いろいろありますが、基本となる以下の端子について説明していきます。

* HDMI INPUTS (1~4)
* SDI INPUTS (5~8)
* PGM (Program)
* AUX
* MULTI-VIEW

?> SDI は、主に業務用途で使われている映像信号規格の 1つで、HDMI より長い距離を伝送できる特徴があります。

HDMI は、主に PC やゲーム機の映像入力に。SDI は、主にカメラの映像入力に使用されます。

Program は、最終的なメイン出力です。

AUX は、各入力や出力から任意の映像を 1つ選んで出力できます。特定の出力を別で記録したり、モニタリングしたりするのに使えます。

MULTI-VIEW は、各入力、Preview、Program を 1画面で確認できる出力です。
この画面を見ながら操作をするのが基本です。

![ATEM Multi view](./media/atem-multi-view.webp ':size=700')

?> Multi view の映像配置は[変更することができます](./custom-multiview.md)。

映像入力から出力までを図にすると、以下のようになります。

![ATEM Video flow diagram](./media/atem-videoio-draw.svg ':size=700')

?> Still 1~20 の詳細は[スチルを使う](./use-still)を参照

?> Color Bars はカラーバー、Black (BLK) は黒単色の静止画入力です。この静止画は変更できません。

スイッチングで中心となるのは、Program と Preview です。
次の[基本的なスイッチング操作](./basic-switching)のページで説明します。
