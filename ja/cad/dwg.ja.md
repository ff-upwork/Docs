{
  "date" : "2020-03-16",
  "keywords" :["DWG","ファイル形式","CAD","開く","作成"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"DWG ファイル形式と,DWG ファイルを作成して開くことができる API について学びます。",
  "title" :"DWGファイル形式",
  "linktitle" : "DWG",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## DWG ファイルとは?

DWG 拡張子を持つファイルは、2D および 3D 設計データを格納するために使用される独自のバイナリ ファイルを表します。 ASCII ファイルである DXF と同様に、DWG は CAD (Computer Aided Design) 図面のバイナリ ファイル形式を表します。 CAD ファイルの内容を表現するためのベクター画像とメタデータが含まれています。 Autodesk の無料の DWG TrueView など、Windows オペレーティング システムで DWG ファイルを表示するための無料のビューアがあります。 DWG ファイルへのアクセスをサポートする他のサードパーティ アプリケーションもあります。 DWG ファイルには、ユーザーが作成した情報が含まれており、次のものが含まれます。

*デザイン
* 幾何学的データ
*地図と写真

この形式は、建築家、エンジニア、デザイナーがさまざまな設計目的で広く使用しています。

## 簡単な歴史 ##

DWG ファイル形式は、1982 年に正式に導入されて以来、時間とともに進化してきました。歴史の観点から見た過去の出来事の概要は次のとおりです。

**1982:** Autodesk は、AutoCAD の基礎として、1970 年に Mike Riddle によって開発された DWG ファイル形式のライセンスを取得しました。

**1998:** AutoCAD R14.01 のリリースにより、Autodesk は DWGCHECK と呼ばれる機能を介してファイル検証を追加しました。これは、Autodesk によって WaterMark と呼ばれる暗号化されたチェックサムと製品コードを、プログラムによって作成された DWG ファイルに埋め込みます。

**2006:** Autodesk は AutoCAD 2007 を修正し、「TrustedDWG テクノロジ」を組み込み、テキスト文字列「Autodesk DWG.This file is a Trusted DWG last saved by a Autodesk application or Autodesklicensed application」を DWG ファイルに埋め込みました。この目的は、オートデスク ソフトウェアのユーザが、これらのファイルがオートデスクまたは RealDWG アプリケーションによって作成されたことを確認できるようにすることでした。これは、非互換性のリスクを確実に軽減するのに役立ちます。

## ファイル構造 ##

DWG は、さまざまなアプリケーションで広く使用されているファイル形式の 1 つであり、堅牢なファイル構造を備えています。 DWG はバイナリ ファイル形式であるため、プレーン ASCII [DXF](/cad/dxf/) ファイル形式のように人間が判読することはできません。通常、DWG ファイルには、イメージの座標に関する情報と、それに関連付けられたメタデータが含まれています。 DWG ファイル形式の完全な[仕様](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)は、OpenDesign でダウンロードできます。 DWGファイル形式のファイル構造をまとめると以下のようになります。

**ヘッダー**: ファイル ヘッダーは、DWG ヘッダー変数と、エラー検出に使用される巡回冗長検査 (CRC) に関する情報で構成されます。各サブセクションは、異なるラベルを表すために異なる長さのビットが使用される特殊なベクトルです。たとえば、DWG ヘッダー変数の最初の 6 ビットは、バージョン文字列を表します。

**クラス定義:** DWG ファイルには、特定の .dwg ファイルの目的に応じて多数のクラスが含まれる場合があります。その他、クラスデータ領域のクラスメタデータサイズ、クラス番号、チェックサムなどの情報。

**テンプレート**: これはオプションであり、R15 および R15 バージョンでは、このセクションはオブジェクトの空き領域セクションの下にあります。

**パディング**: メタデータには特定のバイト数のサフィックスとポストフィックスが付けられ、古い AutoCAD ソフトウェア バージョンが新しい DWG ファイル形式と上位互換性を持つようになります。

**画像データ**: このセクションのメタデータは、特定の .dwg タイプによって異なります。 R14 および R15 ユーザーの場合、このセクションはオプションです。

**オブジェクト データ**: オブジェクト データは、既存のオブジェクト リストに対応するテーブル エンティティ、辞書エントリなどの完全なリストで構成されます。

**オブジェクト マップ**: ファイル内の各オブジェクトの場所は、ファイルのこのセクションで指定されます。このセクションのメタデータのほとんどは、オブジェクトの識別と再レンダリングで役割を果たすファイル ハンドルです。

**オブジェクトの空き容量**: このセクションはすべてのユーザーにとってオプションです

**2 番目のヘッダー**: DWG ファイルの末尾にあるファイル ヘッダー セクションの複製

## 参照 ##

* [DWGファイル形式仕様書](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)
* [DWG ファイル仕様](https://www.scan2cad.com/blog/dwg/file-spec/)
* [DWG - ウィキペディアによる](https://en.wikipedia.org/wiki/.dwg)

