{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PST - Outlook Personal Information Store ファイル形式",
  "description":"PST ファイルの形式と,PST ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "PST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## PST ファイルとは何ですか?

拡張子が .pst のファイルは、さまざまなユーザー情報を格納する Outlook 個人用記憶域ファイル (個人用記憶域テーブルとも呼ばれます) を表します。ユーザー情報は、電子メール、予定表アイテム、メモ、連絡先、およびその他のいくつかのファイル形式を含むさまざまな種類のフォルダーに保存されます。 PST ファイルは、電子メール データをオフラインでアーカイブするために使用され、後でさまざまなアプリケーションで読み込んで表示できます。

## PST ファイル形式の仕様

PST ファイル形式 [仕様](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546) は、Microsoft から、Open Specification Promise を通じて無料かつ取消不能な無料の特許ライセンスとして入手できます。 .

### PST 形式の種類

PST ファイル形式は、ファイル タイプのエンコーディングに基づいて 2 つのタイプに分類されます。 ANSI でエンコードされた PST ファイルは古いファイル形式であり、Outlook 2002 以前のバージョンでのみサポートされています。このようなファイルの最大サイズは 2 GB (2^^31^^ バイト) に制限されており、Unicode はサポートされていません。 Unicode エンコーディングに基づく、より最新のファイル形式タイプでは、ファイル サイズの制限がなくなり、最大データ サイズが 50 GB に達する可能性があります。

### PST ファイル形式の論理構成

PST ファイル形式の基盤には B ツリーがあり、データを並べ替え、検索、順次アクセス、挿入、削除などを対数時間で実行できます。 PST ファイルの全体的な構造は、3 つの層で構成されています。

![Logical layers of a PST file](/email/PST-1.png "Logical layers of a PST file")

「ノード データベース (NDB) レイヤー」 - ノード データベース レイヤーは、PST ファイルの下位レベルにあり、ノードのデータベースを含みます。これらのノードは、実際には PST ファイル形式の下位レベルのストレージ機能を表しています。 NDB レイヤーは、ストレージの観点から、ヘッダー、ファイル割り当て情報、ブロック、および BTree (ノード BTree およびブロック BTree) で構成されます。 NDB レイヤーのノードとブロックは、ノード参照の 4 つのプロパティ、つまり NID (ノード ID)、親 NID、データ BID (ブロック BID)、およびサブノード BID の 1 つであるデータ BID を介してリンクされます。

「リスト、テーブル、およびプロパティ レイヤー -」 LTP レイヤーは、NDB の上にあるより高いレベルの概念の論理的な理解を提供します。他の要素に加えて、LTP レイヤーは主にプロパティ コンテキスト (PC) とテーブル コンテキスト (TC) で構成されます。 PC はプロパティのコレクションであり、TC はプロパティのコレクションとこれらの存在の 2 次元マトリックスを表します。 PC と TC の効率的な実装である LTP レイヤーは、NDB ノード上で次の 2 種類のデータ構造を使用します。

* Heap On Node (HN) - ノードのデータ ストリームを小さな可変サイズのフラグメントにサブアロケーションすることを可能にします。
* BTree on Heap (BTH) - BTH はデータ PC を検索する便利で実用的な方法を提供し、上記の PC は BTH として実装されるため、HN 構造の内部に構築することによって実装されます。

`メッセージング層 -` PST ファイルを操作するためのより高いレベルのルールとビジネス ロジックは、この層で実装されます。このレイヤーの論理出力は、LTP レイヤーと NDB レイヤーを組み合わせることで可能になる、Folder オブジェクト、Message オブジェクト、Attachment オブジェクト、およびプロパティとして生成されます。 PST コンテンツを変更する際に従う必要がある規則と要件も、この層で定義されます。

### PST ファイル形式の物理的な構成

PST ファイルのファイル構成の高レベルは、下の図に示すとおりです。これは、PST ファイルの論理要素とは異なる概念の概要にすぎません。

![Physical organization of the PST file format](/email/PST-2.png "Physical organization of the PST file format")


#### PST ヘッダー情報

PST ファイルの HEADER 構造は、ファイルの最初の 0 オフセットにあります。これには、PST ファイルに関するメタデータ情報と、上記の NDB レイヤー データ構造にアクセスするための ROOT 情報が含まれています。 HEADER 構造は、PST ファイル形式の Unicode バージョンと ANSI バージョンでは異なります。

ヘッダーは、バイト (0x21、0x42、0x44、0x4E) で表される 4 バイトのマジック ワード **!BDN** で始まります。別の 2 バイトのマジック ナンバー **SM** (0x53, 0x4D) は、ファイルの先頭からオフセット 8 にあります。バージョン情報 (ANSI または Unicode) は、ファイルの先頭から 10 のオフセットにあります。 16 進値 (0x17) は Unicode PST ファイルを指定し、0x0E または 0x0F は ANSI ファイル形式を表します。

|フィールド|説明
---|---|
|dwMagic (4 バイト)|「{ 0x21, 0x42, 0x44, 0x4E } ("!BDN")」でなければなりません
|dwCRCPartial (4 バイト)|wMagicClient (0ffset 0x0008) から始まる 471 バイトのデータの 32 ビット CRC 値
|wMagicClient (2 バイト)|「{ 0x53, 0x4D }」でなければなりません。
|wVer (2 バイト)|ファイル形式のバージョン。この値は、ファイルが ANSI PST ファイルの場合は 14 または 15 でなければならず、ファイルが Unicode PST ファイルの場合は 23 でなければなりません。
|wVerClient (2 バイト)|クライアント ファイル形式のバージョン。このドキュメントで説明されている形式に対応するバージョンは 19 です。このドキュメントに基づく新しい PST ファイルの作成者は、この値を 19 に初期化する必要があります。
|bPlatformCreate (1 バイト) |この値は 0x01 に設定する必要があります。
|bPlatformAccess (1 バイト) |この値は 0x01 に設定する必要があります。
|dwReserved (8 バイト)|
|bidUnused (8 バイトの Unicode のみ)|Unicode PST ファイル形式が作成されたときに追加された未使用のパディング。
|bidNextP (Unicode: 8 バイト; ANSI: 4 バイト)|次のページの BID。ページには、bidIndex 値を割り当てるための特別なカウンターがあります。ページの BID の bidIndex の値は、このカウンターから割り当てられます。
|bidNextB (4 バイト ANSI のみ): |次の BID。この値は、次に割り当てられるブロックに割り当てられる BID を示すモノトニック カウンターです。 BID 値は 4 ずつ進みます。詳細については、セクション 2.2.2.2 を参照してください。
|dwUnique (4 バイト)|これは単調に増加する値で、PST ファイルの HEADER 構造が変更されるたびに変更されます。この値の機能は、一意の値を提供し、各ヘッダーの変更後に HEADER CRC が異なることを確認することです。
|rgnid[]   (128 バイト)|32 の NID の固定配列で、それぞれが 32 の可能な NID_TYPE (NID_TYPE、NID_TYPE_NORMAL_FOLDER、NID_TYPE_SEARCH_FOLDER、NID_TYPE_NORMAL_MESSAGE、NID_TYPE_ASSOC_MESSAGE) のいずれかに対応します。
|qwUnused (8 バイト)|未使用スペース。ゼロに設定する必要があります。 Unicode PST ファイル形式のみ。
|root (Unicode: 72 バイト; ANSI: 40 バイト)|ROOT 構造 (セクション 2.2.2.5)。
|dwAlign (4 バイト)|未使用のアラインメント バイト。ゼロに設定する必要があります。 Unicode PST ファイル形式のみ。
|rgbFM (128 バイト)|非推奨の FMap。これはもう使用されていないため、0xFF で埋める必要があります。リーダーは、これらのバイトの値を無視する必要があります。
|rgbFP (128 バイト)|非推奨の FPMap。これはもう使用されていないため、0xFF で埋める必要があります。リーダーは、これらのバイトの値を無視する必要があります。
|bSentinel (1 バイト)|0x80 に設定する必要があります。
|bCryptMethod (1 バイト)|PST ファイル内のデータがどのようにエンコードされているかを示します。事前定義された値 (NDB_CRYPT_NONE、NDB_CRYPT_PERMUTE、NDB_CRYPT_CYCLIC) のいずれかに設定する必要があります。
|rgbReserved (2 バイト)|予約済み;ゼロに設定する必要があります。
|bidNextB (8 バイト)|次に使用可能な BID 値を示します。 Unicode PST ファイル形式のみ。
|bidNextB (Unicode のみ: 8 バイト)|次の BID。この値は、次に割り当てられるブロックに割り当てられる BID を示すモノトニック カウンターです。 BID 値は 4 ずつ進みます。詳細については、セクション 2.2.2.2 を参照してください。
|dwCRCFull (4 バイト)|wMagicClient から始まり、bidNextB を含む 516 バイトのデータの 32 ビット CRC 値。 Unicode PST ファイル形式のみ。
|ullReserved (8 バイト)|予約済み。ゼロに設定する必要があります。 ANSI PST ファイル形式のみ。
|dwReserved (4 バイト)|予約済み。ゼロに設定する必要があります。 ANSI PST ファイル形式のみ。
|rgbReserved2 (3 バイト)|
|b予約済み (1 バイト) |
|rgbReserved3 (32 バイト) |

### データ保護 ###

セキュリティのために、PST ファイルをパスワードで保護することもできます。これにより、ロードするアプリケーションは、表示する前にパスワードを適用する必要があります。 PST ファイルに適用されたパスワードは、メッセージ ストアに保存されます。ただし、利用可能なツールでパスワードを削除できるため、これは強力なデータ保護にはなりません。また、ユーザー指定のパスワードは、暗号アルゴリズムのエンコードおよびデコードのキーの一部として使用されません。したがって、許可されていない関係者がアクセスするデータを保護するメリットはありません。パスワードを元の文字列の CRC-32 ハッシュとして保存することも、ブルート フォース アプローチに対するデータ セキュリティの脆弱な方法になります。

## 参照 ##

* [Outlook 個人用フォルダー (.pst) ファイル形式](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [個人フォルダのファイル形式仕様](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

