{
  "date" : "2019-10-11",
  "keywords" :[ "ott ファイル", "ott ファイル形式", "ott ファイルとは", "ファイル", "ott の例", "ott ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTT - OpenDocument テンプレート ファイル",
  "description":"OTT ファイル形式と,OTT ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "OTT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## .OTT ファイルとは何ですか?

拡張子が OTT のファイルは、OASIS の OpenDocument 標準形式に準拠したアプリケーションによって生成されたテンプレート ドキュメントを表します。これらは、無料の OpenOffice Writer などのワード プロセッサ アプリケーションで作成され、これらのテンプレート ファイルから新しいドキュメントを生成するために使用できる設定を保持できます。これらの設定には、ページの余白、罫線、ヘッダー、フッター、およびその他のページ設定が含まれます。このようなテンプレートは、会社のレターヘッドや標準化されたフォームなどの公式文書で使用されます。

## 簡単な歴史 ##

ODP ファイル形式の仕様は、ODF 仕様として開発された標準に基づいています。これらの仕様は、以下のように OASIS によって開発および公開された 3 つのバージョンの形で過去に進化してきました。

**2005:** 2005 年 5 月にバージョン 1.0 が公開されました

**2007:** 2007 年 2 月にバージョン 1.1 が公開されました

**2011:** 2011 年 9 月にバージョン 1.2 が公開されました

ODF 1.0 から 1.1 バージョンへの移行では、かなり小さな変更がありました。 [ODF 1.2 バージョン](https://www.oasis-open.org/standards#opendocumentv1.2) は、ODF 仕様の最新バージョンであり、ODS 読み取り/書き込みに関連するアプリケーションを開発する開発者は参照する必要があります。

## ファイル形式の仕様

OpenDocument 形式は、単一の XML ドキュメントとしてのドキュメント表現と、[ZIP](/Compression/ZIP/) アーカイブとしてのパッケージ内の複数のサブドキュメントのコレクションをサポートします。 ZIP アーカイブの各ファイルには、ドキュメント全体の一部が格納されています。各サブドキュメントには、ドキュメントの特定の側面が格納されます。たとえば、あるサブドキュメントにはスタイル情報が含まれ、別のサブドキュメントにはドキュメントのコンテンツが含まれます。一般的な ODF ドキュメントには、次のコンポーネントがあります。

* content.xml – ドキュメント コンテンツとコンテンツで使用される自動スタイル。
* styles.xml – ドキュメント コンテンツで使用されるスタイルと、スタイル自体で使用される自動スタイル。
* meta.xml – 作成者や最後の保存アクションの時間などのドキュメント メタ情報。
* settings.xml – ウィンドウ サイズやプリンター情報など、アプリケーション固有の設定。

これらに加えて、ドキュメント サムネイル、画像などの他の多くのサブドキュメントをパッケージに含めることができます。ドキュメント ファイルは、コンテンツ (シート) が //content.xml// サブドキュメントに格納される ODF ファイルのサブセットです。

## 参照 ##

* [OpenDocument - ウィキペディアによる](https://en.wikipedia.org/wiki/OpenDocument)
