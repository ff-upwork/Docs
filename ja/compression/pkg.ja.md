{
  "date" : "2021-04-08",
  "keywords" :[ "pkg ファイル", "pkg ファイル形式", "pkg ファイルとは", "ファイル", "pkg 例", "pkg ファイル拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PKG - 拡張可能なアーカイブ ファイル形式",
  "description":"PKG ファイル形式と,PKG ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "PKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## .PKG ファイルとは何ですか?

拡張子が .pkg のファイルは、macOS にソフトウェアをインストールするために使用されるインストーラー パッケージ ファイルです。マッキントッシュパソコンだけでなく、iPhoneでも使用されています。組み込みの Apple インストーラー アプリケーションを使用して、PKG ファイルの内容をインストールできます。 PKG ファイルは、Windows オペレーティング システムでソフトウェアのインストールに使用される MSI ファイルに似ています。インストール中に、これらのパッケージ ファイルはメッセージをログに記録し、このパッケージによってどのような追加機能がインストールされるかを示すことができます。

## PKG ファイル形式

PKR は、全体のファイル サイズを縮小するために圧縮されたバイナリ ファイルです。 OSX 10.5 以降、単一のインストーラー ファイルを含むフラット パッケージが Apple によって導入されました。これらは、単一のファイルではなくバンドルとして提供された以前のパッケージ形式とは異なります。これらのバンドルされたパッケージには、構造化されたディレクトリ階層が含まれており、インデックス ファイルを介して簡単に検索できるようにファイルを格納していました。フラット PKG ファイル形式は、実際には [XAR](/compression/xar/) アーカイブであり、次のものがあります。

* ヘッダー - サイズ、チェックサム、およびバージョン情報を定義します
* 目次 - UTF-8 としてエンコードされている (必要な) XML ドキュメントで、ファイルの先頭に格納されているため、アーカイブをスキャンして個々のファイルを簡単に抽出できます。
* ヒープ - TOC によって参照されるデータの非構造化ヒープ

## 参考文献

* [フラット パッケージ ファイル形式](http://s.sudre.free.fr/Stuff/Ivanhoe/FLAT.html)
* [PKG - ウィキペディア](https://en.wikipedia.org/wiki/.pkg)
