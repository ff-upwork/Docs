{
  "date" : "2021-04-29",
  "keywords" :[ "amr", ".amr", "file", "extension", "format", "What is an amr file", "music", "amr file format", "amr file", "amr फाइल को कन्वर्ट करें mp3", "amr फ़ाइल चलाएं"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"एएमआर फ़ाइल प्रारूप और एपीआई के बारे में जानें जो एएमआर फाइलें बना, परिवर्तित और खोल सकते हैं।",
  "title" :"एएमआर - अनुकूली बहु-दर कोडेक फ़ाइल",
  "linktitle" : "AMR",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-29"
}

## एएमआर फाइल क्या है?
.amr एक्सटेंशन वाली फ़ाइल **एडेप्टिव मल्टी-रेट** ऑडियो कोडेक के लिए प्रासंगिक ऑडियो डेटा प्रारूप है; एक मल्टी-रेट नैरोबैंड स्पीच कोडेक होता है जो नैरोबैंड सिग्नल को 4.75-12.2 kbit/s बिट रेट पर एन्कोड करता है और टोल क्वालिटी स्पीच 7.4 kbit/s से शुरू होती है; आठ अलग-अलग बिट दरों में से एक का चयन करने के लिए लिंक अनुकूलन का उपयोग करता है।

## एएमआर फ़ाइल प्रारूप
AMR फ़ाइल स्वरूप कई कोडिंग तकनीकों का उपयोग करता है, ACELP (बीजगणितीय कोड उत्साहित रैखिक भविष्यवाणी) एल्गोरिथ्म सबसे अच्छी तकनीक में से एक है; मानव बोले गए ऑडियो को अधिक कुशल तरीके से संपीड़ित करने के लिए डिज़ाइन किया गया। AMR को 1999 में 3GPP द्वारा मानक आवाज या भाषण कोडेक के रूप में सेट किया गया था। AMR फ़ाइल प्रारूप का उपयोग **एडेप्टिव मल्टी-रेट** ऑडियो कोडेक का उपयोग करके बोले गए ऑडियो को संग्रहीत करने के लिए भी किया जाता है, जिसका उपयोग कई स्मार्ट फोन द्वारा रिकॉर्ड किए गए स्टोर करने के लिए किया जाता है। भाषण।

### फ़ाइल स्वरूप संरचना
एएमआर (एडेप्टिव मल्टी-रेट) एक ऑडियो प्रारूप है; विभिन्न मोबाइल एप्लिकेशन और उपकरणों में व्यापक रूप से उपयोग किया जाता है, आमतौर पर ऑडियो प्लेयर / रिकॉर्डर या वीओआईपी प्रकार के अनुप्रयोगों में। एएमआर को आगे वर्गीकृत किया जा सकता है:

1. एएमआर-एनबी (नैरोबैंड)
2. एएमआर-डब्ल्यूबी (वाइडबैंड)

आमतौर पर, एएमआर एएमआर-एनबी को संदर्भित करता है। AMR फ़ाइल स्वरूप में निम्नलिखित संरचना है:

प्रत्येक एएमआर फ़ाइल में एक 6-बाइट हेडर होता है जो फ़ाइल को एएमआर ऑडियो के रूप में पहचानता है। यह हेडर हमेशा इस पर सेट होता है:
- 0x23
- 0x21
- 0x41
- 0x4D
- 0x52
- 0x0A

यह आमतौर पर सभी एएमआर-एनबी फाइलों में सिमियलर होता है। यदि हेडर एक मानक का पालन करता है, तो यह संभावना है कि फ़ाइल दूषित है और इसका उपयोग नहीं किया जाना चाहिए। AMR फ़ाइल में ऑडियो के पैक किए गए फ़्रेमों की एक पूरी संख्या होती है। ये फ्रेम प्रत्येक 20ms ऑडियो की रचना करते हैं। प्रत्येक फ्रेम को किसी भी वैध एएमआर-एनबी मोड (डीटीएक्स मोड में 0-7, 8 एसआईडी) का उपयोग करके एन्कोड किया जा सकता है। चूंकि, फ़्रेम को अलग-अलग बिट दरों पर एन्कोड किया जा सकता है, इसलिए इस विशिष्ट विधि को एडेप्टिव मल्टी-रेट (एएमआर) कहा जाता है।
#### एएमआर मोड
विभिन्न एएमआर मोड और उनके संबंधित बिटरेट निम्नलिखित हैं:

|मोड| बिट दरें|
---|---|
|0| एएमआर 4.75 - 4.75kbit/s पर एनकोड |
|1 | एएमआर 5.15 - 5.15kbit/s पर एन्कोड करता है|
|2 | एएमआर 5.9 - 5.9kbit/s पर एन्कोड करता है|
|3 | एएमआर 6.7 - 6.7kbit/s पर एन्कोड करता है|
|4 | एएमआर 7.4 - 7.4kbit/s पर एन्कोड करता है|
|5 | एएमआर 7.95 - 7.95kbit/s पर एन्कोड करता है|
|6 | एएमआर 10.2 - 10.2kbit/s पर एन्कोड करता है|
|7 | एएमआर 12.2 - 12.2kbit/s पर एन्कोड करता है|

बाइट्स में एएमआर मोड का फ्रेम आकार (हेडर बाइट सहित) नीचे दिया गया है:

|सीएमआर |मोड |फ्रेम साइज(बाइट्स में)|
---|---|---|
|0 |एएमआर 4.75 |13|
|1 |एएमआर 5.15 |14|
|2 |एएमआर 5.9 |16|
|3 |एएमआर 6.7 |18|
|4 |एएमआर 7.4 |20|
|5 |एएमआर 7.95 |21|

## संदर्भ ##

* [अनुकूली बहु-दर ऑडियो कोडेक - विकिपीडिया द्वारा](https://en.wikipedia.org/wiki/Adaptive_Multi-Rate_audio_codec)
* [एएमआर और एएमआर-डब्ल्यूबी ऑडियो कोडेक के लिए आरटीपी पेलोड फॉर्मेट और फाइल स्टोरेज फॉर्मेट](https://tools.ietf.org/html/rfc4867#page-35)

