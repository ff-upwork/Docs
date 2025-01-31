{
  "date" : "2019-10-11",
  "keywords" :["एमएचटी", "एमएचटी फाइल", "एमएचटी फाइल फॉर्मेट", "एमएचटी फाइल टाइप", "फाइल", "टाइप", "एमएचटी फाइल क्या है"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHT - MIME HTML फ़ाइल स्वरूप",
  "description" :"एमएचटी फाइल बनाने और खोलने के लिए एमएचटी फाइल फॉर्मेट और एपीआई के बारे में जानें।",
  "linktitle" : "MHT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## एमएचटी फाइल क्या है?

.mht एक्सटेंशन वाली फ़ाइल एक MIME सक्षम संग्रह फ़ाइल स्वरूप है जिसमें एक ही फ़ाइल में विभिन्न प्रकार के डेटा होते हैं। यह [css](/hi/web/css/) फाइलों, जावास्क्रिप्ट, और अन्य संसाधनों के रूप में टेक्स्ट, छवियों, पेज स्टाइल जैसे डेटा को एम्बेडेड संसाधनों के रूप में स्टोर कर सकता है। MHT फाइलें, MIME टाइप मैसेज / rfc822 वाली, HTML फाइल की सभी सामग्री को स्टोरेज डिवाइस पर आर्काइव करने के लिए सिंगल आर्काइव फाइल के रूप में इनकैप्सुलेट करती हैं। Microsoft Word जैसे सॉफ़्टवेयर एप्लिकेशन आपको MHT फ़ाइल के रूप में निर्यात करके अपने WORD दस्तावेज़ों को MHT में बदलने देते हैं। MHT फाइलें लोकप्रिय ब्राउज़र जैसे Microsoft इंटरनेट एक्सप्लोर और Google Chrome का उपयोग करके खोली जा सकती हैं।

## एमएचटी फ़ाइल स्वरूप

[MHTML](/hi/web/mhtml/) की तरह, MHT भी समग्र HTML दस्तावेज़ों का एक MIME एनकैप्सुलेशन है। MHT दस्तावेज़ के अंदर दस्तावेज़ सामग्री जैसे इनलाइन चित्र, स्टाइल शीट, एप्लेट आदि MIME-एन्कोडेड हैं जहाँ ये URI के माध्यम से रूट संसाधन से जुड़े होते हैं। ईमेल क्लाइंट जैसे माइक्रोसॉफ्ट आउटलुक ईमेल (आमतौर पर [EML](/hi/email/eml/)) को MHT फाइल फॉर्मेट में स्टोर करता है। MHT फ़ाइल फ़ॉर्मेट के पूर्ण विनिर्देश [RFC 822](https://tools.ietf.org/html/rfc822) में उपलब्ध हैं और इन्हें सॉफ़्टवेयर एप्लिकेशन डेवलपमेंट के लिए संदर्भित किया जा सकता है जो MHT फ़ाइलों को प्रोसेस कर सकता है।

## एमएचटी और एमएचटीएमएल के बीच अंतर

एक ऑनलाइन पृष्ठ को सहेजते समय, उपयोगकर्ता को उस प्रकार के फ़ाइल प्रारूप पर व्यवस्थित करने के लिए कहा जाता है जिसके भीतर मूल प्रणाली पर ऑनलाइन पृष्ठ सहेजा जाना चाहिए। आमतौर पर, उपयोगकर्ता मार्कअप भाषा और MHTML फ़ाइल स्वरूपों के बीच भ्रमित हो जाता है। उन्हें यह देखने में मुश्किल होती है कि इनके बीच फाइल फॉर्मेट बेहतर है।

जब कोई उपयोगकर्ता मार्कअप भाषा के रूप में ऑनलाइन पेज को बर्बाद करने से बचने का फैसला करता है, तो एक फोल्डर बन जाता है, जिसमें पेज की विभिन्न सामग्रियों के लिए कई फाइलें होती हैं यानी टेक्स्ट, ग्राफिक्स, एप्लेट आदि के लिए पूरी तरह से अलग-अलग फाइलें बनाई जाती हैं। एमएचटीएमएल के रूप में ऑनलाइन पेज पूरे ऑनलाइन पेज के लिए एक फाइल बनाता है। ग्राफिक्स, लिंक और वैकल्पिक फाइलों के साथ पृष्ठ के सभी तत्व एक फाइल के अंदर एम्बेडेड क्षेत्र इकाई हैं।

स्वाभाविक रूप से, MHT या MHTML फ़ाइलों को संभालना सीधा है क्योंकि फ़ाइल, जिसे केवल ई-मेल के माध्यम से संरक्षित और साझा किया जा सकता है। हालांकि, मार्कअप लैंग्वेज फाइलें जानकारी के नुकसान की संभावना से कम होती हैं क्योंकि एक भी फाइल के खो जाने या विलोपन से पूरा मार्कअप लैंग्वेज फोल्डर उपयोगकर्ता के लिए अनुपयोगी हो सकता है।

## संदर्भ

* [एमएचटीएमएल - विकिपीडिया](https://en.wikipedia.org/wiki/MHTML)
* [एमएचटी आरएफसी](https://tools.ietf.org/html/rfc822)

