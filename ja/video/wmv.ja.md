{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMVファイル形式",
  "description":"WMV ファイル形式と,WMV ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "WMV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-16"
}

## WMV ファイルとは何ですか?

Advanced Systems Format (ASF) は、主にメディア ストリームの保存と送信を目的として設計されたデジタル マルチメディア コンテナーです。 Microsoft Windows Media Video (WMV) は圧縮されたビデオ形式で、Microsoft Windows Media Audio (WMA) は圧縮されたオーディオ形式で、Microsoft が開発した ASF コンテナー内の追加のメタデータと共に使用されます。 WMV または WMA ファイルが Windows Media ビデオおよび Windows Media オーディオ コーデックでエンコードされると、.asf 拡張子で表されます。 WMV は、ビデオの品質を維持しながら、ネットワーク上での伝送速度を向上させるために大きなファイルを圧縮します。 WMV は、すべての Windows デバイスで動作するように特別に設計されています。 Society of Motion Picture and Television Engineers (SMPTE) による標準化の後、WMV は現在、オープン スタンダード フォーマットと見なされています。

## 歴史 ＃＃

Microsoft 独自のコーデックの助けを借りて、MPEG-4 Part 2 に基づいた WMV7 として知られる新しい圧縮ビデオ形式が 1999 年に開発されました。さらに 2 つのバージョン、つまり WMV8 と 9 で改良が加えられました。Microsoft は 9^^^^ バージョンを提出しました。 2003 年の標準化のために WMV を SMPTE に変換し、最終的に 2006 年に VC-1 としても知られる SMPTE 421M として標準化されました。 WMV の背後にあるアイデアは、Microsoft がサポートするすべてのハードウェアとソフトウェアでサポートできるメディア形式を開発することでした。さらに、もう 1 つの主要な目的は、最適なシナリオでインターネット経由でビデオ ストリームを送信することでした。 SMPTE からの標準化の後、WMV は Blu-ray ディスクのビデオ形式にもなりました。

## ファイル形式の仕様

＃＃＃ 容器

通常、WMV は ASF コンテナーにパックされますが、さらに、Matroska または AVI コンテナーも、それぞれ .mkv および .avi の拡張子でサポートできます。

### Windows メディア ビデオ 9

Windows Media Video 9 シリーズには、デジタル メディアのオーサリングと再生用にさまざまなオーディオおよびビデオ コーデックが用意されていますが、WMV-9 コーデックは、非常に低いビット レート、つまり 160 x 10 Kbps で 120 から 4 ～ 8 Mbps で 1920 x 1080 まで、さまざまな HD ビデオに対応。

### コーデックの構造

WMV-9 には、8 ビット 4:2:0 内部カラー形式があります。他のすべての一般的なビデオ圧縮規格 MPEG-1 および H.261 と同様に、WMV-9 はブロックベースの動き補償と空間変換スキームを使用します。一般に、これらの規格は、動きベクトル (MV) と呼ばれる 2-D 量を使用して、以前に再構築されたフレームからブロックごとの動き補償を実行し、空間変位を通知すると言えます。現在のブロックは、動きベクトルによって現在の位置から変位された同じサイズの前の再構成されたフレームからの値を予測することを利用して形成されます。最終的に、残差は、動き補償された予測ブロックと実際のブロックとの差として計算されます。この残差は、線形エネルギー圧縮変換を使用して変換され、量子化およびエントロピー符号化されます。

量子化された変換係数は、エントロピー デコード、逆量子化、および逆変換されて、デコーダ側で残差の近似値が生成されます。次に、これが動き補償予測に追加され、再構成が生成されます。コーデックの概要を次の図に示します。

このセクションの残りの部分では、WMV-9 の新しい改善点について説明します。これは、MPEG 標準などの他のビデオ コーディング ソリューションとは一線を画しています。 WMV-9 には、イントラ (I)、予測 (P)、および双方向予測 (B) フレームがあります。イントラ フレームは、独立して符号化され、他のフレームに依存しないフレームです。予測フレームは、過去の 1 つのフレームに依存するフレームです。予測フレームの復号化は、最新の (I) フレームから始まる現在のフレームより前のすべての参照フレームが復号化された後にのみ行うことができます。 B フレームは、時間的な過去と時間的な未来の 2 つの参照を持つフレームです。 B フレームは参照に続いて送信されます。つまり、B フレームは順不同で送信され、デコード時に参照が利用できるようになっています。 WMV-9 の B フレームは、後続のフレームの参照として使用されません。これにより、B フレームがデコード ループの外に置かれ、B フレームのデコード中にドリフトや長期的な視覚的アーティファクトなしで近道を行うことができます。上記の I、P、および B フレームの定義は、プログレッシブ シーケンスとインターレース シーケンスの両方に適用されます。

ビデオ コーデックのパフォーマンスは、レート歪み (RD) プロットと比較されます。これは、特定のビットレートでの圧縮によって生じる歪みを示す 2D 曲線です。

WMV-9 では、以下に示すさまざまな手法を導入することで、この問題に対処しています。

1.適応ブロックサイズ変換

2. 限られた精度の変換セット

3. 動き補償

4. 量子化と逆量子化

5.高度なエントロピーコーディング

6.ループフィルタリング

7.高度なBフレームコーディング

8.インターレースコーディング

9. オーバーラップ スムージング

10. 低レートのツール

11.フェージング補正

## 参照 ##

* [https://bytescout.com/blog/2014/10/windows-media-video-format.html](https://bytescout.com/blog/2014/10/windows-media-video-format.html )
* [https://en.wikipedia.org/wiki/Windows_Media_Video](https://en.wikipedia.org/wiki/Windows_Media_Video)
* [http://citeseerx.ist.psu.edu/viewdoc/download?doi#10.1.1.101.488&rep#rep1&type#pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi#10.1 .1.101.488&rep#rep1&type#pdf)
