{
  "date" : "2021-24-02",
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "MKS File Format",
  "keywords" : [ "mks", "matroska video", "mkv format", "file", "format", "video"],
  "description":"Learn about MKS file format for subtitles only created by Matroska and APIs that can create and open MKS files.",
  "linktitle" : "MKS",
  "menu" : {
    "docs" : {
      "parent" : "video"
    }
  },
  "lastmod" : "2021-25-02"
}

## What is an MKS file?

The MKS files are generally known as Matroska files containing subtitles only. Although the Matroska is a general file container, it avoids keeping the information of specific formats. Since subtitles are being used in some of the audio or video containers, Matroska is paying attention to store some common subtitle formats. It helps Matroska to be consistent with the growth rate. You need to follow the points as given below to store the subtitles in Matroska:

- The “.mks”. the extension will be used by the Matroska file (containing only subtitles).
- **CodecPrivate** is being used to store all codecs related information that is global to an entire stream.
- Remove the Start and stop timestamps that are used in a timestamp native storage format. Instead, use the Blocks timestamp and Duration.
- You can use anything with a transparent layer, including a video.  

## Common Subtitle Formats

Here are some brief notes about more common subtitle formats stored in Matroska:

### Images Subtitles
The VobSub subtitle format is the first image subtitle format to import into Matroska. This format is generated by exporting the subtitles from a DVD. The tracks should be separated while storing in Matroska if the VobSub consists of a set of multiple streams.

### SRT Subtitles
The SRT is the most simple and basic of all subtitle formats. It consists of four parts as given below:
 
 1. A number that indicates the sequence of the subtitle.
 2. Subtitle's appearing and disappearing time on the screen.
 3. The subtitle itself.
 4. A blank line to indicate the start of the next subtitle.
 
### SSA/ASS Subtitles
Sub Station Alpha (SSA) is a file format used by the popular subtitle editor SubStation Alpha. The SSA subtitles are widely used by fansubbers. It has the ability to display modern features, e.g. karaoke, positioning, styling, etc.
 
### WebVTT Subtitles
The World Wide Web Consortium (W3C) developed the WebVTT which is abbreviated as “Web Video Text Tracks Format”. This format is being used to mark up external text track resources in connection with the HTML element.

### HDMV presentation graphics subtitles
The HDMV presentation graphics subtitle format (HDMV PGS) is a series of bitmaps and we can't say it text at all. In the other words, you can say it is just a timed sequence of graphic images. To extract the information,  converting PGS to SRT is a necessary process.

### HDMV text subtitles
The HDMV text is known as the textual subtitle format used on Blu-rays. Matroska only allows UTF-8 character set When stores the TextST subtitles.

### Digital Video Broadcasting (DVB) subtitles
The DVB subtitle format was introduced for regulating the transmission and display of several languages subtitling on TV signals. A typical subtitling format would also allow any viewer to watch DVB subtitled transmissions, no matter what is the manufacturer of the transmission systems.


## References ##

- [Matroska Subtitles](https://www.matroska.org/technical/subtitles.html)
