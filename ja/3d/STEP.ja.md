---
date: 2019-10-11
keywords: step,.step,step ファイル形式,step ファイルの開き方,.step 拡張子,step 拡張子
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: STEP ファイル形式
linktitle: STEP
description: "STEP ファイル形式と,STEP ファイルを作成して開くことができる API について学習します。"
menu:
  docs:
    parent: "3d"
lastmod: 2020-18-01
---

## .STEP ファイルとは何ですか?

STEP ファイルは、コンピューター支援設計 (CAD) で広く使用されているデータ交換形式です。 1994年にISO委員会により「ISO 10303-21」として標準化されました。 ISO 10303-21 は、EXPRESS データ モデリング言語でデータを表現するためのエンコード メカニズムを定義します。 STEP-ファイルは、p21-ファイルおよび STEP 物理ファイルとも呼ばれます。 STEP ファイルに使用されるファイル拡張子は、.stp および .step です。

## 基本的な歴史

1994 年に、最初のパート 21 仕様が発行されました。 1996 年に発行された技術正誤表によって修正されたいくつかのバグがあります。2002 年に発行された第 2 版には、いくつかのデータ セクションの正誤表と拡張が含まれています。第 3 版は 2016 年に発行され、エンティティと値を外部ファイルに保存できるアンカー セクションと参照セクションが追加されました。文字列の UTF-8 サポートが追加されました。ファイルの内容を検証し、資格情報を検証するために、デジタル署名が追加されました。 ZIP を使用して交換構造を圧縮および保存するためのサポートも追加されました。

## STEP ファイル形式

STEP ファイルのプレーン テキスト形式は、一連のレコードで構成されます。文字セットは、ISO 10646 のコード ポイントとして定義されています。最初のレコードの最初の文字です。コメントは「/*」および「*/」文字で囲みます。最後のレコードには「END-ISO-10303-21;」が含まれています。 STEP ファイルが 2002 バージョンに準拠している場合。 2016 バージョンに準拠している場合、「END-ISO-10303-21;」の後に 1 つ以上のデジタル署名がある場合があります。ターミネーター。改行は「\N\」で示され、改ページは「\F\」で示されます。

STEP ファイルはセクションに分割されており、それらの名前は予約語です。すべてのセクションは「ENDSEC」レコードで終わり、以下に示す順序になっている必要があります。

- **HEADER**: これは必須で繰り返し禁止のセクションです。次のエンティティで構成されます。
  - file_description (mandatory)
  - file_name (mandatory)
  - file_schema (mandatory)
  - schema_population (optional)
  - file_population (optional)
  - section_language (optional)
  - section_context (optional)
- **ANCHOR**: 2016 バージョンで導入されたオプションの非繰り返しセクションです。インスタンスを参照できるように、インスタンスの外部名を定義します。
- **参照**: 2016 年版でも導入されたオプションの非繰り返しセクションです。このセクションの各エントリは、エントリ/値のインスタンス名を外部ファイルのインスタンス/値に関連付けます。
- **DATA**: モデル インスタンスのコア コンテンツを含むオプションの繰り返し可能なセクションです。
- **SIGNATURE**: 2016 年版で導入されたオプションの繰り返し可能なセクションです。ファイルの内容を検証したり、資格情報を検証したりするためのデジタル署名を保持します。

## 参考文献

- [ISO 10303-21 - ウィキペディア](https://en.wikipedia.org/wiki/ISO_10303-21)

