{
  "date" : "2021-04-16",
  "keywords" :["XML","P6XML","ファイル","拡張子","ファイル形式","プロジェクト","管理","プリマベーラ","P6"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P6XML - プリマベーラ P6 プロジェクト",
  "description":"P6XML ファイル形式と,P6XML ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "P6XML",
  "menu" : {
    "docs" : {
      "parent" : "project-management"
}
},
  "lastmod" : "2021-05-07"
}

## .P6XML ファイルとは? ##

P6XML ファイル拡張子は、優れた可読性、適応性、および幅広い用途を備えているため、理想的な形式になっています。 Primavera P6 Professional には、[XER](/project-management/xer) ファイルと XML ファイルの両方をエクスポートおよびインポートする機能があります。 XML は **Extensible Markup Language** の略です。この一般的な形式により、ユーザーは Primavera P6 データベース間でプロジェクト情報を共有できます。プロジェクト データは、XML ファイルを介してテキスト ファイルに簡単に保存できます。これにより、多数のソフトウェア プログラムがデータを簡単に交換できるようになります。このようなデータは、Primavera P6 ユーザーが簡単に共有および管理できます。

## P6XML ファイル形式の利点 ##

* Primavera ユーザーは、XML ファイルを使用してエクスポートおよびインポートするベースラインを簡単に定義できます。
* XML エクスポートには、すべてのプロジェクトの詳細なアクション プランを含めることができます
* アクティビティ コード、カレンダー、リソースなどの特定のグローバル データ項目を編集、追加、または削除できない Primavera 6 を使用しているユーザーは、それらをインポートできません。
* Primavera が使用する General および Project Security Profile 設定に加えて、データベース内のデータに影響または変更するデータ項目はインポートされません

## Primavera P6 からの XML ファイルのエクスポート ##

P6 Professional プロジェクトとプロジェクト データを P6XML ファイルにエクスポートするには、Oracle Primavera Cloud を使用します。 P6 Professional デスクトップ アプリケーションから作成されたファイルをダウンロードして、Primavera Cloud にインポートできます。中断なくエクスポート プロセスを実行する前に、P6 Professional データベースまたは P6 EPPM にリンクしているかどうかを調整する必要があります。エクスポート プロセスの一部の機能は、データベースによって異なる場合があります。 P6 Proficient データベースを使用した P6 Specialized 設定により、エクスポート プロセスはシステム上でローカルに動作します。 P6 Professional データベースがあれば、システムの設定から P6 XML ファイルを簡単にエクスポートして開くことができます。

エクスポート プロセスを説明するいくつかの手順を次に示します。

*オープン欲望プリマベーラP6プロジェクト
※その後、ファイルタブのエクスポートを選択
※「Primavera P6-(XML)」を選択。その後、[次へ] をクリックします。
* エクスポートするプロジェクトをダブルクリックします
* エクスポートしたファイルを配置するパスの切り捨てを選択し、[完了] を選択します。
* ファイルの保存方法を選択します
* エクスポート ファイルでプロジェクト レベルのレイアウトが必要ない場合は、[すべてのプロジェクト レベルのレイアウトをエクスポートする] の選択を解除することが不可欠です。
* 終了を選択すると、XML エクスポートの確認が表示されます

### 重要なヒント ###

* P6 EPPM データベースに接続するたびに、管理者はコンテンツ ソースの URL を P6 のアプリケーション設定の [全般] ページにある [P6 URL] フィールドに渡す必要があります。
* 多数のプロジェクトを 1 つの XML ファイルにエクスポートすると便利です
* プロジェクトに割り当てられているグローバル データがエクスポートされます
* すべてのリソースを許可せずに XML ファイルをエクスポートすると便利です
  


## P6XML ファイルを開く際の問題? ##

P6XML 形式の誤動作の原因となる一般的な問題は次のとおりです。

*サポートソフトウェアの不在
* 破損したファイル
* ウイルスによる感染ファイル
* P6XML の記述が誤って Windows レジストリから削除された
* システムにファイルを開くためのアクセス権がありません
* システムの古いドライブ
※ファイルの拡張子はリネーム
 

## 参照 ##

* [Oracle - P6 XML](https://docs.oracle.com/cd/E80480_01/English/admin/p6_eppm_xml_import_guide/190894.htm)
