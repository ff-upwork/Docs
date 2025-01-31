{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMV 文件格式",
  "description":"了解 WMV 文件格式和可以创建和打开 WMV 文件的 API。",
  "linktitle" : "WMV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-16"
}

## 什么是一 .wmv 文件？

高级系统格式 (ASF) 是一种数字多媒体容器，主要用于存储和传输媒体流。 Microsoft Windows Media Video (WMV) 是压缩视频格式，Microsoft Windows Media Audio (WMA) 是压缩音频格式以及 Microsoft 开发的 ASF 容器中的其他元数据。一旦使用 Windows Media Video 和 Windows Media Audio 编解码器对 WMV 或 WMA 文件进行编码，它们就会以 .asf 扩展名表示。 WMV 压缩大文件以获得更好的网络传输速率，同时保持视频质量。 WMV 专为在所有 Windows 设备上运行而设计。在电影和电视工程师协会 (SMPTE) 标准化之后，WMV 现在被认为是一种开放的标准格式。

## 历史 ＃＃

在 Microsoft 专有编解码器的帮助下，1999 年开发了新的压缩视频格式，称为 WMV7，它基于 MPEG-4 第 2 部分。在另外两个版本中添加了改进，即 WMV8 和 9。Microsoft 提交了第 9^^th^^ 版本2003 年将 WMV 转为 SMPTE 进行标准化，最终在 2006 年标准化为 SMPTE 421M，也称为 VC-1。 WMV 背后的想法是开发一种可由 Microsoft 支持的所有硬件和软件支持的媒体格式。此外，另一个主要目的是在最佳情况下通过互联网传输视频流。从 SMPTE 标准化后，WMV 也成为了蓝光光盘的视频格式。

## 文件格式规范

＃＃＃ 容器

通常，WMV 被打包到一个 ASF 容器中，但另外，Matroska 或 AVI 容器也可以分别支持它，扩展名为 .mkv 和 .avi。

### Windows 媒体视频 9

尽管 Windows Media Video 9 系列中有各种音频和视频编解码器可用于数字媒体的创作和播放，但 WMV-9 编解码器是最新和最好的视频编解码器，因为它可以从非常低的比特率（即 160 x 10 Kbps 的 120 到 4-8 Mbps 的 1920 x 1080，适用于各种高清视频。

### 编解码器结构

WMV-9 具有 8 位 4:2:0 内部颜色格式。与所有其他流行的视频压缩标准 MPEG-1 和 H.261 一样，WMV-9 使用基于块的运动补偿和空间变换方案。一般来说，我们可以说这些标准借助称为运动矢量 (MV) 的二维量从先前的重构帧执行逐块运动补偿，以表示空间位移。当前块是在从与当前位置偏移运动矢量的相同大小的先前重构帧中预测值的帮助下形成的。最终，残差被计算为运动补偿的预测块与实际块之间的差异。使用线性能量压缩变换对该残差进行变换，然后对其进行量化和熵编码。

量化的变换系数经过熵解码、去量化和逆变换以在解码器端产生残差的近似值，然后将其添加到运动补偿预测中以生成重构。下图显示了编解码器的高级描述。

本节的其余部分将讨论 WMV-9 的新改进，这些改进将其与其他视频编码解决方案（如 MPEG 标准）区分开来。 WMV-9 具有帧内 (I)、预测 (P) 和双向预测 (B) 帧。帧内帧是独立编码且不依赖于其他帧的帧。预测帧是依赖于过去一帧的帧。只有在当前帧之前从最近 (I) 帧开始的所有参考帧都已被解码后，才能对预测帧进行解码。 B 帧是具有两个参考的帧——一个在时间过去，一个在时间未来。 B 帧在它们的参考之后传输，这意味着 B 帧是乱序发送的，以确保它们的参考在解码时可用。 WMV-9 中的 B 帧不用作后续帧的参考。这将 B 帧置于解码循环之外，允许在 B 帧解码期间采用捷径，而不会出现漂移或长期视觉伪影。上述 I、P 和 B 帧的定义适用于逐行和隔行序列。

视频编解码器的性能与其速率失真 (RD) 图进行了比较。这是一条二维曲线，显示了在特定比特率下压缩产生的失真。

WMV-9 通过引入下面列出的各种技术解决了这个问题：

1.自适应块大小变换

2. 有限精度变换集

3.运动补偿

4.量化和反量化

5. 高级熵编码

6.环路滤波

7.高级B帧编码

8. 隔行编码

9. 重叠平滑

10. 低利率工具

11. 衰落补偿

## 参考 ＃＃

* [https://bytescout.com/blog/2018/02/windows-media-video-format.html](https://bytescout.com/blog/2018/02/windows-media-video-format.html)
* [https://en.wikipedia.org/wiki/Windows_Media_Video](https://en.wikipedia.org/wiki/Windows_Media_Video)


