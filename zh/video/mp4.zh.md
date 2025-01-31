---
date: 2019-10-11
keywords: "MP4,文件,扩展名,格式,视频格式,MPEG-4"
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "了解 MP4 文件格式和可创建和打开 MP4 文件的 API。"
title: "MP4 文件格式"
linktitle: "MP4"
menu:
  docs:
    parent: "video"
lastmod: 2021-07-26
---

## 什么是 MP4 文件？ ##

MP4（MPEG-4 Part 14 的缩写）是一种基于 ISO/IEC 14496-12:2004 的文件格式，它基于 QuickTime 文件格式，但正式指定了对初始对象描述符 (IOD) 和其他 MPEG 功能的支持。它主要用于存储视频和音频，但也可用于存储字幕和静止图像。 MP4 文件以 .mp4 扩展名存储。 MP4 是一种国际视听编码标准。与大多数现代容器格式类似，MP4 支持通过 Internet 进行流式传输。由于 MP4 中使用的高压缩率，生成的文件尺寸更小，几乎所有原始质量都保留了下来。

## 历史简介 ＃＃

MP4 规范由运动图像专家组 (MPEG) 开发，基于 2001 年发布的 QuickTime 格式 [MOV](/zh/video/mov/)。MP4 的第一个版本 (ISO/IEC 14496-1:2001)是 MPEG-4 第 1 部分：系统规范的修订版，于 1999 年发布。MP4 文件格式被推广为 ISO 基本媒体文件格式 ISO/IEC 14496-12:2004，它定义了基于时间的媒体文件的一般结构。因此，它被用作其他文件格式的基础。

## MP4 文件的结构##

MP4 是一个可扩展的容器文件，这意味着它没有定义严格的结构，并且允许为每种媒体类型自定义结构和层次结构。 MP4 文件中的数据分为两部分，第一部分包含媒体相关数据，第二部分包含元数据。媒体数据包含音频或视频，元数据指示随机访问的标志、时间戳等。
MP4 中的结构通常称为原子或盒子。原子的最小大小为 8 个字节（前 4 个字节指定大小，接下来的 4 个字节指定类型）。以下是 MP 文件中包含的根级原子的列表：

- **ftyp**：包含文件类型、描述和常用的数据结构。
- **pdin**：包含渐进式视频加载/下载信息。
- **moov**：所有电影元数据的容器。
- **moof**：带有视频片段的容器。
- **mfra**：随机访问视频片段的容器
- **mdat**：媒体的数据容器。
- **stts**：样本到时间表。
- **stsc**：样本到块表。
- **stsz**：样本大小（框架）
- **meta**：包含元数据信息的容器。

以下是 MP4 中使用的二级原子列表：

- **mvhd**：包含视频的完整详细信息的视频标题信息。
- **trak**：带有单个轨道的容器。
- **udta**：包含用户和跟踪信息的容器。
- **iods**：MP4 文件描述符

## 参考 ＃＃

- [MP4 - 维基百科](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

