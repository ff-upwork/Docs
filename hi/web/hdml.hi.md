{
  "date" : "2021-08-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"हैंडहेल्ड डिवाइस मार्कअप लैंग्वेज फ़ाइल",
  "description":"HDML फ़ाइल स्वरूप और API के बारे में जानें जो HDML फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "HDML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-21"
}

## एचडीएमएल फ़ाइल क्या है?

.Hdml (हैंडहेल्ड डिवाइस मार्कअप लैंग्वेज) एक्सटेंशन वाली फाइल पोर्टेबल इलेक्ट्रॉनिक उपकरणों जैसे हैंडहेल्ड कंप्यूटर, स्मार्टफोन और सूचना प्रदर्शन उपकरणों के लिए वेब पेज बनाने के लिए एक मार्कअप भाषा है। HDML को [SGML](https://en.wikipedia.org/wiki/Standard_Generalized_Markup_Language) भाषा का विस्तार कहा जाता है। एचडीएमएल एचटीएमएल के समान है, लेकिन वायरलेस और हैंडहेल्ड डिवाइस के लिए जिसमें पीडीए, मोबाइल फोन आदि जैसे छोटे डिस्प्ले हैं। इसे WML से बदल दिया गया जिसके लिए इसने एक महत्वपूर्ण प्रभाव के रूप में काम किया।

## एचडीएमएल फ़ाइल स्वरूप - अधिक जानकारी

एचडीएमएल हैंडहेल्ड उपकरणों के लिए एक मार्कअप भाषा है जो एचटीएमएल के समान मार्कअप टैग पर आधारित है। HDML को मानकीकरण के लिए W3C को प्रस्तुत किया गया था लेकिन यह कभी भी मानक नहीं बना। हालाँकि, इसके फ़ाइल प्रारूप विनिर्देश संदर्भ के लिए [W3 वेबसाइट](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) पर उपलब्ध हैं। [HDML भाषा के लिए सिंटैक्स](https://www.w3.org/TR/hdml20-5.html#HEADING5-0) डेवलपर के संदर्भ के लिए उपलब्ध है और इसका उपयोग नमूना अनुप्रयोग विकास के लिए किया जा सकता है।

## एचडीएमएल तत्व

निम्नलिखित तत्वों का एक समूह है जो एचडीएमएल के लिए रन-टाइम वातावरण प्रदान करता है और इसे उपयोगकर्ता एजेंट के रूप में संदर्भित किया जाता है।

|तत्व|विवरण|
---|---|
|कार्ड्स|यह एचडीएमएल का मूलभूत बिल्डिंग ब्लॉक है, और प्रदर्शित करता है और उपयोगकर्ता को जानकारी के कार्ड के साथ बातचीत करने की अनुमति देता है। |
| डेक | एचडीएमएल कार्ड एक साथ डेक में समूहित होते हैं। एक एचडीएमएल डेक एक एचटीएमएल पेज के समान है जिसमें इसे यूआरएल [आरएफसी1738] द्वारा पहचाना जाता है और एक सर्वर से अनुरोधित सामग्री की इकाई है और उपयोगकर्ता एजेंट द्वारा कैश किया जाता है।
|क्रियाएँ|क्रियाएँ PREV, SOFT1-SOFT8, और HELP प्रकार की हो सकती हैं। ये सार हैं और उपयोगकर्ता एजेंट विशिष्ट तरीके से उपयोगकर्ता इंटरफ़ेस में समर्थित हैं
| क्रियाएँ | एक गतिविधि संबंधित कार्डों के समूह की तरह होती है जो एक तार्किक कार्य करते हैं। ये एक या एक से अधिक डेक फैला सकते हैं। एचडीएमएल नेविगेशन और राज्य मॉडल गतिविधियों के आसपास संरचित है
|इतिहास-आधारित नेविगेशन|उपयोगकर्ता एजेंट उपयोगकर्ता को प्रदर्शित किए जाने वाले कार्डों का इतिहास रखता है। एक्सेस किए गए प्रत्येक कार्ड को कार्ड इतिहास में जोड़ा जाता है। उपयोगकर्ता एजेंट उपयोगकर्ता को इतिहास में पिछले कार्ड पर आसानी से नेविगेट करने की अनुमति देता है

## संदर्भ

* [एचडीएमएल - विकिपीडिया](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)
* [HDML विशिष्टताएं - W3 स्कूल](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)
