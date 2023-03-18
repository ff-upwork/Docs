{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"एमएसजी - माइक्रोसॉफ्ट आउटलुक ईमेल प्रारूप",
  "description":"MSG फ़ाइल स्वरूप और API के बारे में जानें जो MSG फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "MSG",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## एमएसजी फाइल क्या है?

MSG एक फ़ाइल स्वरूप है जिसका उपयोग [Microsoft Outlook](https://products.office.com/en-us/outlook/email-and-calendar-software-microsoft-outlook?rtc#1) और एक्सचेंज द्वारा ईमेल संदेशों को संग्रहीत करने के लिए किया जाता है। , संपर्क, अपॉइंटमेंट, या अन्य कार्य। ऐसे संदेशों में प्रेषक, प्राप्तकर्ता, विषय, दिनांक और संदेश का मुख्य भाग, या संपर्क जानकारी, नियुक्ति विवरण और एक या अधिक कार्य विनिर्देशों के साथ एक या अधिक ईमेल फ़ील्ड हो सकते हैं। वे गुण जो संदेश वस्तु का गठन करते हैं, सहित भी MSG फ़ाइल का एक हिस्सा हैं। MSG फ़ाइल में प्लेन ASCII टेक्स्ट के रूप में हेडर्स, मेन मैसेज बॉडी और हाइपरलिंक्स होते हैं। MSG फ़ाइलें उन प्रोग्रामों के लिए भी उपयुक्त हैं जिन्हें Microsoft के मैसेजिंग एप्लिकेशन प्रोग्रामिंग इंटरफ़ेस (MAPI) की आवश्यकता होती है।

## एमएसजी फ़ाइल संरचना

CFB_3 प्रारूप MSG फ़ाइल का आधार है। प्रतिमान स्टोरेज और स्ट्रीम अवधारणाओं पर आधारित है, जो निर्देशिकाओं और फाइलों के काफी करीब है। इसलिए पूर्व में एक बड़ा अंतर संपूर्ण पदानुक्रम है, जिसे एक विशिष्ट फ़ाइल में पैक किया जाता है, जिसे एक मिश्रित फ़ाइल कहा जाता है। ऑब्जेक्ट संदेश फ़ाइलों का गठन करते हैं और इसमें एक ही संपत्ति या उसके संग्रह शामिल होते हैं। यह क्षमता अनुप्रयोगों को जटिल, संरचित डेटा को एक फ़ाइल में संग्रहीत करने की सुविधा प्रदान करती है। यह प्रारूप कई भंडारणों को भी निर्दिष्ट करता है, प्रत्येक भंडारण संदेश वस्तु को एक प्रमुख घटक के रूप में दर्शाता है। इन स्टोरेज में उस घटक की संपत्ति का प्रतिनिधित्व करने वाली कई धाराएं होती हैं। भंडारण का घोंसला बनाना भी संभव है।

## मैपी गुण

.msg फ़ाइल के शीर्ष स्तर पर, संग्रहण में ऐसी धाराएँ होती हैं जो उनमें गुणों को संग्रहीत करती हैं। गुणों को निम्नानुसार वर्गीकृत किया जा सकता है:

* निश्चित लंबाई गुण
* परिवर्तनीय लंबाई गुण
* बहु-मूल्यवान गुण

श्रेणी के बावजूद, एक संपत्ति या तो एक टैग या नामित है। हालांकि, उनके मानचित्रण भंडारण द्वारा निर्दिष्ट नामित गुणों के लिए उपयुक्त मानचित्रण जानकारी की आवश्यकता होती है।

## भंडार

भंडारण संदेश वस्तु के प्रमुख घटक होते हैं। MSG फ़ाइल स्वरूप निम्न संग्रहण बताता है:

## शीर्ष स्तर की संरचना

संदेश वस्तु MSG फ़ाइल स्वरूप के संपूर्ण शीर्ष स्तर का प्रतिनिधित्व करती है। प्रकार, गुण, प्राप्तकर्ता की संख्या और अटैचमेंट ऑब्जेक्ट के आधार पर, एक संदेश ऑब्जेक्ट में संबंधित .MSG फ़ाइल में अलग-अलग स्ट्रीम स्टोरेज हो सकते हैं।

### अन्य संरचनाओं के साथ संबंध

Msg फ़ाइल स्वरूप में अन्य संरचनाओं के साथ निम्नलिखित संबंध हैं:

* .msg का आधार कंपाउंड फाइल बाइनरी फाइल फॉर्मेट है।
* संदेश और अनुलग्नक ऑब्जेक्ट प्रोटोकॉल द्वारा उपयोग किए जाने वाले गुण इस प्रारूप द्वारा उपयोग किए जाते हैं।

## एमएसजी प्रारूपों से बचने के लिए परिदृश्य

संदेश ऑब्जेक्ट को क्लाइंट या संदेश स्टोर के बीच साझा किया जा सकता है जो .msg फ़ाइल सिस्टम का उपयोग करते हैं। ऐसी कुछ परिस्थितियाँ हैं जिनमें संदेश ऑब्जेक्ट को .msg फ़ाइल स्वरूप में संग्रहीत करना उचित नहीं होगा। उदाहरण के लिए:

* एक बड़े स्टैंडअलोन संग्रह को बनाए रखने के मामले में, एक पूर्ण-विशेषताओं वाले प्रारूप का उपयोग करना बेहतर होता है जिसमें विचारों को अधिक सटीक रूप से प्रस्तुत किया जा सकता है।
* यदि रिसीवर अज्ञात है, तो यह संभव है कि प्रारूप रिसीवर के अंत द्वारा समर्थित नहीं है और निजी या अप्रासंगिक वितरित किया जा सकता है।

## एमएसजी फ़ाइल उदाहरण

MSG फ़ाइल कैसी दिखती है, इसका अंदाजा लगाने के लिए, आप एक [नमूना MSG फ़ाइल](https://products.conholdate.app/viewer/view/mL7cmq6qYbcNG329P/sample-msg-file.msg) डाउनलोड कर सकते हैं और अपने कंप्यूटर इसकी सामग्री को देखने के लिए।

## संदर्भ

* [[एमएस-ओएक्सएमएसजी]: आउटलुक एमएसजी फाइल फॉर्मेट](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)
