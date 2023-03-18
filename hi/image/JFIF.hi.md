---
date: 2020-08-12
keywords: jfif, .jfif, jfif फ़ाइल स्वरूप, jfif फ़ाइलें कैसे खोलें, .jfif एक्सटेंशन, jfif एक्सटेंशन
लेखक:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JFIF फ़ाइल - एक .jfif फ़ाइल क्या है?
linktitle: JFIF
description: "JFIF फ़ाइल स्वरूप और API के बारे में जानें जो JFIF फ़ाइलें बना और खोल सकते हैं।"
menu:
  docs:
    parent: "image"
lastmod: 2021-21-01
---

## जेएफआईएफ फाइल क्या है?

JFIF (JPEG फाइल इंटरचेंज फॉर्मेट (JFIF)) एक इमेज फॉर्मेट फाइल है जो .jfif एक्सटेंशन का उपयोग करती है। जेएफआईएफ जटिलता को कम करके और इसकी सीमाओं को हल करके जेआईएफ (जेपीईजी इंटरचेंज फॉर्मेट) पर बनाता है।

## जेएफआईएफ का संक्षिप्त इतिहास

JFIF दस्तावेज़ विकास का नेतृत्व एरिक हैमिल्टन ने किया था और पहले संस्करण पर एक समझौता 1991 के अंत में स्थापित किया गया था। संस्करण 1.02 7 सितंबर, 1992 को प्रकाशित हुआ था। RFC 2046 ने निर्दिष्ट किया कि JFIF प्रारूप का उपयोग इंटरनेट पर JPEG छवियों को प्रसारित करने के लिए किया जाता है। JFIF को 2009 में ECMA द्वारा प्रकाशित किया गया था और 2011 में ITU-T द्वारा इसकी सिफारिश T.871 के रूप में और ISO/IEC द्वारा 2013 में ISO/IEC 10918-5 के रूप में मानकीकृत किया गया था।

## जेएफआईएफ फ़ाइल स्वरूप ##

JFIF फ़ाइल में JPEG मानक के भाग 1 में परिभाषित मार्करों का एक क्रम होता है। प्रत्येक मार्कर में दो बाइट्स होते हैं (FF के बाद एक बाइट होती है जो मार्कर के प्रकार को निर्दिष्ट करती है)। मार्कर या तो स्टैंड-अलोन हो सकते हैं या मार्कर सेगमेंट की शुरुआत का संकेत दे सकते हैं।

जेएफआईएफ वाई, सीबी, सीआर जैसे कई घटकों को अलग-अलग संकल्प रखने की अनुमति देता है लेकिन उनके संरेखण को परिभाषित नहीं किया गया है। जेपीईजी के विपरीत, जेएफआईएफ संकल्प और पहलू अनुपात की जानकारी प्रदान कर सकता है। JFIF उपयोग किए जाने वाले रंग मॉडल को भी परिभाषित करता है।

### फ़ाइल संरचना ##

|सेगमेंट|कोड|विवरण|
|---|---|---|
|SOI|FF D8|छवि की शुरुआत|
|JFIF-APP0|FF E0 s1 s2 4A 46 49 46 00 ...||
|JFXX-APP0|FF E0 s1 s2 4A 46 58 58 00 ...||
|अतिरिक्त मार्कर खंड|
|एसओएस|एफएफ डीए|स्कैन की शुरुआत|
||कंप्रेस्ड इमेज डेटा||
|ईओआई|एफएफ डी9|छवि का अंत|

जेएफआईएफ मानक निम्नलिखित खंडों को परिभाषित करता है:

### JFIF APP0 मार्कर खंड ###

यह एक अनिवार्य खंड है जिसमें छवि पैरामीटर शामिल हैं। इसमें एक एम्बेडेड असम्पीडित थंबनेल भी हो सकता है।

|फ़ील्ड|साइज़ (बाइट्स)|विवरण|
|---|---|---|
|APP0 मार्कर|2|FF E0|
|लंबाई|2|APP0 मार्कर को छोड़कर खंड की लंबाई|
|पहचानकर्ता|5|JFIF (4A 46 49 46 00) ASCII में एक शून्य बाइट द्वारा समाप्त |
|JFIF संस्करण|2|JFIF का संस्करण|
|घनत्व इकाइयां|1|निम्नलिखित पिक्सेल घनत्व क्षेत्रों के लिए इकाई</br> 00 : कोई इकाई नहीं; चौड़ाई:ऊंचाई पिक्सेल पहलू अनुपात Yघनत्व:Xघनत्व के बराबर है</br> 01 : पिक्सेल प्रति इंच</br> 02 : पिक्सेल प्रति सेंटीमीटर|
|Xघनत्व|2|क्षैतिज पिक्सेल घनत्व शून्य से अधिक|
|Yघनत्व|2|ऊर्ध्वाधर पिक्सेल घनत्व शून्य से अधिक|
|Xthumbnail|1|एम्बेडेड आरजीबी थंबनेल की क्षैतिज पिक्सेल गणना। शून्य हो सकता है |
|थंबनेल|1|एम्बेडेड आरजीबी थंबनेल की लंबवत पिक्सेल गणना। शून्य हो सकता है |
|थंबनेल डेटा|3 × n|असम्पीडित 24 बिट आरजीबी रास्टर थंबनेल डेटा|

### JFIF एक्सटेंशन APP0 मार्कर सेगमेंट ###

यह एक वैकल्पिक खंड है जिसे परिभाषित किए जाने पर तुरंत JFIF APP0 मार्कर खंड का अनुसरण करना चाहिए। यह खंड JFIF संस्करण 1.02 और इसके बाद के संस्करण द्वारा समर्थित है और थंबनेल को तीन अलग-अलग स्वरूपों में एम्बेड करने की अनुमति देता है।

|फ़ील्ड|साइज़ (बाइट्स)|विवरण|
|---|---|---|
|APP0 मार्कर|2|FF E0|
|लंबाई|2|APP0 मार्कर को छोड़कर खंड की लंबाई|
|पहचानकर्ता|5|JFXX (4A 46 58 58 00) ASCII में एक शून्य बाइट द्वारा समाप्त |
|थंबनेल प्रारूप|1|निर्दिष्ट करता है कि निम्नलिखित एम्बेड किए गए थंबनेल के लिए किस डेटा प्रारूप का उपयोग किया जाता है:</br> 10: जेपीईजी प्रारूप</br> 11: 1 बाइट प्रति पिक्सेल पैलेटाइज्ड प्रारूप</br> 13 : 3 बाइट प्रति पिक्सेल आरजीबी प्रारूप |
|थंबनेल डेटा|वैरिएबल||

## जेएफआईएफ का अन्य छवि फ़ाइल स्वरूपों में रूपांतरण

JFIF को [PNG](/hi/image/png/), [JPG](/hi/image/jpg/), और [PDF](/hi/pdf/) जैसे लोकप्रिय इमेज फ़ाइल फ़ॉर्मैट में बदला जा सकता है।

## संदर्भ ##

- [जेएफआईएफ - विकिपीडिया](https://en.wikipedia.org/wiki/JPEG_File_Interchange_Format#History)
