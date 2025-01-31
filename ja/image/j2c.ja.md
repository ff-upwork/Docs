{
  "date" : "2019-10-11",
  "keywords" :[ "j2c ファイル", "j2c ファイル形式", "j2c ファイルとは", "ファイル", "j2c の例", "j2c ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"J2C",
  "description":"J2C ファイル形式と,J2C ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "J2C",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-14"
}

## .J2C オプション番号

拡張子が .j2c のファイルは、JPEG ファイル形式の変形であり、ウェーブレット圧縮で圧縮されています。 JPEG 2000 ファイル形式とほぼ同じマーカーとセグメントのシステムを備えています。 J2C ファイル形式は、非可逆圧縮と可逆圧縮の両方をサポートする JPEG 2000 スタンドのパート 1 で定義されているとおりです。 JPEG 2000 コードストリームは、[JP2](/image/jp2/) または別のファイル形式に埋め込むように設計されていますが、単独でファイルに表示される場合もあります。 J2C ファイルは、Adobe Photoshop 2020、Adobe Illustrator 2020、および Corel Paintshop Pro を使用して開くことができます。

## J2C ファイル形式

J2C ファイル形式は、多くの場合 .jp2 および .jpc として保存される JPEG 2000 の形式と同じです。これにより、J2C ファイルは、標準 12234-1 が Exif タグと XML コンポーネント間の参照として使用される XML 形式でメタデータをエンコードする同じアプローチに従います。これは、アニメーション メカニズムとコード ストリーム構成を 1 つの画像に結合する JPEG 2000 part-2 拡張によってさらに改善されます。このような拡張ファイル形式のファイルは、[.jpx](/image/jpx/)として保存されます。

### JPEG2000 ファイルのレイアウト

JPEG2000 は、拡張可能なファイル フォーマットへの準拠に基づいて、さまざまなアプリケーションをサポートします。最も単純なタイプには 1 つの画像を含めることができますが、より複雑なタイプには一連の画像を含めることができ、互いに積み重ねたり、時間ベースの順序で並べたりすることができます。

#### JP2 ボックス
これは、JP2 ファイル形式の最上位のビルディング ブロックであり、ヘッダーにタイプ フィールドと長さフィールド、およびデータ セクションが含まれています。ボックスの最も注目すべきタイプは、連続コードストリーム ボックスです。このボックスは、データ セクションに JPEG2000 コードストリームを格納します。

#### JPEG2000コードストリーム

JPEG2000 CodeStream は、JPEG2000 圧縮イメージをデコードするために必要な一連のバイトです。ファイルにこのコードストリーム以外のものが含まれていない場合、それは未加工のコードストリーム ファイルと呼ばれます。通常、JPEG コードストリームは、JPEG2000 圧縮アルゴリズムを画像に適用したものですが、これが唯一の方法ではありません。

#### タイルパーツ ####

JPEG2000 でエンコードされた画像は、パケットと呼ばれるデータ単位の集まりです。これらのパケットは、タイル パーツと呼ばれるパケット グループ内のコードストリームで維持されます。画像をエンコードする前に、エンコーダーは画像をタイルと呼ばれるブロックの長方形のグリッドに分割し、各タイルは他のタイルに関係なく個別にエンコードされます。

{{< figure src="../JPEG2000_Codestream.png" alt="JPEG2000 ファイル形式" >}}

## J2C 圧縮
JPEG 2000 は、ビューアが画像を表示するビューポートまたはウィンドウに表示されるピクセルが比較的少ないという事実に基づいて、ウェーブレット圧縮テクノロジを使用して高速化します。これは、非常に大きなサイズの画像 (ギガバイト単位) の場合、数メガバイトのピクセルしか画面に表示されないという事実によって強調されます。これにより、表示ピクセルにデータを入力するために必要な画像データの部分のみをすばやく取得してレンダリングできます。これには、必要な画像をその場で作成するための画像フェッチ メカニズムを高速化するための高速解凍テクノロジも必要です。

J2C は、高速解凍を利用して、ピクセル データに必要な情報のみをフェッチし、可視イメージの一部を画面にすばやくレンダリングします。 J2C は、主にデータの表示用に設計されており、編集用ではありません。

## J2C ID
JPEG 2000 ファイルには署名バイト「FF 4F FF 51」があります。

### MIME タイプ
JPEG 2000 ファイル用に登録されている MIME タイプには、次のものがあります。
*画像/j2c
※画像/jpx
※画像/jpm
* ビデオ/mj2

## JPEG 規格の改良点
JPEG 標準からの改善点は次のとおりです。
* 優れた圧縮性能
* 複数の解像度表現
* ピクセルと解像度の精度によるプログレッシブ伝送
*ロスレスまたはロッシー圧縮の選択
* エラー耐性、柔軟なファイル形式
* ハイ ダイナミック レンジのサポート
* サイド チャネルの空間情報

## 参照 ##
* [タウブマン、デビッド。マーセリン、マイケル (2012)](https://books.google.com/books?id=y7HeBwAAQBAJ&pg=PA402)

