{
  "date" : "2019-10-11",
  "keywords" :["टीजीए फाइल", "टीजीए फाइल फॉर्मेट", "टीजीए फाइल क्या है", "फाइल", "टीजीए उदाहरण", "टीजीए फाइल एक्सटेंशन", "एक्सटेंशन", "फॉर्मेट"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGA फ़ाइल स्वरूप - एक TARGA ग्राफ़िक छवि फ़ाइल",
  "description":"TGA फ़ाइल स्वरूप और API के बारे में जानें जो TGA फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "TGA",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## टीजीए फाइल क्या है?

.tga एक्सटेंशन वाली फ़ाइल एक रास्टर ग्राफ़िक फ़ॉर्मैट है और इसे Truevision Inc. द्वारा बनाया गया था। इसे TARGA (Truevision Advanced Raster एडेप्टर) बोर्डों के लिए डिज़ाइन किया गया था और IBM-संगत पीसी के लिए हाईकलर/ट्रूकलर डिस्प्ले सपोर्ट प्रदान किया गया था। यह 8, 16, 24 और 32 बिट प्रति पिक्सेल और 8-बिट अल्फा चैनल का समर्थन करता है। यह दोषरहित RLE संपीड़न का भी समर्थन करता है जिसे छवि आकार को कम करने के लिए लागू किया जा सकता है। डिजिटल तस्वीरें और बनावट TGA छवि प्रारूप का उपयोग करते हैं।

## संक्षिप्त इतिहास

TGA फ़ाइल स्वरूप का निर्माण 1984 में AT&T EPICenter (बाद में निकाला गया और Truevision के रूप में ज्ञात एक स्वतंत्र इकाई के रूप में गठित) द्वारा अस्तित्व में आया, जो कलर फ्रेम बफ़र्स के लिए AT&T द्वारा विकसित नई तकनीकों के विपणन पर काम कर रहा था। EPICenter पहले से ही अपने पहले दो कार्डों, VDA (वीडियो डिस्प्ले एडेप्टर) और ICB (इमेज कैप्चर बोर्ड) पर काम कर रहा था, जिसके लिए दो फ़ाइल प्रकारों, .vda और .icb पर काम पहले से ही चल रहा था। इन फ़ाइल स्वरूपों को संहिताबद्ध किया गया था और कम व्यापक विशिष्ट फ़ाइल स्वरूप TGA पेश किया गया था। टीजीए जो पहले से ही उपयोग में था, उसका विस्तार था, और चौड़ाई, ऊंचाई, पिक्सेल गहराई, संबंधित रंग मानचित्र और छवि उत्पत्ति जैसी जानकारी प्रदान करता था।

1989 में प्रकाशित टीजीए के 2.0 संस्करण में कई उन्नत विशेषताएं शामिल हैं जैसे:

* थंबनेल
* अल्फा चैनल
* गामा मूल्य
* शाब्दिक मेटाडाटा

टीजीए के 2.0 संस्करण में प्रमुख योगदानकर्ताओं में ट्रूविजन के शॉन स्टेनर, केविन फिडली और डेविड स्पोलेस्ट्रा शामिल हैं।

## TGA TARGA फ़ाइल स्वरूप निर्दिष्टीकरण

एक TGA फ़ाइल में 2 मुख्य भाग होते हैं:

* शीर्षलेख
* रंग पिक्सेल जानकारी

प्रारूप विनिर्देशों के अनुसार टीजीए फ़ाइल में सभी मान लिट्ल-एंडियन में हैं।

### टीजीए हैडर

एक TGA फाइल हेडर में निम्नलिखित 5 फील्ड होते हैं।

|फ़ील्ड संख्या|लंबाई |फ़ील्ड का नाम |विवरण|
---|---|---|---|
|1| 1 बाइट | आईडी लंबाई | छवि आईडी फ़ील्ड की लंबाई (0-255) |
|2| 1 बाइट | कलर मैप टाइप | क्या एक रंगीन नक्शा शामिल है (0 - इंगित करता है कि इस छवि के साथ कोई रंग-मानचित्र डेटा शामिल नहीं है। 1 - इंगित करता है कि इस छवि के साथ एक रंग-मानचित्र शामिल है।)|
|3| 1 बाइट | छवि प्रकार | संपीड़न और रंग प्रकार (0- कोई छवि डेटा शामिल नहीं है। 1- असम्पीडित, रंगीन मैप की गई छवि, 2- असम्पीडित, सही रंग छवि, 9- रन-लंबाई एन्कोडेड, रंग मैप की गई छवि, 11- रन-लंबाई एन्कोडेड, काली और सफेद छवि )|
|4| 5 बाइट्स | कलर मैप स्पेसिफिकेशन | रंग मानचित्र का वर्णन करता है |
|5| 10 बाइट्स |इमेज स्पेसिफिकेशन| छवि आयाम और प्रारूप |

### इमेज और कलर मैप डेटा

| फील्ड नं. |लंबाई |फ़ील्ड |विवरण|
---|---|---|---|
|6 |छवि आईडी लंबाई क्षेत्र से| इमेज आईडी | पहचान करने वाली जानकारी युक्त वैकल्पिक फ़ील्ड |
|7 |कलर मैप स्पेसिफिकेशंस फील्ड से| कलर मैप डेटा | रंग मानचित्र डेटा वाली लुक-अप तालिका |
|8 |इमेज स्पेसिफिकेशंस फील्ड से| छवि डेटा | इमेज डिस्क्रिप्टर के अनुसार संग्रहित |

### डेवलपर क्षेत्र (वैकल्पिक)

टीजीए संस्करण 2.0 अतिरिक्त संवर्द्धन/अतिरिक्त के लिए समर्थन प्रदान करता है जिसे कई डेवलपर अधिक जानकारी संग्रहीत करना चाहते थे। जानकारी वैकल्पिक है ताकि अगर कोई टीजीए डिकोडर इसकी व्याख्या करने में सक्षम न हो, तो इसे अनदेखा कर दिया जाएगा।

### विस्तार क्षेत्र (वैकल्पिक)

|फील्ड नं.| लम्बाई| फ़ील्ड |विवरण|
---|---|---|---|
|10| 2 बाइट्स | एक्सटेंशन का आकार | विस्तार क्षेत्र के बाइट्स में आकार, हमेशा 495 |
|11| 41 बाइट्स| लेखक का नाम | लेखक का नाम। यदि उपयोग नहीं किया जाता है, तो बाइट्स को NULL (\0) या रिक्त स्थान | पर सेट किया जाना चाहिए
|12| 324 बाइट्स| लेखक टिप्पणी | एक टिप्पणी, चार पंक्तियों के रूप में व्यवस्थित, प्रत्येक में 80 वर्ण और एक NULL| शामिल है
|13| 12 बाइट्स| दिनांक/समय स्टैम्प | वह दिनांक और समय जिस पर चित्र बनाया गया था|
|14| 41 बाइट्स| जॉब आईडी ||
|15| 6 बाइट्स| काम का समय| फ़ाइल बनाने में लगने वाले घंटे, मिनट और सेकंड (बिलिंग आदि के लिए)|
|16| 41 बाइट्स| सॉफ़्टवेयर आईडी | फ़ाइल बनाने वाला एप्लिकेशन.|
|17| 3 बाइट्स| सॉफ्टवेयर संस्करण ||
|18| 4 बाइट्स| मुख्य रंग||
|19| 4 बाइट्स| पिक्सेल पहलू अनुपात ||
|20| 4 बाइट्स| गामा वैल्यू ||
|21| 4 बाइट्स| रंग सुधार ऑफ़सेट | फ़ाइल की शुरुआत से रंग सुधार तालिका में बाइट्स की संख्या यदि मौजूद है |
|22| 4 बाइट्स| डाक टिकट | फ़ाइल की शुरुआत से डाक टिकट छवि तक बाइट्स की संख्या यदि मौजूद है
|23| 4 बाइट्स| स्कैन लाइन ऑफ़सेट | फ़ाइल की शुरुआत से स्कैन लाइनों की तालिका में बाइट्स की संख्या यदि मौजूद है
|24| 1 बाइट| गुण प्रकार | अल्फा चैनल निर्दिष्ट करता है |

### फ़ाइल पादलेख (वैकल्पिक)

फ़ाइल के अंतिम 26 बाइट पादलेख का प्रतिनिधित्व करते हैं, जो यदि मौजूद है तो इसका मतलब है कि इसकी संभावना एक TGA संस्करण 2 फ़ाइल है।

|फील्ड नं.| लम्बाई| क्षेत्र| विवरण|
---|---|---|---|
|28| 4 बाइट्स| एक्सटेंशन ऑफ़सेट| फ़ाइल की शुरुआत से बाइट्स में ऑफ़सेट |
|29| 4 बाइट्स| डेवलपर क्षेत्र ऑफसेट | फ़ाइल की शुरुआत से बाइट्स में ऑफ़सेट |
|30| 16 बाइट्स| हस्ताक्षर| "ट्रूविज़न-XFILE" शामिल है|
|31| 1 बाइट| | शामिल है "."||
|32| 1 बाइट| | इसमें न्यूल| शामिल है


## संदर्भ

* [टीजीए 2.0 फ़ाइल प्रारूप विनिर्देश](https://products.conholdate.app/viewer/view/rVqTeZPLAL/tga-file-format-specifications.pdf?default=view&preview = true.pdf)
* [विकिपीडिया द्वारा टीजीए](https://en.wikipedia.org/wiki/Truevision_TGA)
