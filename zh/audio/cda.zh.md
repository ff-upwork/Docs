{
  "date" : "2021-06-09",
  "keywords" :["cda","文件","扩展名","格式","什么是 cda 文件","音乐","cda 文件格式","cda 文件格式规范"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 CDA 文件格式和可以创建、转换和打开 CDA 文件的 API。",
  "title" :"CDA - CD 音轨快捷方式文件",
  "linktitle" : "CDA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## 什么是一 .cda 文件？
带有 .cda 扩展名的文件是 Microsoft Windows 为音频 CD 上的每个音轨生成的小存根文件。这些文件包含轨道时间和 Windows 快捷方式等典型信息，使用户能够访问特定的音轨。 CDA 文件不是音乐，但它们指向存储中某处存在的音乐文件。我们可以说它是位于 CD 上的音频文件的快捷方式。
## CDA 文件格式
CDA 文件格式用于告诉计算机要在 CD 上播放哪个音频文件。因此，CDA 文件从它们所代表的 CD 中分离出来就变得毫无用处。 CDA 文件通常被视为 RIFF 资源。当前版本的 .cda 文件中只有一个名为“CDDA"的块，并且只包含一个名为“FMT"的数据块。该块长 24 个字节。 Windows 创建的标识符被 Windows 95 和 Windows 98 相关的 CD 驱动器使用，其播放器无法连接到 FreeDB 或 CDDB。这样它就可以显示歌曲标题和艺术家姓名，您必须在 cdplayer.ini 文件中手动输入这些信息。

### CDA 文件的组织结构
下表显示了有关典型偏移量的信息：
|偏移 |长度 |内容 |
---|---|---|
| 0x00 | 4 | 4 个 ASCII 字符“RIFF" |
| 0x04 | 4 |以下块的大小：始终为 36 (44 - 8)，占 4 个字节（Intel 顺序）|
| 0x08 | 4 |块标识符：4 个 ASCII 字符“CDDA" |
| 0x0C | 4 | 3 个 ASCII 字符“fmt"后跟一个空格 |
| 0x10 | 4 |块的长度：总是 24，4 个字节（Intel 顺序）|
| 0x14 | 2 | CD 格式的版本，占 2 个字节（Intel 订单）。 2006 年 5 月，始终等于 1。
| 0x016 | 2 |范围的编号，2 个字节（Intel 顺序）。第一首曲目的编号为 1。
| 0x18 | 4 | Windows 为 cdplayer.exe 计算的标识符。 |
| 0x1c | 4 |范围偏移，帧数（Intel 订单）|
| 0x20 | 4 |曲目的持续时间，总帧数（英特尔订单）|
| 0x24 | 1 |范围位置：帧 |
| 0x25 | 1 |范围位置：秒 |
| 0x26 | 1 |范围位置：分钟 |
| 0x27 | 1 |一个空字节（二进制值 0）|
| 0x28 | 1 |曲目时长：帧 |
| 0x29 | 1 |曲目时长：秒 |
| 0x2a | 1 |曲目时长：分钟 |
| 0x2b | 1 |一个空字节（二进制值 0）|

## 参考 ＃＃

* [.cda 文件 - 维基百科提供](https://en.wikipedia.org/wiki/.cda_file)

