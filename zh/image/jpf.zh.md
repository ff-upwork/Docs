{
  "date" : "2021-02-10",
  "keywords" :["jpf 文件","jpf 文件格式","什么是 jpf 文件","文件","jpf 示例","jpf 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPF - 图像文件格式",
  "description":"了解 JPF 文件格式和可以创建和打开 JPF 文件的 API。",
  "linktitle" : "JPF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-10"
}

## 什么是一 .jpf 文件？ ##

带有 .jpf 扩展名的文件是 JPEG 2000 图像编码系统 ISO/IEC 15444 的扩展名，被称为其第 2 部分 ISO/IEC 15444-2。它定义并指定了一组无损（比特保留）和有损压缩方法，用于对连续色调、双电平、灰度、彩色数字静止图像或多分量图像进行编码。 ISO/IEC 15444-1 的第一部分参考了 [JP2](/zh/image/jp2/)，它使用小波技术对无损内容进行编码，是 JPEG 2000 图像文件格式的基础。由于 JPEG 格式的广泛使用，JPF 文件格式没有受到热烈欢迎。 JPF 文件可以使用流行的图像应用程序打开，例如 Adobe Photoshop 2020、Adobe Illustrator 2020 和 CorelDraw Graphics Suite 2020。

## 历史简介

2000 年，联合图像专家组委员会设计了 JP2，目的是通过这种新的基于小波的方法改进他们自己的基于离散余弦变换的 JPEG 标准。 JPEG 委员会的目标是免费提供他们的基线方法。在 20 家公司的 JP2 牌照争夺战中，他们以微弱优势获胜。 JPEG 2000 已被宣布为 ISO 标准，尽管自 2017 年以来大多数 Web 浏览器还没有准备好支持 JPEG 2000。2004 年，ISO/IEC 15444-2 格式被公众接受为 JP2 文件格式的扩展。

## JPF 文件格式

JPF 文件格式定义了用于转换压缩图像数据以进行重建的扩展解码过程。它是一种扩展文件格式，它指定包含用于解释压缩图像数据的信息的扩展码流语法。该扩展标准指定了存储图像元数据的容器，并为将源图像数据转换为压缩图像数据的扩展编码过程提供了指导。

### 文件组织

JPF 是 JPX 文件存储在计算机文件系统中时的正式存储文件格式。此外，其他建议/国际标准可能会定义在 JPX 文件中使用的其他框。但是，JPX 文件中包含的所有信息均应采用框格式；文件中不应找到非 box 格式的字节流。 JPX 文件中框的二进制结构与 [JP2](/zh/image/jp2/) 文件格式中定义的相同。

## 参考 ＃＃

* [JPEG 2000 概述](https://jpeg.org/jpeg2000/)
* [ISO/IEC 15444-2:2004](https://www.iso.org/standard/33160.html)

