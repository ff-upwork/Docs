{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSG - Microsoft Outlook 電子メール形式",
  "description":"MSG ファイル形式と,MSG ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "MSG",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## .MSG オプション番号

MSG は、[Microsoft Outlook](https://products.office.com/en-us/outlook/email-and-calendar-software-microsoft-outlook?rtc#1) および Exchange で電子メール メッセージを保存するために使用されるファイル形式です。 、連絡先、予定、またはその他のタスク。このようなメッセージには、送信者、受信者、件名、日付、およびメッセージ本文、または連絡先情報、予定の詳細、および 1 つまたは複数のタスク仕様を含む 1 つまたは複数の電子メール フィールドが含まれる場合があります。 Message オブジェクトを構成するプロパティも、MSG ファイルの一部です。 MSG ファイルには、ヘッダー、メイン メッセージ本文、およびハイパーリンクがプレーン ASCII テキストとして含まれています。 MSG ファイルは、Microsoft の Messaging Applications Programming Interface (MAPI) を必要とするプログラムにも適しています。

## MSG ファイル構造

CFB_3 形式は MSG ファイルのベースです。このパラダイムは、ストレージとストリームの概念に基づいており、ディレクトリとファイルに非常に近いものです。したがって、前者の主な違いは、複合ファイルと呼ばれる別個のファイルにパッケージ化された階層全体です。オブジェクトはメッセージ ファイルを構成し、単一のプロパティまたはそのコレクションで構成されます。この機能により、アプリケーションは複雑な構造化データを 1 つのファイルに簡単に格納できます。この形式は複数のストレージも指定します。各ストレージは Message オブジェクトを主要コンポーネントとして表します。これらのストレージには、そのコンポーネントのプロパティを表す多数のストリームが含まれています。収納のネスティングも可能です。

## マピ プロパティ

.msg ファイルの最上位にあるストレージには、プロパティを格納するストリームが含まれています。プロパティは次のように分類できます。

* 固定長のプロパティ
* 可変長プロパティ
* 多値プロパティ

カテゴリに関係なく、プロパティはタグ付きまたは名前付きです。ただし、マッピング ストレージによって指定された名前付きプロパティには、適切なマッピング情報が必要です。

## 倉庫

ストレージは、Message オブジェクトの主要コンポーネントを構成します。 MSG ファイル形式には、次のストレージが記載されています。

## トップレベルの構造

メッセージ オブジェクトは、MSG ファイル形式のトップ レベル全体を表します。タイプ、プロパティ、受信者および添付オブジェクトの数に応じて、メッセージ オブジェクトは対応する .MSG ファイルに異なるストリーム ストレージを持つことができます。

### 他の構造との関係

Msg ファイル形式には、他の構造と次のような関係があります。

※.msgのベースはCompound File Binary File Formatです。
* Message and Attachment Object Protocol で使用されるプロパティは、この形式で使用されます。

## MSG フォーマットを回避するシナリオ

メッセージ オブジェクトは、.msg ファイル システムを使用するクライアントまたはメッセージ ストア間で共有できます。 Message オブジェクトを .msg ファイル形式で格納することが適切でない状況はほとんどありません。例えば：

* 大規模なスタンドアロン アーカイブを維持する場合は、ビューをより正確にレンダリングできるフル機能の形式を使用することをお勧めします。
※受信者が不明な場合、受信側が対応していない形式で、非公開や無関係なものが配信される可能性があります。

## MSG ファイルの例

MSG ファイルがどのように見えるかを理解するには、[サンプル MSG ファイル](https://products.conholdate.app/viewer/view/mL7cmq6qYbcNG329P/sample-msg-file.msg) をダウンロードして、その内容を表示するコンピュータ。

## 参考文献

* [[MS-OXMSG]: Outlook MSG ファイル形式](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

