{
  "date" : "2019-12-12",
  "keywords" :[ "SQLite", "拡張子", "ファイル", "ファイル形式", "データベース ファイルの種類", "データベース ファイル形式", "データベース ファイル" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"SQLITE ファイルを作成して開くことができる SQLITE ファイル形式と API について学びます。",
  "title" :"SQLiteファイル形式",
  "linktitle" : "SQLITE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-09"
}

## SQLite ファイルとは何ですか?

拡張子が .sqlite のファイルは、[SQLite](https://www.sqlite.org/index.html) ソフトウェアで作成された軽量の SQL データベース ファイルです。これはファイル自体のデータベースであり、自己完結型の完全な機能を備えた信頼性の高い [SQL](/database/sql/) データベース エンジンを実装しています。 SQLite データベース ファイルを使用すると、これらのファイルをネットワーク経由で簡単に交換するだけで、システム間でリッチ コンテンツを共有できます。ほとんどすべてのモバイルとコンピューターは、データの保存と共有に SQLite を使用しており、クロスプラットフォーム アプリケーションのファイル形式として選択されています。コンパクトな使用と使いやすさのために、他のアプリケーション内にバンドルされています。 C、[C#](/programming/cs/)、[C++](/programming/cpp/)、[Java](/programming/java/)、[PHP](/programming/php/) などのプログラミング言語用の SQLite バインディングが存在します。 )、および他の多く。

## SQLite ファイル形式

実際の SQLite は、SQLite ファイル形式を使用して SQLite RDBMS を実装する C 言語ライブラリです。日々新しいデバイスが進化しているため、そのファイル形式は古いデバイスに対応するために下位互換性が保たれています。 SQLite ファイル形式は、データの長期アーカイブ形式と見なされます。

### データベースファイル

SQLite データベースは、2 つのファイルによって完全に維持されます。
* メイン データベース ファイル - SQLite データベースの完全な状態が含まれています
* ロールバック ジャーナル - 追加情報を 2 番目のファイルに保存し、トランザクションの実行中に使用されます。 SQLite が WAL モードの場合、書き込みヘッド ログ ファイルが維持されます。

#### ジャーナル ファイル

このファイルは、コンピューターのクラッシュなどで最後のトランザクションを完了できなかった場合に備えて、すべての情報を維持することを目的としています。このファイルは、データベース ファイルを一貫した状態に復元するために使用されます。

#### ページ

メインの SQLite データベース ファイルは、1 つまたは複数のページで構成されます。任意の時点で、メイン データベース内のすべてのページには、次のいずれかの 1 つの用途があります。

*ロックバイトページ
* フリーリストページ
* フリーリスト トランク ページ
* フリーリストのリーフ ページ
* Bツリーページ
* A table b-tree 内部ページ
* テーブル b-tree リーフ ページ
* インデックス b-tree 内部ページ
* インデックス B ツリー リーフ ページ
* ペイロード オーバーフロー ページ
* ポインター マップ ページ

SQLite データベース ファイルのサイズは、数キロバイトから数ギガバイトまでさまざまです。

### SQLite ヘッダー

SQLite データベース ヘッダーは、データベース ファイルの最初の 100 バイトにあります。すべての有効な SQLite データベース ファイルは、16 バイト (16 進数) で始まります。

|オフセット|サイズ|説明|
---|---|---|
|0|16|ヘッダー文字列: "SQLite フォーマット 3\000"|
|16|2|データベースのページ サイズ (バイト単位)。 512 から 32768 までの 2 の累乗、または 65536 のページ サイズを表す値 1 である必要があります。|
|18|1|ファイル形式書き込みバージョン。レガシーの場合は 1。 WAL の場合は 2。|
|19|1|ファイル形式の読み取りバージョン。レガシーの場合は 1。 WAL の場合は 2。|
|20|1|各ページの最後にある未使用の「予約済み」スペースのバイト数。通常は 0 です。|
|21|1|埋め込まれたペイロードの最大部分。 64 歳である必要があります。|
|22|1|埋め込まれたペイロードの最小部分。 32 歳である必要があります。|
|23|1|葉のペイロード部分。 32 歳である必要があります。|
|24|4|ファイル変更カウンター。|
|28|4|ページ単位のデータベース ファイルのサイズ。 「ヘッダー内データベース サイズ」。|
|32|4|最初のフリーリスト トランク ページのページ番号。|
|36|4|フリーリスト ページの総数。|
|40|4|スキーマ Cookie。|
|44|4|スキーマ形式番号。サポートされているスキーマ形式は、1、2、3、および 4 です。|
|48|4|デフォルトのページ キャッシュ サイズ。|
|52|4|自動バキューム モードまたはインクリメンタル バキューム モードの場合は最大のルート B ツリー ページのページ番号、それ以外の場合は 0。
|56|4|データベースのテキスト エンコーディング。値 1 は UTF-8 を意味します。値 2 は UTF-16le を意味します。値 3 は UTF-16be を意味します。|
|60|4|user_version プラグマによって読み取られ、設定された「ユーザー バージョン」。|
|64|4|インクリメンタル バキューム モードの場合は True (ゼロ以外)。それ以外の場合は false (ゼロ)。|
|68|4|PRAGMA application_id によって設定された「アプリケーション ID」。|
|72|20|拡張用に予約されています。ゼロでなければなりません。|
|92|4|バージョン有効番号。|
|96|4|SQLITE_VERSION_NUMBER|

## 参照 ##

* [SQLite ファイル形式 - SQLite](https://www.sqlite.org/fileformat2.html)
* [SQLite - ウィキペディア](https://en.wikipedia.org/wiki/SQLite)
* [SQLite - C 言語仕様](https://www.sqlite.org/c3ref/intro.html)

