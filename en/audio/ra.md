---
date: 2019-12-13
keywords: ra, ra file format, .ra extension, real audio file format, ra audio format, RealAudio file format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: Learn about RA file format and APIs that can create and open RA files.
title: RA File Format
linktitle: RA
menu:
  docs:
    parent: "audio"
lastmod: 2020-28-12
---

## What is a RA file?

RealAudio (RA) is a proprietary audio format developed by Real Networks, Inc. and released in April 1995. It uses the .ra extension for its files. It uses low-bitrate as well as high fidelity audio codecs. RA was used for audio streaming over the internet by many internet radio stations. The BBC website used RA heavily until 2009 but discontinued in March 2011.

## File Extension by RealNetworks ##

RealNetworks used the RA file format for audio. RealNetworks started offering video format ([RealVideo](/video/rv/)) in 1997 with the .rv extension. [RealMedia (RM)](/video/rm/) was used for the combination of audio and video formats. With the latest release of RealProduce (Real's encoder), RV format is used for video files and [RealMedia Variable Bitrate (RMVB)](/video/rmvb/) format is used for VBR (Variable bitrate) video files.

## Streaming Audio ##

RA was developed as a streaming media format and can be streamed using HTTP. The audio file starts playing as soon as the first part of the file is received and continues playing as the rest of the file is downloaded.

The first version of the RealAudio used the proprietary PNA or PNM protocol to stream audio. Later they switched to IETF standardized RTSP (Real Time Streaming Protocol) to manage connections. To send data, they used the RDT (Real Data Transfer) protocol. The protocol was kept secret initially but later some of it was made public through the Helix project.

To stream RealAudio files, the majority of pages link to the RAM (Real Audio Metadata) or SMIL (Synchronized Multimedia Integration Language) file. This file is used to load the user's media player and stream the audio from the URL contained in the file.

## RealAudio Audio Codecs ##

Here is a list of audio codecs each identified by a four character code along with the version of RealAudio that introduced it.

|Codec|RealAudio Version|
|---|---|
|lpcJ and 14_4|1|
|28_8|2|
|dnet|3|
|sipr|4/5|
|cook|6|
|atrc|8|
|raac|9|
|racp|10|
|ralf|10|

## References ##

- [RealAudio - Wikipedia](https://en.wikipedia.org/wiki/RealAudio)
