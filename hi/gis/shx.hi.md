{
  "date" : "2021-07-29",
  "keywords" :["shx फ़ाइल", "shx फ़ाइल स्वरूप", "shx फ़ाइल क्या है", "फ़ाइल", "shx उदाहरण", "shx फ़ाइल एक्सटेंशन", "एक्सटेंशन", "प्रारूप"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHX - शेपफाइल शेप इंडेक्स फॉर्मेट",
  "description":"SHX फ़ाइल स्वरूप और API के बारे में जानें जो SHX फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "SHX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## एसएचएक्स फाइल क्या है?
SHX फाइल शेप इंडेक्स फॉर्मेट से संबंधित है, जो फीचर ज्योमेट्री का एक पोजिशनल इंडेक्स है, जो आगे और पीछे की ओर तेजी से जाने में सक्षम है। SHX एक डायरेक्ट एक्सेस ऑफ़सेट फ़ाइल है। इस फ़ाइल में कोई डेटा नहीं है, केवल पहले सौ बाइट्स की एक डुप्लिकेट कॉपी, रिकॉर्ड संख्या और उस रिकॉर्ड के शुरुआती बाइट को shp में ऑफसेट करें। कृपया ध्यान दें कि .shx एक्सटेंशन वाली फ़ाइल [SHP](/hi/gis/shp) और [DBF](/hi/database/dbf) से जुड़ी नहीं है।

## SHX फ़ाइल स्वरूप
एसएचएक्स प्रारूप में फीचर ज्योमेट्री का पोजिशनल इंडेक्स और एसएचपी फाइल के समान 100-बाइट हेडर होता है, इसके बाद 8-बाइट फिक्स्ड-लेंथ रिकॉर्ड की कोई भी संख्या होती है जिसमें निम्नलिखित दो फ़ील्ड होते हैं:
| बाइट्स | प्रकार | अंतहीनता | उपयोग |
-------|-------|------------|---------------------------------|
| 0–3 | int32 | बड़ा | रिकॉर्ड ऑफ़सेट (16-बिट शब्दों में) |
| 4-7 | int32 | बड़ा | रिकॉर्ड लंबाई (16-बिट शब्दों में) |

यह इंडेक्स शेपफाइल में पीछे की ओर खोज करना संभव बनाता है, पहले, शेप इंडेक्स में पीछे की ओर खोज कर और फिर रिकॉर्ड ऑफसेट पढ़कर। उस ऑफ़सेट का उपयोग SHP फ़ाइल में सही स्थिति खोजने के लिए किया जा सकता है। आप आगे भी खोज सकते हैं; एक ही विधि का उपयोग कर रिकॉर्ड की मनमानी संख्या। हालाँकि, SHP फ़ाइल के साथ-साथ पूर्ण अनुक्रमणिका उत्पन्न करना संभव है, लेकिन यह SHP फ़ाइल के शीघ्र दूषित होने की संभावना को बढ़ा सकता है।


## संदर्भ

* [शेपफाइल - विकिपीडिया द्वारा)](https://en.wikipedia.org/wiki/Shapefile)

