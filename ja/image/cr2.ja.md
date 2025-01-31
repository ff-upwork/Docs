{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CR2 ファイル形式 - Canon Raw 2 画像ファイル",
  "description":"CR2 ファイル形式と,CR2 ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "CR2",
  "menu" : {
    "docs" : {
      "identifier":"image-cr2",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## CR2ファイルとは何ですか?

CR2 (Camera RAW 2) ファイルは、キヤノンのデジタル カメラで作成された RAW 画像ファイルです。カメラでキャプチャされた元の未処理のロスレス画像データを保存します。 CR2 ファイル形式は、キヤノンがデジタル カメラ用に開発したもので、RGB 14 ビットまでの高画質な画像を記録できます。これにより、後処理の余地が十分にある高品質の画像が生成されます。 CR2 画像形式は、Canon の 350D、20D、および 1D カメラ モデルで使用されています。 CR2 ファイルは RAW ファイルであり、カメラ情報、レンズ情報、ブラケット情報、ホワイト バランス、その他の設定などの追加のメタデータ情報が含まれています。

## CR2 ファイル形式

CR2 ファイルは、キヤノン独自のファイル形式のバイナリ ファイルとしてカメラのメモリ カードに保存されます。 CR2 ファイル形式は、最初に使用された CRW ファイル形式を置き換え、後で Canon RAW 3 ファイル形式に置き換えられました。 CR2 ファイル形式は、4 つの画像ファイル ディレクトリ (IFD) を持つ [TIFF](/image/tiff/) 仕様に基づいています。

|オフセット |コンテンツ |コメント|
---|---|---|
| |0x0000 |ヘッダー |バイト順、バージョン、および RAW 画像へのオフセットが含まれます|
|計算済み |IFD#0 |この部分には、Makernotes セクションを含む Exif セクションが含まれます。
画像についての情報#0|
|計算された |picture#0 |Jpeg で圧縮された画像の小さいバージョン (元のサイズの 4 分の 1)|
|計算された|IFD#1 |画像#1に関する情報。|
|計算された|画像#1 |Jpeg で圧縮された画像の縮小版|
|計算された|IFD#2 |画像#2に関する情報。
|計算された |picture#2 |圧縮されていない縮小版の画像|
|ヘッダー内| IFD#3| pic#3 原寸RAW画像のご案内|
|計算 |picture#3 |RAW 画像データ、JPEG で可逆圧縮 (RGB データではありません!)|

## CR2 ファイル形式の利点

写真を RAW 形式で保存すると、ホワイト バランスの調整など、写真に対する多くの後処理が可能になります。これははるかに難しく、[JPEG](/image/jpeg/) などの他の画像ファイル形式では品質が大幅に低下します。

## CR2 は JPEG より優れていますか?

CR2 ファイルは、データが失われない未加工のファイルであるため、品質が低下することはありません。一方、JPEG は、ファイルを縮小するために一部のデータを失うため、非可逆画像ファイル形式です。したがって、CR2 ファイルは高品質であり、レタッチや拡張に適しています。

## 参考文献

* [CR2 ファイル形式](http://lclevy.free.fr/cr2/)

