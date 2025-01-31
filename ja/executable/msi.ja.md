{
  "date" : "2021-06-30",
  "keywords" :[ "msi ファイル", "MSI ファイル形式", "msi ファイルとは", "ファイル", "msi の例", "msi ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"MSI ファイル形式と,MSI ファイルを作成して開くことができる API について学びます。",
  "title" :"MSI - Windows インストーラー パッケージ ファイル",
  "linktitle" : "MSI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## .MSI ファイルとは何ですか?
Windows プログラムのインストールと起動に使用される MSI ファイル。インストールする必要のある重要なファイルやインストール場所に関する情報など、一般的なソフトウェア プログラムのインストール情報を含む、Microsoft Windows 用の完全なパッケージ。 MSI ファイルには、ソフトウェア更新プログラムのパッケージが含まれている場合もあります。 MSI ファイルは [EXE](/executable/exe/) に似ていますが、EXE にはインストーラー情報が含まれていない場合があり、EXE ファイルを実行するとソフトウェア プログラムが直接実行される場合があります。

## MSI ファイル形式
Windows インストーラーは、実際には、ソフトウェア プログラムのインストール、削除、およびメンテナンスに使用される Microsoft Windows の API (アプリケーション プログラミング インターフェイス) およびソフトウェア コンポーネントです。インストール情報とオプション ファイルは、インストール パッケージと、COM 構造化ストレージとして構造化された緩やかなリレーショナル データベースとしてパッケージ化されています。 **MSI ファイル**としてよく知られており、ファイル拡張子は .msi です。ファイル拡張子が **.mst** のパッケージには Windows インストーラーの **変換スクリプト**が含まれ、**.msm** 拡張子のファイルには **Merge Modules** とファイル拡張子 **.pcp** が含まれます。 **パッチ作成プロパティ**に使用されます。 Windows インストーラーは、以前のバージョンであるセットアップ API から大幅に変更された後、より高度になります。 GUI フレームワークとアンインストール シーケンスの自動生成は、Windows インストーラーの新機能です。現在、スタンドアロンの実行可能インストーラー フレームワークの代替として検討されています。

### MSI パッケージの論理構造
パッケージは、1 つ以上の完全な製品のインストールを指定し、通常は **GUID** によって識別されます。製品は、1 つまたは複数のコンポーネントで構成され、さまざまな機能にグループ化されています。 Windows インストーラーは、さまざまな製品間の依存関係を同時に処理しません。パッケージの論理構造は、次の要素で構成されています。

- **製品**: 単一の、インストールされた、動作するプログラム、または組み合わせた複数のプログラムのセットが製品です。製品は一意の GUID によって識別されます。
- **機能**: 任意の数のコンポーネントおよびその他のサブ機能を含めることができます。小さいパッケージは、単一の機能で構成できます。
- **コンポーネント**: コンポーネントは、Windows インストーラーによって 1 つの単位として扱われます。プログラム ファイル、フォルダー、レジストリ キー、COM コンポーネント、およびショートカットを含めることができます。
- **キー パス**: キー パスは、パッケージ作成者が特定のコンポーネントにとって重要であると指定する、特定のファイル、ODBC データ ソース、またはレジストリ キーです。

## 参考文献

* [Windows インストーラ - ウィキペディアによる](https://en.wikipedia.org/wiki/Windows_Installer)


