{
  "date" : "2021-09-06",
  "keywords" :[ "बीटीआर", "एक्सटेंशन", "फ़ाइल", "फ़ाइल प्रारूप", "डेटाबेस फ़ाइल प्रकार", "डेटाबेस फ़ाइल प्रारूप", "डेटाबेस प्राप्त करें"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"बीटीआर फ़ाइल प्रारूप और एपीआई के बारे में जानें जो बीटीआर फाइलें बना और खोल सकते हैं।",
  "title" :"BTR - Btrieve डेटाबेस फ़ाइल",
  "linktitle" : "BTR",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## बीटीआर फाइल क्या है?

.btr एक्सटेंशन वाली फ़ाइल [Btrieve](https://www.actian.com/) ट्रांजेक्शनल डेटाबेस एप्लिकेशन द्वारा बनाई गई एक डेटाबेस फ़ाइल है। रिलेशनल डेटाबेस मैनेजमेंट सिस्टम (RBMS) के विपरीत, Btrieve इंडेक्सेड सीक्वेंशियल एक्सेस मेथड (ISAM) पर आधारित है, जो तेजी से पुनर्प्राप्ति के लिए डेटा संग्रहीत करने का एक तरीका है। BTR फ़ाइल अभिलेखों के संग्रह को संग्रहीत करती है और आवश्यकताओं के अनुसार रिपोर्ट तैयार करने के लिए उपयोग की जाती है। BTR फाइलें Pervasive Btrieve Database Manager, Pervasive PSQL मेंटेनेंस यूटिलिटी और लीजेंड सॉफ्टवेयर BTRIEVE व्यूअर का उपयोग करके खोली जा सकती हैं।

## बीटीआर फ़ाइल संरचना - अधिक जानकारी

बीटीआर फ़ाइल की संरचना में प्रत्येक बाइट की आंतरिक डेटा संरचना और संरेखण सार्वजनिक रूप से उपलब्ध नहीं है। हालाँकि, Btrieve
[Btrieve API] (https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm) प्रदान करता है जिसका उपयोग BTR फ़ाइलों से जानकारी पढ़ने के लिए किया जा सकता है। यह निम्नलिखित प्रोग्रामिंग भाषाओं और विकास परिवेशों के अनुकूल है।

* एम्बरकेडेरो सी / सी ++
* एम्बरकेडेरो डेल्फी
* जीएनयू सी/सी++
* माइक्रो फोकस COBOL
* माइक्रोसॉफ्ट विजुअल बेसिक
* माइक्रोसॉफ्ट विजुअल सी++
* वाटकॉम सी/सी++

किसी BTR फ़ाइल से डेटा पुनर्प्राप्त करना इसके साथ संबद्ध DDF फ़ाइल पर निर्भर है। DDF के बिना, ऐसी फ़ाइल से जानकारी प्राप्त करना आसान नहीं होगा।

## संदर्भ

* [Btrieve - विकिपीडिया](https://en.wikipedia.org/wiki/Btrieve)
* [Btreive API का परिचय](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)
