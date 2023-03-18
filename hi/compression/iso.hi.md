{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"आईएसओ - डिस्क छवि फ़ाइल प्रारूप",
  "description":"एक आईएसओ फाइल और एपीआई क्या है जो आईएसओ फाइलें बना और खोल सकती है।",
  "linktitle" : "ISO",
  "menu" : {
    "docs" : {
     "identifier": "compression-iso",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## एक आईएसओ फाइल क्या है?

.iso एक्सटेंशन वाली फ़ाइल एक असम्पीडित संग्रह डिस्क छवि फ़ाइल है जो सीडी या डीवीडी जैसे ऑप्टिकल डिस्क पर संपूर्ण डेटा की सामग्री का प्रतिनिधित्व करती है। [ISO-9660](https://www.iso.org/standard/17505.html) मानक के आधार पर, ISO छवि फ़ाइल स्वरूप में डिस्क डेटा के साथ-साथ उसमें संग्रहीत फ़ाइल सिस्टम जानकारी शामिल होती है। सामग्री की सटीक प्रतिकृति रखने के लिए आईएसओ फाइलों की क्षमता इसे सीडी/डीवीडी की प्रतियां बनाने के लिए एकदम सही फ़ाइल प्रकार बनाती है और ज्यादातर स्थापना के लिए बूट करने योग्य डेटा को स्टोर करने के लिए उपयोग की जाती है। अधिकांश समय, आईएसओ फाइलें यूएसबी/सीडी/डीवीडी में बूट करने योग्य सामग्री के रूप में संस्थापन के लिए मशीन को बूट करने के लिए जला दी जाती हैं। ISO फाइलों में MIME टाइप एप्लिकेशन/x-iso9660-image होता है।

## आईएसओ फ़ाइल प्रारूप

आईएसओ फ़ाइल प्रारूप अन्य कंटेनर फ़ाइल फ़ाइल स्वरूपों की तरह नहीं है, हालांकि यह डेटा की निर्दिष्ट सामग्री को संग्रहीत करता है। संग्रह सामग्री और फाइल सिस्टम जानकारी की सटीक संरचना के साथ एक बाइनरी फ़ाइल के रूप में बनाया गया है। ISO फ़ाइल स्वरूप का वर्णन [ISO-9660](https://en.wikipedia.org/wiki/ISO_9660) द्वारा निम्नानुसार किया गया है।

### आईएसओ फाइल की शीर्ष स्तरीय संरचना

फ़ाइल की समग्र संरचना में निम्न शामिल हैं:

* `सिस्टम एरिया` - 32,768 बाइट्स और ISO_9660 द्वारा उपयोग नहीं किया जाता है
* `डेटा क्षेत्र` - वॉल्यूम डिस्क्रिप्टर सेट और पथ तालिकाएं, निर्देशिकाएं और फ़ाइलें शामिल हैं

### वॉल्यूम डिस्क्रिप्टर सेट

डेटा क्षेत्र वॉल्यूम डिस्क्रिप्टर सेट के साथ शुरू होता है, एक या अधिक वॉल्यूम डिस्क्रिप्टर का एक सेट वॉल्यूम डिस्क्रिप्टर सेट टर्मिनेटर के साथ समाप्त होता है। ये सामूहिक रूप से डेटा क्षेत्र के लिए हेडर के रूप में कार्य करते हैं, इसकी सामग्री का वर्णन करते हुए (FAT, HPFS और NTFS स्वरूपित डिस्क द्वारा उपयोग किए जाने वाले BIOS पैरामीटर ब्लॉक के समान)।

एक वॉल्यूम डिस्क्रिप्टर सेट नीचे दिखाया गया है।

|वॉल्यूम डिस्क्रिप्टर सेट|
---|
|वॉल्यूम डिस्क्रिप्टर #1|
|...|
|वॉल्यूम डिस्क्रिप्टर #N|
|वॉल्यूम डिस्क्रिप्टर सेट टर्मिनेटर|

#### वॉल्यूम डिस्क्रिप्टर

प्रत्येक वॉल्यूम डिस्क्रिप्टर आकार में 2048 बाइट्स है और इसकी संरचना निम्न है:

|भाग |प्रकार |पहचानकर्ता |संस्करण |डेटा|
---|---|---|---|---|
|आकार |1 बाइट |5 बाइट्स (हमेशा 'सीडी001') |1 बाइट (हमेशा 0x01) |2,041 बाइट्स|

## संदर्भ

* [ऑप्टिकल डिस्क इमेज - विकिपीडिया](https://en.wikipedia.org/wiki/Optical_disc_image)
* [फाइल सिग्नेचर](https://www.garykessler.net/library/file_sigs.html)
* [आईएसओ 9660 - विकिपीडिया](https://en.wikipedia.org/wiki/ISO_9660)
