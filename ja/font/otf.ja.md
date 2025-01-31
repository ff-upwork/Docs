{
  "date" : "2020-08-20",
  "keywords" :[ "otf ファイル", "otf ファイル形式", "otf ファイルとは", "ファイル", "otf の例", "otf ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTF - TrueType フォント ファイル形式",
  "description":"OTF ファイル形式と,OTF ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "OTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## .OTF ファイルとは何ですか?

拡張子が .otf のファイルは、OpenType フォント形式を指します。 OTF フォント形式はよりスケーラブルで、デジタル タイポグラフィ用の [TTF](/font/ttf/) 形式の既存の機能を拡張します。 Microsoft と Adobe によって開発された OTF は、PostScript と TrueType フォント形式の機能を組み合わせたものです。これにより、OTF 形式は大多数の書記体系に対応できるようになり、主要なコンピューター プラットフォームで一様に使用されるようになりました。 OpenType フォント形式は、Mac OS X および Windows 2000 以降でサポートされています。

## 簡単な歴史

OpenType フォントの要件は、細かいタイポグラフィを処理できる、より表現力豊かなフォント形式の要件として生まれました。さらに、世界の多くの書記体系の複雑な動作の要件を満たすことを目的としていました。 Microsoft は、1990 年代初頭に、GX タイポグラフィとして知られる Apple の高度なタイポグラフィ技術のライセンス供与を試みました。これはうまくいかず、その結果、Microsoft は 1994 年に独自の TrueType フォント テクノロジの拡張を開始しました。変更には、Adobe の Type 1 (PostScript) フォント形式の機能も満たす、より適切なフォント形式を導入することも含まれていました。

Adobe は 1996 年に Microsoft に加わり、Apple の TrueType と独自の Type 1 フォント形式の両方を置き換える取り組みに参加しました。これにより、基礎となる両方のフォント形式を組み合わせて、制限を克服し、新しい拡張機能を追加することができました。この新しいテクノロジーは、**OpenType** という名前で同じ年に導入されました。

## OTF ファイル形式の仕様

OTF 仕様は Microsoft によって公開されており、開発者の観点から参照できます。 TTF と同様に、同じ 'sfnt' コンテナー構造を使用し、TrueType 仕様と互換性があります。 OpenType フォント ファイル内のデータは、テキスト レイアウトの計算、TrueType またはコンパクト フォント フォーマット (CFF) アウトラインとしてのグリフの定義、代替グリフ記述としてのモノクロまたはカラー ビットマップまたは SVG ドキュメントの提供、メタデータ情報など、さまざまな目的で使用されます。

### OTF データ型
OTF ファイルは、すべてビッグ エンディアンである次のデータ型を使用します。

|データ型|説明|
---|---|
|uint8| 8 ビット符号なし整数。|
|int8| 8 ビットの符号付き整数。|
|uint16| 16 ビット符号なし整数。|
|int16| 16 ビットの符号付き整数。|
|uint24| 24 ビット符号なし整数。|
|uint32| 32 ビット符号なし整数。|
|int32| 32 ビットの符号付き整数。|
|固定| 32 ビットの符号付き固定小数点数 (16.16)|
|FWORD|フォント デザイン単位で量を記述する int16。|
|UFWORD|量をフォント デザイン単位で記述する uint16。|
|F2DOT14|小数部の下位 14 ビット (2.14) を持つ 16 ビットの符号付き固定数。|
|LONGDATETIME| UTC 1904 年 1 月 1 日深夜 12:00 からの秒数で表される日付と時刻。値は、符号付き 64 ビット整数として表されます。|
|タグ|テーブル、設計変動軸、スクリプト、言語システム、機能、またはベースラインを識別するために使用される 4 つの uint8 (長さ = 32 ビット) の配列|
|オフセット16| uint16 と同じテーブルへの短いオフセット、NULL オフセット = 0x0000|
|オフセット32| uint32 と同じテーブルへの long オフセット、NULL オフセット = 0x00000000|
|Version16Dot16|メジャー バージョン番号とマイナー バージョン番号を含むパックされた 32 ビット値。 (表のバージョン番号を参照してください。)|

### OTF テーブル ディレクトリ

OTF ファイルは、テーブル ディレクトリで始まります。このディレクトリは、フォント ファイル内のテーブルの最上位コレクションです。ファイル内のフォントの数によっては、テーブル ディレクトリがファイル内の別の場所にある場合があります。たとえば、フォント ファイルにフォントが 1 つしかない場合、テーブル ディレクトリはファイルのバイト 0 から始まります。複数の OpenType Fonts コレクションの場合、
テーブル ディレクトリの先頭は TTCHeader に示されます。

|タイプ |名前 |説明|
---|---|---|
|uint32 |sfntVersion| 0x00010000 または 0x4F54544F ('OTTO')|
|uint16| numTables |テーブルの数。|
|uint16| searchRange |numTables 以下の 2 の最大累乗、16 倍 ((2\**floor(log2(numTables))) * 16、「**」は累乗演算子)|
| uint16 |entrySelector numTables 以下の 2 の最大累乗の Log2 (log2(searchRange/16)、これは floor(log2(numTables)) に等しい)。
|uint16 |rangeShift |numTables に 16 を掛けて、searchRange ((numTables * 16) - searchRange) を引いた値。
|テーブルレコード| tableRecords[numTables] |テーブル レコード配列 — フォントの最上位テーブルごとに 1 つ |


### テーブル レコード

フォントの最上位テーブルごとに、次のフィールドで構成されるテーブル レコードがあります。

|タイプ|名前|説明|
---|---|---|
|タグ|テーブルタグ|テーブル識別子。|
|uint32|チェックサム|このテーブルのチェックサム。|
|オフセット32|オフセット|フォント ファイルの先頭からのオフセット。|
|uint32| length このテーブルの長さ。|

OpenType フォント ファイル内の各テーブルは、テーブル タグと呼ばれる名前で表されます。配列内のすべてのレコードをタグで昇順にソートする必要があります。

## 参考文献
* [マイクロソフトによる OpenType フォント仕様](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
* [TrueType の概要](https://learn.microsoft.com/en-us/typography/truetype/)

