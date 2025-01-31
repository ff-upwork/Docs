{
  "date" : "2019-10-11",
  "keywords" : [ "txt file", "txt file format", "what is an txt file", "file", "txt example", "txt file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "TXT - Text Document File",
  "description":"Learn about TXT file format and APIs that can create and open TXT files.",
  "linktitle" : "TXT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a TXT file?

A file with .TXT extension represents a text document that contains plain text in the form of lines. Paragraphs in a text document are recognized by carriage returns and are used for better arrangement of file contents. A standard text document can be opened in any text editor or word processing application on different operating systems. All the text contained in such a file is in human-readable format and represented by sequence of characters.

Text files can store large amount of data as there is no limitation on the size of contents. However, text editors opening such large files need to be smart for loading and displaying these. Almost all operating systems come with text editors that allow you to create and edit text files. For example, Windows OS comes with Notepad and Wordpad for this purpose. Similarly, MacOS comes with TextEdit for creating and editing Text Documents. There are, however, other free text editors available as well over the internet that provide you the capability to work with Text Documents like Notepad++ which is far more advanced in terms of functionality.

## File Format Specifications ##

The text file format doesn't have any special file format specifications. Text files have "text/plain" MIME type and have little or no formatting at all. This enables text editors to open such files without any other requirements. The default character set of text files is ASCII that is used for creating and display of text file contents. Characters are encoded using ASCII character set, but this imposes limitation of usage on characters such as Pound Sign, Dollar and Euro sign that can't be represented using the ASCII character set. Thus, text files can also be saved in Unicode format, with UTF-8 being the mostly used.

### Windows Text File Format ###

Text files on Windows OS consists of several lines where each line is made up of a sequence of characters. Each user implied line is defined by combination of two characters i.e. carriage return (CR) and Line Feed (LF). Windows text files can be in ANSI, OEM, Unicode or UTF-8 encoding. The UTF-16 encoding helps save information in a text file that requires two bytes for representation. Such files usually begin with Byte Order Mark (BOM) which communicates the endianness of the file content. It should be noted that other applications on Windows OS can store information in text file format but with different file extensions to represent application specific text. For example, programming languages usually save code in text file but with their own extensions.

### Unix Text File Format ###

All such systems fine a text file as a file whose characters are organized into zero or more lines. Each line is a sequence of zero or more non-newline characters and a terminating newline character, normally LF.

## References ##

* [TXT File Format](https://en.wikipedia.org/wiki/Text_file)
