{
  "date" : "2021-08-17",
  "keywords" :["udf 文件","udf 文件格式","什么是 udf 文件","文件","udf 示例","udf 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"了解 UDF 文件格式和可以创建和打开 UDF 文件的 API。",
  "title" :"UDF - 通用磁盘格式文件",
  "linktitle" : "UDF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-17"
}

## 什么是一 .udf 文件？
扩展名为 .udf 的文件是一种光盘映像格式，通常用于将文件保存在光学介质上；可用于刻录 DVD、CD 和其他光学介质；使用 UDF 标准中指定的目录结构存储文件集合；允许在目标光盘上删除和修改文件，即使它们已被写入。光学存储技术协会将 UDF 文件系统作为标准，为所有光学介质（例如可重写光学介质和只读介质）形成通用文件系统。

## UDF 文件格式
UDF 文件格式是一种开放的供应商中立文件系统，用于存储各种媒体的计算机数据。它通常用于 DVD 和较新的光盘格式。通常，该软件以批处理的方式掌握 UDF 文件系统，并一次性将其写入光学介质。然而，当它将数据包写入可重写媒体时，UDF 允许在磁盘上创建、删除和更改文件，类似于在可移动媒体（如闪存驱动器或软盘）上的通用文件系统。
### UDF 规格
UDF 标准定义了以下三种文件系统变体：

- **Plain Build**：这是所有 UDF 修订版支持的原始格式。它是在标准的第一个版本中引入的，这种格式可以用于任何类型的支持随机读取或写入访问的磁盘，例如 DVD+RW、硬盘和 DVD-RAM 介质。
- **增值税构建**：专门用于写入一次写入媒体。 VAT 是磁盘上允许写入数据包的附加结构；也就是说，当磁盘上的文件或其他数据被修改或删除时，重新映射物理块。对于一次写入媒体，整个光盘都是虚拟化的，使得一次写入的性质对用户来说是透明的；可以像对待可重写光盘一样对待光盘。
- **备用（RW）构建**：专门用于写入可重写媒体。它添加了一个额外的备用表来管理最终将在已被多次重写的光盘部分上发生的故障。此表保存磨损扇区的跟踪并将它们重新映射到工作扇区。 UDF 的缺陷管理不适用于已经实施另一种形式的缺陷管理的系统，例如用于光盘的 Mount Rainier (MRW)，或用于硬盘驱动器的磁盘控制器。
 




## 参考


* [Windows 图像格式 - 维基百科提供](https://en.wikipedia.org/wiki/Windows_Imaging_Format)

