{
  "date" : "2021-02-15",
  "keywords" :[ "asf ファイル", "asf ファイル形式", "asf ファイルとは", "ファイル", "asf 例", "asf ファイル拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASF - 高度なシステム ファイル形式",
  "description":"ASF ファイル形式と,ASF ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "ASF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## .ASF オプション番号

拡張子が .asf のファイルは、ネットワーク経由でデジタル メディア ストリームを保存および再生するためのマルチメディア ファイル形式です。これは、オンライン ストリーミング用のビデオ コンテンツとオーディオ コンテンツの両方を持つことができるコンテナ ファイル形式です。 ASF ファイルを見つけることはめったになく、ASF ファイルを指定する Windows Media オーディオ ([WMA](/audio/wma/)) および Windows Media ビデオ ([WMV](/video/wmv/)) ファイルに出くわす可能性が高くなります。それぞれのコーデックでエンコードされたコンテンツを持つ。 Windows Media ファイルは、Windows Media フォーマット SDK を使用して作成および読み取ることができます。

## ASF ファイル形式

ASF ファイルは、複数の独立または従属ストリームで構成できます。これには、マルチチャンネル オーディオの複数のオーディオ ストリームまたは複数のビットレート ビデオ ストリームを含めることができます。複数のビットレートにより、ストリームは異なる帯域幅での伝送に適したものになります。さらに、ASF ファイル内のストリームは、圧縮または非圧縮形式にすることができます。最高の圧縮率は、Microsoft Windows Media オーディオおよびビデオ 9 シリーズ コーデックで実現されます。 ASF ファイル形式の完全な仕様は、[Microsoft Web サイト](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc) で入手できます。

### ASF 最上位ファイル構造

ASF ファイルには、次の 3 種類の最上位オブジェクトが論理的に含まれています。

* `Header Object` - 必須で、すべての ASF ファイルの先頭に配置する必要があります
* `Data Object` - 必須であり、ヘッダー オブジェクトに従う必要があります
* `Index Object(s)` - オプションですが、ASF ファイルへの時間ベースのランダム アクセスを提供するのに役立ちます

次の図は、ASF ファイルの最上位のファイル構造を示しています。

![ASF File Structure](../asf.png "ASF File Structure")

#### ASF トップレベル ヘッダー オブジェクト

Header オブジェクトは、ASF ファイルの先頭に既知のバイト シーケンスを提供し、オプションで書誌情報などのメタデータを含めることができます。データオブジェクト内の情報を正しく解釈するために必要なすべての情報が含まれています。ヘッダー オブジェクトには、以下を含むがこれらに限定されないいくつかの標準オブジェクトを含めることができます。

* ファイル プロパティ オブジェクト - グローバル ファイル属性が含まれます。
* ストリーム プロパティ オブジェクト - デジタル メディア ストリームとその特性を定義します。
* ヘッダー拡張オブジェクト - 下位互換性を維持しながら、追加機能を ASF ファイルに追加できるようにします。
* 内容説明オブジェクト - 書誌情報が含まれています。
* スクリプト コマンド オブジェクト - 再生タイムラインで実行できるコマンドが含まれています。
* マーカー オブジェクト - ファイル内の名前付きジャンプ ポイントを提供します。

ヘッダー オブジェクトは、次の構造を使用して表されます。

|フィールド名 |フィールドタイプ |サイズ (ビット)|
---|---|---|
|オブジェクトID| GUID| 128|
|オブジェクトサイズ| QWORD| 64|
|ヘッダー オブジェクトの数| DWORD| 32|
|予約済み1|バイト| 8|
|予約済み2|バイト| 8|

#### ASF トップレベル データ オブジェクト

ASF ファイルのすべてのデジタル メディア データはデータ オブジェクトに含まれ、ASF データ パケットの形式で格納されます。各データ パケットは固定長で、1 つまたは複数のデジタル メディア ストリームのデータが含まれています。

#### ASF トップレベル インデックス オブジェクト

ASF トップレベルのインデックス オブジェクトには、次の 2 つのタイプがあります。

* `Simple Index Object` - ASF ファイル内のビデオ データの時間ベースのインデックスが含まれています。インデックス エントリ間の時間間隔は一定で、Simple Index オブジェクトに格納されます。
* `Index Object` - 形式が類似している Index オブジェクト、メディア オブジェクト インデックス オブジェクト、およびタイムコード インデックス オブジェクトを指します。シンプル インデックス オブジェクトと同様に、インデックス オブジェクトは一定の時間間隔でインデックスを作成しますが、ビデオ ストリームに限定されません。

## 参考文献

* [ASF ファイル形式 - Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)
* [QuickTime ファイル形式 - ウィキペディア](https://en.wikipedia.org/wiki/QuickTime_File_Format)

