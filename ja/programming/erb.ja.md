{
  "date" : "2021-09-15", 
  "keywords" :[ "erb","ファイル","拡張子","ファイル形式","erb 実装","プログラミング ガイド","erb の例","eRuby","eRuby ファイル形式","eRuby 言語スクリプト"," eRuby テンプレート", "erb 言語", "ERB Ruby 言語", "eRuby 言語" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ERB - eRuby 言語ファイル",
  "description":"ERB ファイル形式と,ERB ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "ERB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-15"
}

## .ERB オプション番号

eRuby 言語は、テキスト ドキュメントに Ruby を埋め込むテンプレート システムです。 eRuby のテンプレート システムは、ルビ コードとプレーン テキストを組み合わせてフロー コントロールと可変置換を提供するため、メンテナンスが容易になります。 Ruby コードを [HTML](/web/html/) ドキュメントに埋め込むためによく使用されます。これは、АSР、[JSР](/programming/jsp/)、[РHР](/programming/php/)、およびその他のサーバーと同様です。 -サイドスクリプト言語。 ERB Ruby は通常 Web ページを生成します。

Ruby on Rails のビュー モジュールは、ブラウザーでの応答の表示または出力を担当します。最も単純な形式では、ビューはいくつかの統計情報を含む HTML コードのようなものです。ほとんどの場合、統計情報だけでは不十分な場合があります。多くのRailsアプリケーションでは、コントローラーによって作成された動的コンポーネントがビューに表示される必要があります。これは、Embedded Ruby を使用してダイナミックなコンポーネントを生成できるテンプレートを生成することで可能になります。

埋め込み Ruby を使用すると、ルビ コードをビュー ドキュメントに埋め込むことができます。このコードは、実行時にコードが実行された結果のより大きな値に置き換えられます。しかし、ビュー ドキュメントにコードを埋め込む機能を持つことで、MVС フレームに存在する明確な分離を橋渡しするリスクがあります。したがって、開発者は、モデル、ビュー、ソフトウェア モジュール間の責任が明確に分離されていることを確認する責任があります。



## 簡単な歴史 ##

Ruby は 1990 年代半ばに Yukihiro Mаtsumоt® によって設計されました。松本幸宏はRubyの父であり、Ruby界ではマッツの愛称で知られている。 Ruby スクリプトは 1995 年に最初に導入され、Ruby の最初のバージョンは 1995 年にリリースされた Ruby 95 でした。

松本幸宏は、スクリプト言語として簡単に使用できる、完全にオブジェクト指向のプログラミング言語を望んでいました。そう、彼は eRuby 言語を設計しました。松本幸広と石塚圭樹のチャットセッションでは、プログラミング言語である「Соrаl」と「Ruby」の2つの名前が登録され、後に松本幸広は「Ruby」という名前を選択しました。


## 技術仕様 ##

eRuby ファイル形式は、classs、inheritance、abstrасtiоn、роlymоrrhism、enсарsulаtiоn などのオブジェクト指向のプログラム プログラミングのさまざまな形式をサポートします。オブジェクト指向のプログラミング機能により、メンテナンスや開発が容易になります。 eRuby 言語スクリプトは、プログラミング プログラミングの機能もサポートしています。教育プログラムには、特定の問題を解決するためのすべてのプログラムの具体的な手順があります。

eRuby テンプレートは、プログラミングを行う人が簡単かつ迅速にあらゆる Web アプリケーションやプログラムを開発できる豊富な組み込みライブラリを提供します。 eRuby は、一般的なプログラミング言語または多言語プログラミング言語であり、これは、プログラマーがさまざまな種類のアプリケーションおよびプログラムを開発する際に使用できることを意味します。

ERB Ruby 言語はシンプルでソース プログラム言語であり、ユーザーの要件に合わせて変更することもできます。豊富な組み込み機能とツールのさまざまなタイプを提供します。この言語は、自動ガベージ デザイナーの機能も備えています。

eRuby でのコーディングは、他のプログラミング言語への移行が非常に高速です。また、すべてのユーザーが要件に合わせてパーツを変更できるため、柔軟なプログラミング言語でもあります。これは、単一の継承と mixins 機能をサポートし、動的タイリング機能をユーザーに提供します。 eRuby は非常に繊細なプログラミング言語であり、その繊細さゆえに優れたコミュニティを持っています。


## ERB ファイル形式の例 ##

ERB テンプレートのタグのタイプは次のとおりです。

＃＃＃ 表現 ＃＃＃

```
<%= %>
```

```
require 'erb'
x = 500
template = ERB.new("The value of x is: <%= x %>")
puts template.result(binding)
```

### 実行 ###

```
<% %>
```

```
<ul>
<% 4.times do %>

  <li>list item</li>

<% end %>
</ul>
```

### コメント ###

```
<%# %>
```

```
<%# ruby code %>
```

### その他のタグ ###

```
<%2.times do -%> 
    <%= @name %>
<% end -%>

```

### クラスの例 ###

```
class ERBExample
  attr_accessor:variable1
  
  # using bind to access class variables
  def render()
    renderer.result(binding)
  end

  def initialize(variable1)
    @variable1 = variable1
  end

  # Expose private binding() method.
  def get_binding
    binding()
  end
end

example = ERBExample.new(variable1)
renderer = ERB.new(template)
puts output = renderer.result(example.get_binding)

```

## 参照 ＃＃

* [ERB - ウィキペディアによる](https://en.wikipedia.org/wiki/ERuby)



