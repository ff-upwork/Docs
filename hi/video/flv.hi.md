---
date: 2019-10-11
keywords: flv, .flv, flv फ़ाइल स्वरूप, .flv फ़ाइल स्वरूप, .flv एक्सटेंशन, flv एक्सटेंशन, flv वीडियो प्रारूप
लेखक:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "FLV फ़ाइल स्वरूप और API के बारे में जानें जो FLV फ़ाइलें बना और खोल सकते हैं।"
title: FLV फ़ाइल स्वरूप
linktitle: FLV
menu:
  docs:
    parent: "video"
lastmod: 2020-14-12
---

## FLV फ़ाइल क्या है? ##

FLV (फ्लैश वीडियो) .flv एक्सटेंशन के साथ एक कंटेनर फ़ाइल स्वरूप है। FLV का उपयोग Adobe Flash Player या Adobe Air का उपयोग करके इंटरनेट पर ऑडियो/वीडियो सामग्री वितरित करने के लिए किया जाता है। FLV फ़ाइलों में डेटा उसी तरह एन्कोड किया गया है जैसे SWF फ़ाइलें। प्रत्यक्ष समर्थन 2003 में फ्लैश प्लेयर 7 में जोड़ा गया था। Adobe सिस्टम ने FLV के प्रतिबंधों के कारण 2007 में F4V बनाया।

### एन्कोडिंग ###

FLV फ़ाइलों में सोरेनसन स्पार्क के वीडियो बिटस्ट्रीम होते हैं जो H.263 वीडियो मानक के मालिकाना संस्करण हैं। यह फ्लैश प्लेयर 6 और 7 के लिए जरूरी कंप्रेशन फॉर्मेट है। फ्लैश प्लेयर का वर्जन 8 ऑन2 ट्रूमोशन वीपी6 वीडियो बिटस्ट्रीम के लिए सपोर्ट करता है। यह फ्लैश प्लेयर 8 और उच्चतर के लिए अनुशंसित संपीड़न प्रारूप है। FLV MP3, Nellymoser Asao Codec, और ओपन-सोर्स Speex कोडेक में ऑडियो का समर्थन करता है। यह असम्पीडित ऑडियो या ADPCM प्रारूप ऑडियो का भी समर्थन करता है। एएसी (एचई-एएसी/एएसी एसबीआर, एएसी मेन प्रोफाइल और एएसी-एलसी) फ्लैश प्लेयर 9 के नवीनतम संस्करणों द्वारा समर्थित हैं।

## संरचना ##

FLV फ़ाइलों में हैडर और पैकेट होते हैं। एक FLV फाइल हैडर से शुरू होती है। हेडर में निम्नलिखित फ़ील्ड हैं।

- **हस्ताक्षर**: इसका मान FLV है
- **संस्करण**: इसका डिफ़ॉल्ट मान 1 है। केवल 0x01 मान्य है।
- **ध्वज**: 0x04 का उपयोग ऑडियो के लिए किया जाता है और 0x01 का उपयोग वीडियो के लिए किया जाता है, इसलिए 0x05 का उपयोग ऑडियो और वीडियो दोनों के लिए किया जाता है।
- **शीर्षलेख का आकार**: डिफ़ॉल्ट मान 9 है। इसका उपयोग नए विस्तारित शीर्षलेख को छोड़ने के लिए किया जाता है।

हेडर के बाद पैकेट आता है। FLV फ़ाइल को कई पैकेट में विभाजित किया जाता है जिसे FLV टैग कहा जाता है जिसमें 15-बाइट हेडर होते हैं। पैकेट में ऑडियो, वीडियो, स्क्रिप्ट, एन्क्रिप्शन जानकारी और पेलोड के लिए मेटाडेटा होता है। FLV पैकेट में निम्नलिखित क्षेत्र होते हैं।

- **आरक्षित**: यह एफएमएस के लिए आरक्षित है और 0 होना चाहिए।
- **फ़िल्टर**: बताता है कि पैकेट फ़िल्टर किए गए हैं या नहीं।
  - **0**: No preprocessing required. This is used for unencrypted files.
  - **1**: Preprocessing required. This is used for encrypted files
- **पैकेट प्रकार**: यह पैकेट में सामग्री के प्रकार को परिभाषित करता है।
  - **8**: Audio
  - **9**: Video
  - **18**: Script Data
- **डेटा आकार**: यह संदेश की लंबाई दर्शाता है।
- **टाइमस्टैम्प लोअर**: यह टाइमस्टैम्प को मिलीसेकंड में संग्रहीत करता है जिस पर टैग डेटा लागू होता है। यह पहले पैकेट के लिए NULL पर सेट है।
- **टाइमस्टैम्प अपर**: uint32_be मान बनाने के लिए एक्सटेंशन।
- **स्ट्रीम आईडी**: यह पहली स्ट्रीम के लिए NULL पर सेट है।
- **पेलोड डेटा**: यह पैकेट प्रकार पर आधारित डेटा है।

## संदर्भ ##

- [फ्लैश वीडियो - विकिपीडिया](https://en.wikipedia.org/wiki/Flash_Video)
