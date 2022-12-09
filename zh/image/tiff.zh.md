{
  "date" : "2019-10-11",
  "keywords" :["tiff 文件","tiff 文件格式","什么是 tiff 文件","文件","tiff 示例","tiff 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TIFF - 图像文件格式",
  "description":"了解 TIFF 文件格式和可以创建和打开 TIFF 文件的 API。",
  "linktitle" : "TIFF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是 .tiff 文件？

TIFF 或 TIF，标记图像文件格式，表示用于在符合此文件格式标准的各种设备上使用的光栅图像。它能够在多个颜色空间中描述双层、灰度、调色板颜色和全彩图像数据。它支持有损和无损压缩方案，以便为使用该格式的应用程序在空间和时间之间进行选择。该格式不依赖于机器，并且不受处理器、操作系统或文件系统等限制。

## TIFF 文件格式简史

TIFF 文件格式最初是由 Aldus 公司于 1986 年秋天在与各种扫描仪制造商和软件开发商进行一系列会议后创建的。 TIFF 文件格式的主要目的是为所有桌面扫描仪供应商提供通用的扫描图像文件格式。从仅支持二进制图像格式开始，随着时间的推移，该格式演变为支持灰度和彩色图像。 TIFF 文件格式规范的初始版本可以标记为 Reivision 3.0，因为有两个早期的草案版本。 1988 年发布了主要修订版 5.0，增加了对调色板彩色图像和 LZW 压缩的支持。此后，TIFF 文件格式的 6.0 版于 1992 年发布。 1994 年，Adobe Systems 收购了 Aldus，这些规范现在由 Adobe Systems 提供和维护。

## TIFF 文件格式规范

TIFF 文件格式是可扩展的，并且经过多次修改，允许包含无限量的私人或特殊用途信息。 TIFF 文件以 8 字节的标头开头，其中字节是从 0 到 N 的数字。可能的最大 TIFF 文件长度为 2**32 字节。该文件以直接指向图像文件 (IFD) 的 8 字节图像文件头开始。 IFD 包含有关图像的信息以及指向实际图像数据的指针。

### TIFF 文件头

8 字节的 TIFF 文件头包含以下信息：

**字节 0-1：** 文件中使用的字节顺序。合法值为：“II"(4949.H)“MM"(4D4D.H)。

在“II"格式中，对于 16 位和 32 位整数，字节顺序始终是从最低有效字节到最高有效字节。这称为 little-endian 字节顺序。在“MM"格式中，对于 16 位和 32 位整数，字节顺序总是从最高有效到最低有效。这称为大端字节序。

**字节 2-3：** 一个任意但仔细选择的数字 (42)，进一步将文件标识为 TIFF 文件。字节顺序取决于字节 0-1 的值。

**字节 4-7：** 第一个 IFD 的偏移量（以字节为单位）。该目录可以位于文件头之后的任何位置，但必须以单词边界开始。特别是，图像文件目录可能跟随着它所描述的图像数据。读者必须遵循指针可能指向的任何位置。术语字节偏移在本文档中始终用于指代相对于 TIFF 文件开头的位置。文件的第一个字节的偏移量为 0。

### 图像文件目录

IFD 包含有关图像的信息以及指向实际图像数据的指针。它由 2 字节的目录条目数（即字段数）组成，然后是 12 字节的字段条目序列，后跟下一个 IFD 的 4 字节偏移量（如果没有，则为 0）。 TIFF 文件中必须至少有 1 个 IFD，并且每个 IFD 必须至少有一个条目。

#### IFD 条目

每个 12 字节的 IFD 条目采用以下格式。


|字节|说明
---|---|
|0-1|标识字段的标签
|2-3|字段类型
|4-7|指定类型的计数
|8-11|Value Offset，该字段的Value的文件偏移量（以字节为单位）。该Value应该从字边界开始；因此，相应的值偏移量将是偶数。此文件偏移量可能指向文件中的任何位置，即使在图像数据之后

TIFF 字段是由 TIFF 标记及其值组成的逻辑实体。这个逻辑概念被实现为一个 IFD 条目，如果它不适合值/偏移部分，则加上实际值，即 IFD 条目的最后 4 个字节。在大多数情况下，术语 TIFF 字段和 IFD 条目是可以互换的。

### 基线 TIFF ###

Baseline TIFF 是 TIFF 的核心，是所有主流 TIFF 开发人员都应在其产品中支持的要素。符合 TIFF 格式必须遵守基线 TIFF 要求。这些要求在规范文档 6.0 中有详细记录。

#### 每个文件有多个图像####

TIFF 文件中可能有多个 IFD。每个 IFD 定义一个子文件。子文件的一种潜在用途是描述相关图像，例如传真传输的页面。不需要基线 TIFF 阅读器来阅读除第一个之外的任何 IFD。

#### 图像类型####

基线 TIFF 图像具有以下类型：

**双层：**双层图像包含两种颜色——黑色和白色。 TIFF 允许应用程序以白色为零或黑色为零格式写出二级数据。记录此信息的字段称为**PhotometricInterpretation**。

* RGB全彩

Bilevel图像的PhotometricInterpretation信息如下：

标签 = 262 (106.H)
类型 = 短
**价值观**

|价值|说明|
---|---|
|0|对于二级和灰度图像：0 被成像为白色。最大值被成像为黑色。这是 Compression#2| 的正常值
|1|黑即零。对于双层和灰度图像：0 被成像为黑色。最大值被成像为白色。如果为 Compression#2 指定此值，则图像应反转显示和打印。|

**灰度：**灰度图像是双层图像的概括。双层图像只能存储黑白图像数据，但灰度图像也可以存储灰度阴影。要描述此类图像，您必须添加或更改以下字段。其他必填字段与双层图像所需的字段相同。对于灰度图像，压缩 #1 或 32773 (PackBits)。在 Baseline TIFF 中，灰度图像既可以存储为未压缩数据，也可以使用 PackBits 算法进行压缩。

**BitsPerSample** 灰度图像信息如下：

标签 = 258 (102.H)
类型 = 短

每个组件的位数。基线 TIFF 灰度图像的允许值为 4 和 8，允许 16 或 256 种不同的灰度。

**调色板颜色：** 调色板颜色图像类似于灰度图像。它们每个像素仍然有一个分量，但分量值用作完整 RGB 查找表的索引。要描述此类图像，您需要添加或更改以下字段。其他必填字段与灰度图像相同。
Palette-Color 图像的 PhotometricInterpretation 信息如下：

PhotometricInterpretation = 3（调色板颜色）。
ColorMapTag = 320 (140.H)
类型 = 短
N = 3 * (2 BitsPerSample)

该字段为调色板颜色图像定义了红-绿-蓝颜色映射（通常称为查找表）。在调色板颜色图像中，像素值用于索引 RGB 查找表。例如，一个值为 0 的调色板颜色像素将根据第 0 个红色、绿色、蓝色三元组显示。在 TIFF 颜色映射中，所有红色值首先出现，然后是绿色值，然后是蓝色值。在 ColorMap 中，黑色用 0,0,0 表示，白色用 65535、65535、65535 表示。

**RGB 全彩：** 在 RGB 图像中，每个像素由三个分量组成：红色、绿色和蓝色。没有 ColorMap。要描述 RGB 图像，您需要添加或更改以下字段和值。其他必填字段与调色板颜色图像所需的字段相同。

BitsPerSample = 8,8,8。 Baseline TIFF RGB 图像中的每个分量都是 8 位深。

PhotometricInterpretation = 2 (RGB) 并且没有 ColorMap。

标签 = 277 (115.H)
类型 = 短
每个像素的组件数。对于 RGB 图像，此数字为 3，除非存在额外的样本。

## 参考 ＃＃

* [TIFF 文件格式 - 维基百科](https://en.wikipedia.org/wiki/TIFF)
