{
  "date" : "2019-10-11",
  "keywords" :[ "AVI","圧縮オーディオビデオ","ファイル","拡張子","ファイル形式","マルチメディアコンテナ","XVid","DivX","コーデック","リソース交換ファイル形式","RIFF"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AVI ファイル形式 - オーディオ ビデオ インターリーブ ファイル",
  "description":"AVI ファイル形式と,AVI ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "AVI",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-04-23"
}

## AVI ファイルとは何ですか? ##

**AVI** ファイル形式は、Microsoft によって導入されたオーディオ ビデオ マルチメディア コンテナー ファイル形式です。 **XVid** や **DivX** などのいくつかのコーデック (コーダー/デコーダー) を使用して作成および圧縮されたオーディオおよびビデオ データを保持します。さまざまなコーデックを使用して AVI コンテンツをエンコードできるため、取得アプリケーション、つまり AVI プレーヤーは、AVI コンテンツの作成に必要なコーデックがインストールされている場合にのみ、これらを開くことができます。この形式は、すべての **Microsoft Windows** プラットフォームと、他のほとんどすべての主要なプラットフォームでデフォルトでサポートされています。いくつかのアプリケーションと API は、AVI を MP4、MOV、WMV などの他の一般的な形式に作成/保存、読み取り、変換する機能を提供します。

## AVI ファイル形式 ##

.avi 拡張子を持つファイルは AVI ファイルです。 Resource Interchange File Format (RIFF) のサブフォーマットです。 RIFF は、FourCC タグで識別されるブロックまたは「チャンク」にデータを編成します。 AVI ファイルは、RIFF 形式のファイルの単なる 1 つの「チャンク」です。

最初のサブチャンクでは、ファイルのヘッダーは「hdrl」タグで識別されます。その内容には、ビデオの幅、高さ、およびフレーム レートが含まれます。 2 番目のサブチャンクのモーション タグは、ビデオのフレーム レートを表します。 AVI ビデオは、このチャンク内の実際のオーディオ/ビジュアル データで構成されます。ファイルに属する個々のデータ チャンクのファイル内の位置を示す「idx1」タグを持つ 3 番目のオプションのサブチャンクもあります。

### 制限事項 ###

* アスペクト比情報は元の AVI 仕様ではエンコードできませんが、後の OpenDML 仕様 (AVI 2.0) では標準化された方法が提供されています。
* AVI ファイルは映画やテレビのポスト プロダクションで広く使用されていますが、ファイルにタイム コードを追加するさまざまな方法が競合しており、形式の使いやすさに影響を与えています。
* AVI でエンコードされたビデオ ファイルは、エンコードされているフレーム (B フレーム) を超える将来のフレーム データを必要とする圧縮技術を使用できません。
* 可変ビットレート (VBR) の AVI ファイル (サンプル レートが 32 kHz 未満の MP3 オーディオなど) を使用すると問題が発生します。
* 通常使用される標準解像度の長編映画をエンコードする AVI ファイルは、ファイルの使用方法に応じて、1 時間あたり約 5 MB のオーバーヘッドが発生する可能性があります。
* AVI ファイルがフォントや字幕などの添付ファイルに対応できない場合は、字幕をビデオ ストリームにハードコードするか、別のファイルで配布する必要があります。

## 簡単な歴史 ##

AVI は、より堅牢で高度なオーディオおよびビデオ ファイル形式を提供することを目的として、1992 年に Microsoft によって導入されました。この形式は、インターネットの使用によって急速に普及し、個人がクラウドベースのメディア ストレージを介してビデオ ファイルを直接および間接的に共有できるようになりました。

## 参照 ##

* [AVI - ウィキペディアによる](https://en.wikipedia.org/wiki/Audio_Video_Interleave)

