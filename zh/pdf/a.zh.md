{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PDF/A 文件格式",
  "description":"了解 PDF/A 文件格式和可以创建和打开 PDF/A 文件的 API。",
  "linktitle" : "A",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# 什么是 PDF/A？ #

PDF/A 是一种 ISO 标准格式，用于以 PDF 格式归档电子文档。其产生的主要原因是为了满足长期归档的要求。该标准通过对文档的组成部分施加一定的限制以实现一致性，从而确保即使在很长一段时间后也能打开存档文件。该格式现在被所有行业广泛采用。 PDFA/A 查看器（如 Adobe Acrobat Reader）确保以这种格式保存的文件即使在将来也可以按照本标准共享的信息打开。

## PDF/A 版本##

PDF/A 于 2005 年 10 月被接受为 ISO 标准。从那时起，它一直在不断改进，随着时间的推移，已经开发了几个进一步的标准。随着时间的推移发布的有关PDF/A标准的信息及其详细信息如下：

* **PDF/A-1：** 2005 年 10 月作为 ISO 19005-1 发布，基于 PDF 1.4
* **PDF/A-2：** 2011 年 6 月作为 ISO 19005-2 发布，基于 PDF 1.7 (ISO 32000-1:2008)
* **PDF/A-3：** 2012 年 10 月作为 ISO 19005-3 发布，基于 PDF 1.7 (ISO 32000-1:2008)

## PDF/A-1 ##

PDF/A-1 标准基于原始 PDF 1.4 版本。 PDF/A-1 标准为 PDF 文件定义了两个级别的一致性。

### PDF/A-1a ###

符合A级，满足PDF/A-1标准规范中的所有要求。 PDF/A-1a 确保可从文档中提取文本。它还保证了集成文本材料的自然阅读过程保持不变。 PDF/A 通过被称为“标记 PDF"的重组，对缩小屏幕上的文本表示能力提出了要求。它旨在通过允许辅助软件来增加身体受损用户对符合文件的可访问性。

### PDF/A-1b ###

PDF/A-1b 是较低级别的一致性，并根据 ISO 19005 标准处理电子文档的视觉外观。它确保页面上的文本和其他内容被统一复制。此 B 级一致性表示最低一致性，以确保一致性文件的呈现视觉外观可长期保存。

## PDF/A-2 ##

PDF/A-2 于 2011 年 7 月由 ISO 标准发布，作为称为 ISO 32001-1 的新标准。这个新标准不仅受益于 PDF 版本直到 1.7 的所有功能，而且作为一个新标准被引入。 PDF/A-2 包括以下功能作为该新标准的一部分。

* PDF/A-2 支持 [JPEG2000](/zh/image/jp2/)，这对扫描文档很有帮助。
* 它支持嵌入 PDF/A 集合，可用于创建具有其他类似文件的容器 PDF
* 与部分支持的 PDF/A-1 相比，它全面支持 PDF 文件的透明度功能。
* PDF/A-2 提供对可选内容的支持，这些内容对制图应用程序和工程图很有用。这些也称为图层，可以根据查看人的要求使其可见或隐藏。
* 它指定了自定义 XMP 元数据的要求
* 将一些较新的注释类型添加到禁止的注释类型列表中。此外，一些较新的评论类型（例如文本编辑评论）已添加到可接受项目列表中。

## PDF/A-3 ##

PDF/A-3 包括第 2 级的所有一致性要求，并允许嵌入其他文件格式（例如 XML、[CSV](/zh/spreadsheet/csv/)、[CAD](/zh/cad/)、[word-processing](/zh/word-processing/) , [spreadsheet](/zh/spreadsheet/) 和其他) 到符合 PDF/A 的文档中。

## 参考 ＃＃

* [PDF/A - 维基百科提供](https://en.wikipedia.org/wiki/PDF/A)
* [白皮书：PDF/A – 基础](https://www.pdf-tools.com/public/downloads/whitepapers/whitepaper-pdfa.pdf)

