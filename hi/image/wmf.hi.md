{
  "date" : "2019-10-11",
  "keywords" :["wmf फ़ाइल", "wmf फ़ाइल स्वरूप", "wmf फ़ाइल क्या है", "फ़ाइल", "wmf उदाहरण", "wmf फ़ाइल एक्सटेंशन", "विस्तार", "प्रारूप"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"डब्लूएमएफ - माइक्रोसॉफ्ट विंडोज मेटाफाइल फॉर्मेट",
  "description":"WMF फ़ाइल स्वरूप और API के बारे में जानें जो WMF फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "WMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## डब्लूएमएफ फाइल क्या है?

WMF एक्सटेंशन वाली फाइलें वेक्टर के साथ-साथ बिटमैप-फॉर्मेट इमेज डेटा को स्टोर करने के लिए Microsoft Windows मेटाफाइल (WMF) का प्रतिनिधित्व करती हैं। अधिक सटीक होने के लिए, WMF ग्राफिक्स फ़ाइल स्वरूपों की वेक्टर फ़ाइल स्वरूप श्रेणी से संबंधित है जो डिवाइस स्वतंत्र है। Windows ग्राफ़िकल डिवाइस इंटरफ़ेस (GDI) स्क्रीन पर एक छवि प्रदर्शित करने के लिए WMF फ़ाइल में संग्रहीत फ़ंक्शंस का उपयोग करता है। WMF का एक और उन्नत संस्करण, जिसे एन्हांस्ड मेटा फाइल्स (EMF) के रूप में जाना जाता है, बाद में प्रकाशित किया गया था जो प्रारूप को और अधिक समृद्ध बनाता है। व्यावहारिक रूप से, WMF SVG के समान है।

## WMF फ़ाइल स्वरूप निर्दिष्टीकरण ##

Windows 3.0 के साथ लॉन्च होने के समय एक WMF फ़ाइल को 16-बिट फ़ाइल स्वरूप के रूप में संदर्भित किया जाता है। फ़ाइल प्रारूप में चर-लंबाई के रिकॉर्ड की एक श्रृंखला होती है जिसमें ग्राफिक्स ड्राइंग कमांड, ऑब्जेक्ट परिभाषाएं और गुण होते हैं। चूँकि WMF फाइलें छवि बनाने के लिए GDI को दिए गए आदेशों पर आधारित होती हैं, इसलिए इसे छवि की डिजिटल रिकॉर्डिंग के रूप में भी जाना जाता है जिसे उस छवि को पुन: पेश करने के लिए चलाया जा सकता है। WMF के पूर्ण फ़ाइल प्रारूप विनिर्देश ऑनलाइन उपलब्ध हैं और WMF फ़ाइलों के साथ काम करने के लिए अनुप्रयोगों के विकास के लिए संदर्भित किए जाने चाहिए। WMF फ़ाइल को इसमें व्यवस्थित किया जाता है:

* WMF हैडर रिकॉर्ड
* WMF रिकॉर्ड
* डब्ल्यूएमएफ एंड-ऑफ-फाइल रिकॉर्ड

### WMF हैडर रिकॉर्ड ###

**META_HEADER रिकॉर्ड** में वह जानकारी होती है जो मेटाफ़ाइल की विशेषताओं को परिभाषित करती है, जिसमें शामिल हैं:

* मेटाफाइल का प्रकार
* मेटाफ़ाइल का संस्करण
* मेटाफ़ाइल का आकार
* मेटाफ़ाइल में परिभाषित वस्तुओं की संख्या
* मेटाफ़ाइल में सबसे बड़े एकल रिकॉर्ड का आकार

### WMF प्लेसेबल हैडर रिकॉर्ड ###

**META_PLACEABLE रिकॉर्ड** में छवि से संबंधित विस्तृत जानकारी शामिल है, जिसमें निम्न शामिल हैं:

* एक बाउंडिंग आयत
* स्केलिंग के लिए तार्किक इकाई आकार
* सत्यापन के लिए एक चेकसम

### WMF रिकॉर्ड ###

WMF रिकॉर्ड का एक सामान्य प्रारूप होता है, जो विनिर्देश दस्तावेज़ में निर्दिष्ट होता है। प्रत्येक WMF रिकॉर्ड में निम्न जानकारी होती है:

* रिकॉर्ड आकार
* रिकॉर्ड समारोह
* रिकॉर्ड फ़ंक्शन के लिए पैरामीटर, यदि कोई हो

## संदर्भ ##

* [[MS-WMF]: विंडोज मेटाफाइल फॉर्मेट](https://msdn.microsoft.com/en-us/library/cc250370.aspx)
* [विंडोज मेटाफाइल - विकिपीडिया](https://en.wikipedia.org/wiki/Windows_Metafile)

