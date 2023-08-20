# PC を接続する

![Author](https://img.shields.io/badge/Author-aKuad-brightgreen)
![Created date](https://img.shields.io/badge/Created-2023%2F08%2F19-blue)
![Last Modified date](https://img.shields.io/badge/Last%20Modified-2023%2F08%2F19-blue)

ATEM Software Control という PC ソフトから ATEM スイッチャを操作することもできます。
本体ボタンでの操作に比べ、アップストリームキーやスチル設定など、より高度な制御をすることができます。

!> 本体の IP アドレスなど、一部は本体ボタン操作でないと設定できない項目があります。

## ATEM Software Control をインストールする

[ATEM Software Control](https://www.blackmagicdesign.com/products/atemmini/software) は、Blackmagic Design 社から公式に提供されている、ATEM スイッチャ制御ソフトです。

[Blackmagic Design 社のサポートページ](https://www.blackmagicdesign.com/support/family/atem-live-production-switchers)からダウンロードできます。

!> ATEM スイッチャ本体に付属する SD カードからインストールすることもできますが、最新バージョンでないため推奨できません。ネットからダウンロードすることを推奨します。

!> ATEM Software Control は、インストーラのファイルサイズが 1GB 以上と大きく、インストールにも時間がかかります。事前に準備しておきましょう。

## IP アドレス設定

USB で簡単に接続･･･とできればいいのですが、そうはいかず LAN での接続が必要になります。

LAN について詳しく説明すると長くなってしまうので省略します。
ここでは「有線接続, 固定 IP」の方法で進めます。(最も単純な構成で済むため)

!> トラブル回避のため、コントローラとして使う PC はネット回線 (もとい他のネットワーク) に接続しないでください。

以下のように、ATEM スイッチャと PC の LAN 設定をしてください。

* IP アドレス (ATEM): 192.168.0.2 〜 192.168.0.254
* IP アドレス (PC): 固定IP, 192.168.0.2 〜 192.168.0.254
  * ※ ATEM スイッチャと PC の IP アドレスを重複させないように
* サブネットマスク: 255.255.255.0
* デフォルトルート: 192.168.0.1

ATEM スイッチャの IP アドレスは、本体の MENU から設定できます。

?> ATEM スイッチャ本体の設定方法は[本体設定をする](./body-config)を参照

PC の IP アドレスの指定方法は、使用 OS 別で調べてください。

## LAN ケーブルをつなぐ

ATEM スイッチャにもあるこの端子が LAN ポートです。

![LAN Port](./media/lan-port.webp ':size=200')

接続にあたっては、PC にもこの端子が必要です。
しかし、薄型軽量のノート PC ではあまり見かけなくなってきています。
その場合は、変換ケーブルを用意してください。

!> 無線で接続する方法もありますが、無線アクセスポイントが必要です。

ATEM スイッチャと PC を、LAN ケーブルで接続します。
LAN ハブを経由してもよいです。

## ATEM Software Control を起動する

接続したら、PC の ATEM Software Control を起動します。

IP アドレスの入力が出てきたら、上で ATEM スイッチャに設定した IP アドレスを入力します。

下のような画面になれば接続成功です。

![ATEM Software Control UI](./media/atem-sw-ui.webp ':size=500')
