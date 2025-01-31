{
  "date" : "2021-06-11",
  "keywords" :[ "mp2", "mp2 ファイル", "拡張子", "形式", "mp2 ファイルとは", "音楽", "mp2 ファイル形式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"MP2 ファイル形式と,MP2 ファイルを作成,変換,開くことができる API について学びます。",
  "title" :"MP2 - MPEG レイヤー 2 オーディオ ファイル形式",
  "linktitle" : "MP2",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## MP2ファイルとは何ですか?

MPAファイルとも呼ばれるMP2ファイルは、MPEG-1またはMPEG-2のレイヤーIIで圧縮されたオーディオファイルです。 MPEG-1 Audio Layer I および MPEG-1 Audio Layer III ([MP3](/audio/mp3/)) とともに、ISO/IEC 11172-3 で定義された非可逆オーディオ圧縮形式で、オーディオ ファイルのサイズを縮小します。一方、MP3 は MP2 よりもサイズが小さく、インターネット上で利用できるため、人気があります。そのため、MP2 は依然としてオーディオ放送の重要な規格です。

## MP2 ファイル形式

MPEG Audio Layer II (MP2) は、MP3 規格のコア アルゴリズムです。 MPEG-1 オーディオ レイヤー 2 エンコーディングは、MUSICAM オーディオ コーデックから取得されました。これは、EUREKA 研究プログラムの一環として、ドイツでデジタル オーディオ ブロードキャスト (DAB) プロジェクトとして開始されました。 Eureka 147 には、伝送コーディングと多重化、COFDM 変調、および MUSICAM オーディオ コーディング (マスキング パターン ユニバーサル サブバンド統合コーディングおよび多重化) の 3 つの主要な要素が含まれていました。 MUSICAM は、モノラル チャネルあたり 64 ～ 192 kbit/s の範囲のビット レートで高音質を実現できる数少ないエンコーディングの 1 つです。目標は、低遅延、低複雑性、エラー ロバスト性、短いアクセス ユニットを提供し、放送、電気通信、およびデジタル ストレージ メディアへの記録の技術的要件を満たすことでした。

MP2 は、32 の周波数ドメイン コンポーネントを生成する低遅延フィルター バンクを使用して時間ドメインで圧縮できるサブバンド オーディオ エンコーダーです。比較すると、MP3 はハイブリッド フィルター バンクを使用した変換オーディオ エンコーダーです。つまり、時間領域からのハイブリッド変換の後に周波数領域で圧縮が適用されます。 MP2 エンコーダーは、オプションの「ジョイント ステレオ」インテンシティ エンコーディングを使用して、チャネル間の冗長性を利用できます。

### MP2 ファイル形式の仕様

MP2 ファイル形式は、1152 サンプリング間隔の連続するデジタル フレームに基づいており、次の 4 つの形式が可能です。

- モノフォーマット
- ステレオフォーマット
- 強度エンコードされたジョイント ステレオ フォーマット (ステレオとは無関係)
- デュアルチャンネル (無相関) フォーマット
MP2 のいくつかの重要な技術仕様を以下の表に示します。

|仕様|説明|
---|---|
|**サンプリング レート**| 32、44.1、48kHz|
|**ビット レート**|32、48、56、64、80、96、112、128、160、192、224、256、320、および 384 kbit/s|
|**追加のサンプリング レート**|16、22.05、および 24 kHz|
|**追加のビット レート**|8、16、24、40、144 kbit/s|
|**マルチチャンネル サポート**|最大 5 つのフル レンジ オーディオ チャンネルと 1 つの LFE チャンネル (低周波拡張チャンネル)|

## 参照 ##

* [MPEG-1 オーディオ層 II - ウィキペディアによる](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

