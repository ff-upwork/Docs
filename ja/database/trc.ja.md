{
  "date" : "2021-08-24",
  "keywords" :[ "trc ファイル", "trc ファイル形式", "trc ファイルとは", "ファイル", "trc の例", "trc ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"TRC ファイル形式と,TRC ファイルを作成して開くことができる API について学びます。",
  "title" :"TRC - SQL Server トレース ファイル",
  "linktitle" : "TRC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## .TRC オプション番号
拡張子が .trc のファイルには、Miscrosoft SQL サーバー データベースのアクティビティのトレース結果が含まれています。これらのファイルは、ソフトウェア SQL Server Profiler によって作成されます。通常、Microsoft SQL Server ソフトウェアにパッケージ化されています。データベース管理者は、一連のデータベース ステートメントを分析し、何らかのエラーや警告が疑われる場合にトレース ログを確認できます。これらのファイルは通常、Windows オペレーティング システムの Program Files ディレクトリ内の MSSQL の典型的な LOG フォルダにあります。

## TRC ファイル形式
TRC ファイル形式は、MS SQL サーバーによって最近実行されたステートメントの新しいトレースを自動的に生成するために、SQL Server プロファイラーによって使用されます。 SQL Server プロファイラーは、新しいトレースに対して既定のテンプレートを使用します。ただし、ソフトウェアには、特定のタイプのイベントを監視するための定義済みテンプレートがいくつか含まれています。また、SQL Server Profiler を使用して、トレースに含めるイベント クラスとデータ列を定義するテンプレートを作成することもできます。

### 定義済みのテンプレート
SQL Server プロファイラーに含まれている定義済みのテンプレートの一覧を次に示します。
- **SP_Counts**: ストアド プロシージャの実行動作を経時的にキャプチャします。
- **標準**: トレースを作成するための一般的な開始点。
- **TSQL**: クライアントによって SQL Server に送信されたすべての Transact-SQL ステートメントと発行された時間をキャプチャします。
- **TSQL_Duration**: クライアントによって SQL Server に送信されたすべての Transact-SQL ステートメントとその実行時間をキャプチャし、期間別にグループ化します。
- **TSQL_Grouped**: 特定のクライアントまたはユーザーからのクエリを調査するために使用します。
- **TSQL_Locks**: デッドロック、ロック タイムアウト、およびロック エスカレーション イベントのトラブルシューティングに使用します。
- **TSQL_Replay**: ベンチマーク テストなどの反復チューニングを実行するために使用します。
- **TSQL_SPs**: ストアド プロシージャのコンポーネント ステップを分析するために使用します。
- **チューニング**: データベース エンジン チューニング アドバイザーがデータベースをチューニングするためのワークロードとして使用できるトレース出力を生成するために使用します。
### トレースを Windows パフォーマンス ログ データと関連付ける
SQL Server プロファイラーを使用して、Microsoft Windows パフォーマンス ログを開き、トレースと関連付けるカウンターを選択し、選択したパフォーマンス カウンターをトレースと共に MS SQL Server プロファイラー GUI に表示できます。選択したトレース イベントに関連するパフォーマンス ログ データを示すために、SQL Server プロファイラーのシステム モニターのデータ ウィンドウ ペインに赤い垂直バーが表示されます。


## 参照 ##

* [SQL Server プロファイラー](https://docs.microsoft.com/en-us/sql/tools/sql-server-profiler/sql-server-profiler?view=sql-server-ver15)
