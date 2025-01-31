{
  "date" : "2019-10-11",
  "keywords" :[ "mht","mht ファイル", "mht ファイル形式", "mht ファイルの種類", "ファイル", "種類", "mht ファイルとは" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHT - MIME HTML ファイル形式",
  "description" :"MHT ファイル形式と,MHT ファイルを作成して開くための API について学びます。",
  "linktitle" : "MHT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## .MHT オプション番号

拡張子が .mht のファイルは、MIME 対応のアーカイブ ファイル形式で、さまざまな種類のデータが 1 つのファイルに含まれています。テキスト、画像、ページ スタイルなどのデータを [CSS](/web/css/) ファイルの形式で保存したり、JavaScript やその他のリソースを埋め込みリソースとして保存したりできます。 MIME タイプが message/rfc822 の MHT ファイルは、HTML ファイルのすべてのコンテンツを単一のアーカイブ ファイルとしてカプセル化し、ストレージ デバイスのアーカイブに保存します。 Microsoft Word などのソフトウェア アプリケーションを使用すると、Word ドキュメントを MHT ファイルとしてエクスポートして MHT に変換できます。 MHT ファイルは、Microsoft Internet Explorer や Google Chrome などの一般的なブラウザを使用して開くことができます。

## MHT ファイル形式

[MHTML](/web/mhtml/) と同様に、MHT も集約 HTML ドキュメントの MIME カプセル化です。インライン ピクチャ、スタイル シート、アプレットなどの MHT ドキュメント内のドキュメント コンテンツは、URI を介してルート リソースにリンクされる MIME 暗号化されます。 Microsoft Outlook などの電子メール クライアントは、電子メール (通常は [EML](/email/eml/)) を MHT ファイル形式で保存します。 MHT ファイル形式の完全な仕様は [RFC 822](https://tools.ietf.org/html/rfc822) で入手でき、MHT ファイルを処理できるソフトウェア アプリケーションの開発に参照できます。

## MHT と MHTML の違い

オンライン ページを保存する際、ユーザーは、オンライン ページをネイティブ システムに保存するファイル形式の種類を決定するよう求められます。通常、ユーザーはマークアップ言語と MHTML ファイル形式の間で混乱します。彼らは、これらの間でファイル形式がより健全であることを確認するのが面倒であることに気付きます。

ユーザーがマークアップ言語としてオンライン ページを無駄にしないようにすると、フォルダが形成されます。このフォルダには、ページのさまざまなコンテンツ用の複数のファイルが含まれます。つまり、テキスト、グラフィック、アプレットなどのために作成されたまったく異なるファイル領域単位です。 MHTML は完全なオンライン ページに対して 1 つのファイルを作成するため、オンライン ページ。ページのすべての要素と、グラフィック、リンク、および代替ファイル エリア ユニットが 1 つのファイル内に埋め込まれています。

当然のことながら、MHT または MHTML ファイルは簡単に処理できます。ファイルは保護され、電子メールで簡単に共有できるからです。ただし、マークアップ言語ファイルの領域単位は、ファイルが 1 つでも失われたり削除されたりすると、ユーザーにとって役に立たない完全なマークアップ言語フォルダーが作成される可能性があるため、情報が失われる可能性があります。

## 参考文献

* [MHTML - ウィキペディア](https://en.wikipedia.org/wiki/MHTML)
* [MHT RFC](https://tools.ietf.org/html/rfc822)

