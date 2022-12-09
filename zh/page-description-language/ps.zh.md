{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PS 文件格式",
  "description":"了解 PS 文件格式和可以创建和打开 PS 文件的 API。",
  "linktitle" : "PS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是 .PS 文件？ ##

PostScript (PS) 是一种用于桌面和电子出版业务的通用页面描述语言。 PostScript（PS）的主要重点是促进二维图形设计。大多数语言在代码执行之前需要一个不同的编译阶段，而后脚本 (PS) 格式支持运行时直接解释。它的早期版本遵循 Adobe 成像模型的规则，定义了打印页面或显示页面上的图形形状、不同的文本外观和建模图像。 PS的程序能够在组合和打印系统之间相互通信文档描述，保持设备独立和高级。此外，该程序还能够控制显示器上文本和图形的外观。

借助设备的 PostScript 解释器，可以在打印机和其他输出设备上渲染和显示 PostScript 页面描述。由于打印字符、图形形状和图像的命令由解释器执行，因此对于该特定设备，高级 PostScript 描述转换为低级光栅数据格式。通常，不同的应用程序（例如插图画家、文档合成系统和计算机辅助设计 (CAD)）会自动生成 PostScript 页面描述。通常，程序员必须在创建新应用程序时编写 PostScript 程序。但是，程序员可以利用 PostScript 语言的功能，这些功能在任何应用程序中都无法访问，方法是针对该特殊情况编写 PS 程序。

## 历史简介 ＃＃

PostScript 语言的概念首先由 John Warnock 提出。 1966 年，他正在从事纽约港的一个项目。他试图为该项目的数据库开发一个大型 3D 图形的解释器。为了处理这些图形，John Warnock 构思了设计系统语言。与此同时，施乐 PARC 正在为其第一台激光打印机寻找一种定义页面图像的标准方法。尽管 Bob Sproull 和 William Newman 在 1975-76 年开发了 Press 格式（数据格式）来驱动激光打印机，但仍需要一种语言来获得更大的灵活性。 1978 年，Warnock 加入了施乐 PARC 的 Martin Newell 并重写了解释性语言 JaM，该语言后来发展并扩展到 Interpress 语言。 Warnock 于 1982 年 12 月与 Chuck Geschke、Doug Brotz、Ed Taft 和 Bill Paxton 共同创立了 Adobe Systems。他们开始研究一种更简单的语言，称为 PostScript，类似于 1984 年商业发布的 Interpress。Apple 的史蒂夫乔布斯拜访了他们，并建议他们采用 PostScript 来驱动激光打印机。

1985 年 3 月，第一台带有嵌入式 PostScript 解释器的打印机是 Apple 的 LaserWriter，它彻底改变了桌面出版 (DTP)。可靠的技术和广泛的可用性使 PostScript 成为桌面和电子出版的首选语言。在 1990 年，PostScript 语言的解释器是激光打印机的重要组成部分。

## 主要特点 ＃＃

PostScript 语言处理交互式图形和页面描述的能力具有以下特点：

**形状：**本质上是任意的，可能包括直线、曲线、正方形和三次曲线，它们可以是自穿越和断开的（在截面和孔中）。

**绘画操作员：**允许任何厚度、颜色、填充的形状轮廓或允许将形状绘制为剪裁以允许裁剪任何其他图形。

**颜色：**具有灰度、RGB、CMYK 和 CIE 等多样性。特殊种类的颜色被建模为不同的特征：专色、颜色映射、甚至阴影和重复图案。

**文本：** 与图形完全集成。此外，adobe 成像模型允许将文本字符显示为可由任何普通图形操作员操作的图形形状。

**样本图像**：从原始来源（扫描照片）中提取或可能合成。 PostScript 语言提供了多种方法来根据输出设备上的不同颜色模型以任何分辨率重新生成图像。

通用编程语言可以通过在其框架中嵌入 Ps 来利用 PostScript 语言的图形功能。原始数据类型，例如数字、字符、数组和字符串；控制原语，例如循环、过程和条件；以及一些非常规的功能，例如字典在语言中指定。这些特性有助于程序员编写命令来调用更高级别的操作。这些高级操作满足复杂应用程序的需求。这种做法比使用一组固定的基本操作更加紧凑和高效。

用 PostScript 编写的程序可以以 ASCII 源文本的形式生成、交流和解释。整个语言可以以可打印字符和空白的形式定义。这种表示支持程序员轻松地创建、操作和理解语言。此外，通过机器独立性，各种计算机和操作系统之间的文件存储和传输保持方便。

当程序保证与 PostScript 解释器的通信路径完全透明时，语言的二进制编码形式是可能的。 Adobe 建议对 PS 程序的 ASCII 表示进行严格的内聚，以用于文档交换或存档存储。

## 版本##

PS(.ps) 是 PostScript 文档的文件扩展名。英国国家档案馆将 PostScript 文件的五个时间版本分类，在 DSC 版本中定义：版本 1.0、2.0、2.1、3.0、3.1。每个版本都定义了重要的结构注释。封装 PostScript 文件 (EPS) 是 PostScript 文件的一种特殊子类型，它使用语言来指定矩形图形。 PostScript 语言参考手册将 EPS 描述为：“封装的 PostScript (EPS) 文件是一种 PostScript 程序，它以一种可以由其他应用程序导入以嵌入到包含文档中的形式最多描述单个页面"。 PostScript 文档文件可以在其中封装 EPS 文件。 PostScript 的一个附加用途被称为显示 PostScript (DPS)。 DPS 通过使用 PostScript 成像模型和语言的图形引擎生成屏幕图形。

## 参考 ＃＃

* [PostScript 格式系列](https://www.loc.gov/preservation/digital/formats/fdd/fdd000029.shtml)
