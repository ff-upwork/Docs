{
  "date" : "2019-10-11",
  "keywords" :["psbファイル","psbファイル形式","psbファイルとは","ファイル","psb例","psbファイル拡張子","拡張子","形式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSB - Photoshop Big Image File Format",
  "description":"PSB ファイル形式と,PSB ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "PSB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## .PSB オプション番号
Adobe Photoshop は、ファイルを 2 つの形式で保存します。サイズが 30,000 x 30,000 ピクセルのファイルは PSD 拡張子で保存され、PSD より大きい最大 300,000 x 300,000 ピクセルのファイルは「Photoshop Big」と呼ばれる PSB 拡張子で保存されます。より具体的には、PSB ファイルは最大 4 EB (42 億 GB 以上) のサイズで、画像の高さと幅が最大 300,000 ピクセルです。一方、PSD は最大 2 GB で、画像サイズは 30,000 ピクセルです。

PSB は Photoshop のラージ フォーマット サイズとしても知られており、レイヤー、エフェクト、フィルターなどのすべての Photoshop 機能をサポートしています。Photoshop は PSB ファイルを [PSD](/image/psd/)、[JPG](/image/jpeg/) に変換できます。 、[PNG](/image/png/)、[EPS](/page-description-language/eps/)、[GIF](/image/gif/)、その他の形式も同様です。 Photoshop の環境設定ダイアログ ボックスのファイル処理ペインの機能を有効にすると、Photoshop の大きなドキュメント形式を使用できます。

## ファイル形式情報 ##

Photoshop ファイル形式は、セクション間を移動するための多くの長さマーカーを持つ 5 つの主要な部分に分かれています。

|ファイル形式
---|
|ファイル ヘッダー
|カラーモードデータ
| |画像リソース
|レイヤーとマスクの情報
|((((
画像データ
))))

### ファイルヘッダー ###

ファイル ヘッダーは 26 バイトの固定長で、画像の基本的なプロパティが含まれています。

BYTE シグネチャ [4] – 「8BPS」に相当。

WORD バージョン [2] – バージョン番号、PSD # 1、PSB # 2。

BYTE 予約済み [6] – 予約済みで、常にゼロです。

WORD チャネル [2] – アルファ チャネルを含む画像内のカラー チャネルの数。値の範囲は 1 ～ 56 です。

LONG 行 [4] – ピクセル単位の画像の高さ、PSD 1 ～ 30,000、PSB 1 ～ 300,000。

LONG 列 [4] – ピクセル単位の画像の幅、PSD 1 ～ 30,000、PSB 1 ～ 300,000。

WORD 深度 [2] – チャネルあたりのビット数。サポートされている値は、1、8、16、および 32 です。

WORD モード [2] – ファイルのカラー モード。

#### モードの説明 ####


|モード|説明
---|---|
|0|ビットマップ (モノクロ)
|1|グレースケール
|2|索引付き
|3|RGB
|4|CMYK
|7|マルチチャンネル
|8|ダブルトーン (ハーフトーン)
|9|ラボ

### カラーモードデータ ###

ファイル ヘッダー セクションの後に、カラー モード データ セクションが続きます。ブロックは、ブロックの長さをバイト単位で示す LONG Number で始まります。カラー モード データの構造は次のとおりです。

4 バイト – 次のカラー データの長さ。

変数 – カラーデータ

ヘッダー セクションのモード フィールド値が Indexed Color または duotone でない場合、ブロックの長さは 0 になり、長さフィールドの後にデータはありません。

インデックス付きカラー イメージの場合、長さは 768 バイトになり、256 カラー パレットが含まれます。ダブルトーンの場合、データには画面パラメーターとその他の関連情報が含まれます。

### 画像リソース ###

カラー モード データ セクションに続く 3 番目のブロックは、イメージ リソース セクションです。最初の 4 バイトは、ブロックの長さを指定する LONG 数値で、その後に一連のリソース ブロックが続きます。画像リソース ブロックの構造は次のとおりです。

BYTE タイプ [4] – 署名「8BIM」

WORD ID [2] – イメージ リソース ID。参照リンクから参照できるリソース ID のリストがあります。

BYTE Name [Variable] – Name: Pascal 偶数長の文字列。 ** **

LONG サイズ [4] – 後続のリソース データの実際のサイズ。

BYTE データ [変数] – リソース データ。均一なサイズにするためにパッドが入っています。

リソース形式の一部を以下で簡単に説明します。

**グリッドとガイドのリソース形式:** グリッドとガイドの情報はリソース ブロックに格納されます。これらのリソース ブロックには、16 バイトのグリッドとガイド ヘッダーが含まれ、その後にガイド情報の 5 バイト ブロックが続きます。

**サムネイル リソース フォーマット:** サムネイル情報は、28 バイトのヘッダーと RGB の JFIF サムネイルで構成されるプレビュー表示用の画像リソース ブロックに格納されます。

**カラー サンプラー リソース フォーマット:** カラー サンプラー情報は、8 バイトのヘッダーの後にカラー サンプラー情報の可変長ブロックが続く画像リソース ブロックに格納されます。

### レイヤーとマスク情報 ###

4 番目のブロックはレイヤーとマスクの情報ブロックで、レイヤーとマスクに関する情報が含まれています。レイヤー情報が最初に保存され、次にマスク情報が保存されます。

**レイヤー情報:** レイヤー情報は、レイヤー情報の長さを示す LONG 値で始まります。その後に続くレイヤ レコードの数を示す WORD 値 count があります。

[8] – レイヤーの長さ

[2] – レイヤー数

[変数] – 各レイヤーに関する情報。

[変数] – チャンネル画像データ。** **

**マスク情報:** マスク構造の形式は次のとおりです。


|データ構造|フィールド名|説明
---|---|---|
|単語|オーバーレイの色空間| (文書化されていません)
|バイト[8]|カラーコンポーネント| 4x2 バイトのカラー コンポーネント
|単語|不透明度| 0#透明、1#不透明
|バイト|種類| 0#反転、1#保護、128#保存値を使用
|バイト|パディング|ゼロに設定

### 画像データ ###

最後のセクションには、画像のピクセル データが含まれます。画像データはプレーンの一連のシーケンスとして保存されます。つまり、最初にすべての赤のデータ、次にすべての緑のデータなどです。各ラインの先頭にある WORD は、各スキャン ラインに関連するバイト単位のサイズを示します。

[2] – 圧縮方法:

[Variable] – RRRR、GGGG、BBBB などの平面順序の画像データ。

圧縮方法:

0 – Raw 画像データ

1 – RLE 圧縮

2 – 予測なしの圧縮

3 – 予測付きの圧縮

## 参照 ＃＃

* [PSB ファイル形式 - Adobe 提供](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)
* [PSB - ウィキペディア](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)

