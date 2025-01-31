{
  "date" : "2021-08-13",
  "keywords" :[ "sdi फ़ाइल", "sdi फ़ाइल स्वरूप", "sdi फ़ाइल क्या है", "फ़ाइल", "sdi उदाहरण", "sdi फ़ाइल एक्सटेंशन", "एक्सटेंशन", "प्रारूप"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"SDI फ़ाइल स्वरूप और API के बारे में जानें जो SDI फ़ाइलें बना और खोल सकते हैं।",
  "title" :"एसडीआई - विंडोज सिस्टम परिनियोजन छवि फ़ाइल",
  "linktitle" : "SDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-13"
}

## एक sdi फ़ाइल क्या है?
.sdi एक्सटेंशन वाली फ़ाइल में लोड ब्लॉब, बूट ब्लॉब और पार्ट ब्लॉब होता है; विंडोज को लोड करने और स्थापित करने के लिए रैम डिस्क या बूट डिस्क बनाने के लिए आमतौर पर विंडोज एंबेडेड स्टूडियो द्वारा उपयोग किया जाता है। SDI को सिस्टम परिनियोजन छवि के लिए संक्षिप्त किया गया है। विंडोज एंबेडेड स्टूडियो एक प्रोग्राम है जिसका उपयोग विंडोज के लिए डिस्क इमेज बनाने के लिए किया जाता है। असल में इस प्रोग्राम में एसडीआई फाइल मैनेजर प्रोग्राम और **sdimgr.exe** नामक एक कमांड लाइन टूल शामिल है, दोनों का उपयोग एसडीआई छवियों को दर्शाने, बनाने और संपादित करने के लिए किया जा सकता है।

## एसडीआई फ़ाइल प्रारूप
सिस्टम को बूट करने के लिए वर्चुअल डिस्क के उपयोग को सक्षम करने के लिए SDI फ़ाइल स्वरूप का व्यापक रूप से उपयोग किया जाता है। माइक्रोसॉफ्ट विंडोज के कुछ संस्करण **रैम बूटिंग** को सक्षम करते हैं, जो एक एसडीआई फाइल को मेमोरी में लोड करने और फिर उससे बूट करने के लिए महत्वपूर्ण है। SDI फ़ाइल स्वरूप भी PXE (प्रीबूट एक्ज़ीक्यूशन एनवायरनमेंट) का उपयोग करके नेटवर्क बूटिंग के लिए स्वयं को सक्षम करता है। इसका उपयोग हार्ड डिस्क इमेजिंग के लिए भी किया जा रहा है।
### एसडीआई फ़ाइल अनुभाग
SDI फ़ाइल को स्वयं निम्न अनुभागों में उप-विभाजित किया जा सकता है:
- **बूट ब्लॉब**: इसमें वास्तविक बूट प्रोग्राम, STARTROM.COM शामिल है। यह हार्ड डिस्क के बूट सेक्टर के समान है।
- **लोड ब्लॉब**: इसमें आम तौर पर एनटीएलडीआर होता है और इसे बूट बीएलओबी द्वारा लॉन्च किया जाता है।
- **पार्ट बीएलओबी**: इसमें वास्तविक बूट रनटाइम होता है; इसमें boot.ini और ntdetect.com फ़ाइलें भी शामिल हैं जो रनटाइम के रूट डायरेक्टरी में स्थित होनी चाहिए।
- **डिस्क बीएलओबी**: यह एमबीआर से शुरू होने वाली फ्लैट एचडीडी छवि है। इसका उपयोग बूटिंग के बजाय हार्ड ड्राइव इमेजिंग के लिए किया जाता है। साथ ही केवल डिस्क BLOB को Microsoft की उपयोगिताओं के साथ माउंट किया जा सकता है।


## संदर्भ

* [सिस्टम परिनियोजन छवि - विकिपीडिया द्वारा](https://en.wikipedia.org/wiki/System_Deployment_Image)


