{
  "date" : "2021-08-09",
  "keywords" :[ "cso ファイル","cso ファイル形式","cso ファイルとは","ファイル","cso の例","cso ファイルの拡張子","拡張子","形式","iso","DAX 圧縮" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"CSO ファイル形式と,CSO ファイルを作成して開くことができる API について学びます。",
  "title" :"CSO - 圧縮された ISO ディスク イメージ",
  "linktitle" : "CSO",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-09"
}

## .CSO オプション番号

拡張子が .cso のファイルは、圧縮された ISO イメージ ファイルです。 CSO は、DAX 圧縮方法の代替手段です。 CISOとしても知られています。 [ISO](/compression/iso/) ファイルを圧縮する最初の方法であり、通常、PlayStation Portable のものをアーカイブするための推奨される方法です。この形式は Deflate 圧縮を使用し、最大 9 つの圧縮レイヤーを含めることができます。イメージの作成には、Prometheus や YACC などのソフトウェアが使用されます。

## CSO ファイル形式

CSO ファイル形式は、より多くのメモリ領域を節約するための ISO の最初の圧縮方法でした。強化は、より良い圧縮のために時々行われました。 CSO は、9 つのレベルのプリセットを持つ Deflate 圧縮を使用しています。通常、各レベルは 2 KiB ブロックを個別に処理できます。最高レベルの圧縮では、ディスク ストリーミングに大きく依存するソフトウェアのロード時間が長くなり、遅くなる可能性がありますが、低レベルでもかなりの圧縮を実行できます。

### CSO ファイル構造

CSO ファイル形式には、24 バイトのヘッダー、データ ブロック、およびインデックス テーブルが含まれます。 1 バイトより大きいフィールドでは、リトル エンディアンが想定されます。 PlayStation Portable のアーキテクチャのエンディアンは次のとおりです。

#### ヘッダー

| |オフセット (バイト) |名前 |サイズ (バイト) |目的 |
----------|----------|--------------|---------|
| | 0x0 |魔法 | 4 |常に CISO、または 32 ビット整数として読み取られる場合は 0x4F534943。このフィールドは、CSO ファイルを識別するために使用されます。このフィールドは、CSO の他の派生物では異なる場合があることに注意してください。たとえば、ZSO はマジック コード ZISO を使用しました。 | |
| | 0x4 |ヘッダーサイズ | 4 |元の CSO「v1」ファイル形式の場合、このフィールドは無視されるため、正確である必要はありません。ただし、「v2」および ZSO 形式では、このフィールドは常に 0x18 (24 バイト) である必要があります。 | |
| | 0x8 |非圧縮サイズ | 8 |元の圧縮されていない ISO のサイズ (バイト単位)。 | |
| | 0x10 |ブロックサイズ | 4 |圧縮前の各データ ブロックのバイト単位のサイズ。通常は、各 ISO 9660 セクターのサイズと同じ 2048 バイトです。 | |
| | 0x14 |バージョン | 1 |使用中のファイル形式のバージョン。 "v1" 形式の場合、値は 0 または 1 にすることができます。"v2" 形式の場合、これは 2 にする必要があります。さらに、ZSO 形式では、これを 1 にする必要があります。
| | 0x15 |インデックスの配置 | 1 |各インデックス エントリの位置合わせ。ビット単位で指定します。 | |
| | 0x16 |予約済み | 2 |このフィールドは使用されません。 「v1」形式では、このフィールドは無視され、任意の値が含まれる可能性があります。 「v2」形式では、このフィールドはゼロでなければなりません。 | |

#### 索引表

インデックス テーブルには、各データ ブロックの位置を示す 4 バイトのエントリと、ファイルの最後を指す追加の最後のエントリが含まれます。
各エントリーの内容は以下の通りです。
| |ビット | ビット |長さ |マスク | マスク名前 |目的 |
-----|-----|----|-------|------------|
| | 0 | 31 | 0x7FFFFFFFF |ポジション |このフィールドは、ヘッダーで指定されたインデックス アラインメントによって左にシフトされると、データ ブロックの開始位置を示します。 | |
| | 31 | 1 | 0x80000000 |圧縮タイプ | ZSO 形式にも同様のセマンティクスがありますが、0 は Deflate ではなく LZ4 を表すという点だけです。 「v2」形式。ブロック サイズがファイル ヘッダーで指定されたブロック サイズ以上の場合、ブロックは圧縮されていないと暗黙的に見なされます。 | |

#### データブロック

データ ブロックは、圧縮されていないデータまたは圧縮されたデータで構成されます。ブロックのサイズは、その位置を取得し、次のブロックの位置から差し引くことによって計算されます。インデックス アラインメントが 0 より大きい場合、ブロック サイズが保持するデータよりも大きい可能性があります。


## 参考文献

* N/A


