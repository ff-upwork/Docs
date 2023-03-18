{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"OSR ファイル形式と,OSR ファイルを作成して開くことができる API について学びます。",
  "title" :"OSR ファイル - osu! リプレイ ファイル形式",
  "linktitle" : "OSR",
  "menu" : {
    "docs" : {
      "identifier":"game-osr",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## .OSR ファイルとは何ですか?

OSR ファイルは、[osu!ゲーム](https://osu.ppy.sh/home)。大須！は、音楽に合わせてマウスをクリックするリズムゲームです。ユーザーが再生した曲、ヒットとミス、曲の再生日時、総合ランキングが OSR ファイルに記録されます。この OSR ファイルは、再生のために他のユーザーと共有できます。 OSR ファイルでは、ビートマップ ファイルが「Songs」フォルダに存在する必要があります。

**OSR ファイル形式の MIME タイプ:** x-osu-replay

## OSR ファイル形式

OSR ファイルは、固定長と可変長のデータ フィールドを持つバイナリ ファイルとして保存されます。

|データ型|フォーマット|
---|---|
|Byte |リプレイのゲームモード (0 = osu! Standard, 1 = Taiko, 2 = Catch the Beat, 3 = osu!mania)|
|整数 |リプレイが作成されたときのゲームのバージョン (例: 20131216)|
|文字列 |osu!ビートマップ MD5 ハッシュ|
|文字列|プレイヤー名|
|文字列|オス！リプレイ MD5 ハッシュ (リプレイの特定のプロパティを含む)|
|短い| 300 の数|
|短い|スタンダードで100番台、太鼓で150番台、CTBで100番台、マニアで100番台の数|
|短い|数はスタンダードで50代、CTBで小実、マニアで50代|
|短い|スタンダードで激撃数、マニアで最大300発|
|短い|スタンダードでカトゥの数、マニアで200台|
|短い|ミス数|
|整数|スコアレポートに表示される合計スコア|
|短い|スコアレポートに表示される最大のコンボ|
|バイト|パーフェクト/フル コンボ (1 = ミスなし、スライダー ブレイクなし、早期完成スライダーなし)|
|整数|使用されるモッド。 mod 値のリストについては、以下を参照してください。|
|文字列|ライフ バー グラフ: カンマで区切られた u/v のペア。ここで、u は曲のミリ秒単位の時間、v は 0 から 1 の浮動小数点値で、指定された時点でのライフの量を表します (0 = ライフ バーは空、1 = ライフバーがいっぱい)|
|長い|タイム スタンプ (Windows ティック)|
|整数|圧縮された再生データの長さ (バイト単位)|
|Byte |Array 圧縮リプレイデータ|
|長い|オンラインスコアID|
|ダブル|追加の mod 情報。 Target Practice が有効な場合にのみ表示されます。|

## 参考文献

※【押忍！リズムゲーム】(https://osu.ppy.sh/home)
* [OSR ファイル形式](https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)
