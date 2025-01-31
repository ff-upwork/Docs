{
  "date" : "2019-12-13",
  "keywords" :["MP3","ファイル","拡張子","フォーマット","オーディオ","MPEG"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"MP3 ファイル形式と,MP3 ファイルを開いて作成できる API について学びます。",
  "title" :"MP3 - オーディオ ファイル形式",
  "linktitle" : "MP3",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2020-09-04"
}

## MP3ファイルとは何ですか?

拡張子が .mp3 のファイルは、MPEG-1 Audio Layer III または MPEG-2 Audio Layer III に正式に基づくオーディオ ファイルのデジタル エンコード ファイル形式です。レイヤ 3 オーディオ圧縮を使用する MPEG (Moving Picture Experts Group) によって開発されました。 MP3 ファイル形式で達成される圧縮は、.WAV または .AIF ファイルのサイズの 1/10 です。このフォーマットは、オーディオファイルのファイルサイズが大きいために以前は不可能だった、オンラインで聞くためにインターネット経由でそのようなオーディオファイルをストリーミングする利点を提供します. MP3 オーディオ ファイルの音質は、ビット レート、サンプル レート、ジョイント、通常のステレオなどのパラメータ設定によって制御できます。

## MP3 ファイル形式の歴史

MP3 形式は、ドイツの会社である Fraunhofer-Gesellshart によって発明および開発されました。このアルゴリズムは、使用する圧縮技術の特許を取得しています。 MP3の便利なタイムラインは次のとおりです。

• **1987 年** - ドイツのフラウンホーファー研究所は、高品質の低ビットレート オーディオ コーディングの研究を開始しました。それは EUREKA プロジェクト EU147、デジタル オーディオ放送と呼ばれていました。

• **1988 年 1 月** - ムービング ピクチャー エキスパート グループ (MPEG) が設立されました。

• **1989 年 4 月** - Fraunhofer はドイツで MP3 の特許を取得しました。

• **1992 年** - フラウンホーファーの研究を支援したディーター ザイツァーは、オーディオ コーディングを MPEG-1 に統合しました。

• **1993 年** - MPEG-1 標準が発行されました。

• **1994** - MPEG-2 標準が開発され、1 年後に公開されました。

• **11 月。 1996 年 1 月 26 日** - MP3 の米国特許が発行されました。

• **1998 年 9 月** - Fraunhofer は特許権の行使を開始しました。 MP3オーディオコーディングを使用した人は誰でも、フラウンホーファーにライセンス料を支払いました.

• **1999 年 2 月** - レコード会社の SubPop は、MP3 形式で音楽を配信しました。このような会社としては初めてです。

• **1999 年** - 最初のポータブル MP3 プレーヤーが登場。

## MP3 ファイル形式

MP3 ファイルは MP3 フレームで構成され、各フレームはヘッダーとデータ ブロックで構成されます。フレームは独立しておらず、通常、任意のフレーム境界で抽出することはできません。ファイルのデータ ブロックには、周波数と振幅に関するオーディオに関する情報が含まれています。ヘッダー内の同期ワードは、有効なフレームの開始を識別します。この後に 3 ビットが続き、最初のビットは MPEG 標準であることを示し、残りの 2 ビットはレイヤ 3 が使用されていることを示します。したがって、MPEG-1 Audio Layer 3 または MP3 です。以降、MP3 ファイルによって値が異なります。

[ISO](https://en.wikipedia.org/wiki/International_Organization_for_Standardization)/[IEC](https://en.wikipedia.org/wiki/International_Electrotechnical_Commission) 11172-3 は、ヘッダの仕様とともにヘッダ。現在、ほとんどの MP3 ファイルには [ID3](https://en.wikipedia.org/wiki/ID3) [メタデータ](https://en.wikipedia.org/wiki/Metadata) が含まれており、MP3 フレームの前後に配置されています。図に示されているとおりです。データ ストリームには、オプションのチェックサムを含めることができます。

## 参照 ##

* [MP3 - ウィキペディアによる](https://en.wikipedia.org/wiki/MP3)

