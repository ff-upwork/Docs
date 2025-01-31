{
  "date" : "2021-07-13",
  "keywords" :["CER","拡張子","ファイル","フォーマット","ウェブ","証明書","言語"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CER - 証明書ファイル形式",
  "description":"CER ファイル形式と,CER ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "CER",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## .CER オプション番号##

拡張子が .cer のファイルには、所有者の証明書と特定の公開鍵に関する情報が格納されます。この形式のファイルは秘密鍵を保存できず、x509 である 1 つの証明書のみを保存する容量があります。特別に保護された認証局は、ブラウジング用の信頼できる安全なプロトコルである HTTPS に属する認証局です。
CER は、サーバーの証明書です。通常、ドメインの認証局によって受信されます。 CER は [CRT](/web/crt/) とほぼ同じと見なされますが、どちらも SSL 証明書の形式は同じですが、ファイル名の拡張子が異なります。
これらは、ブラウザを開いて、使用しているブラウザまたは Web サイトのセキュリティを確認するだけで、オペレーティング システムで使用できます。

## 簡単な歴史 ##

1995 年、Thawte は米国外でパブリック SSL (セキュア ソケット リンク) 証明書の問題を解決した最初の認証機関になりました。その後、1995年から2020年にかけて設立された一連の当局があります。

## CER ファイル形式 ##

これらのファイルは単純に
* PKC S#7 は Base64 ASCII エンコーディングで構成されています
* ファイル拡張子は p7b または p7cZ です
* バイナリ コンテンツの場合、証明書は DER または pkcs12/pfx になります。
独自の仕様を持つ多くの種類の証明書ファイルがあります。
* .pem、このフォーマットを連鎖する組織 usThawteificate が証明書を作成することがよく知られている場合
* .arm、自己署名を支援する証明書を抽出するメソッドが必要な場合、この目的で指定された形式は .arm です。 base-64 ASCII エンコーディングで表されます。
* .der, バイナリデータで構成されています。これは、単一の証明書にのみ使用できることを意味します
* .pfx (PKC512)、CA によって発行された証明書または自己署名証明書に対応する秘密鍵で構成されます。この形式は、ある SSL 実装から別の SSL 実装への変換でよく知られています。


