{
  "date" : "2022-10-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"एचडीएम फाइल - हैंडहेल्ड डिवाइस मार्कअप लैंग्वेज फाइल",
  "description":"HDM फ़ाइल स्वरूप और API के बारे में जानें जो HDM फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "HDM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-10-12"
}

## एचडीएम फाइल क्या है?

HDM फाइल एक मार्कअप लैंग्वेज वेबपेज फाइल है जो हैंडहेल्ड डिवाइस मार्कअप लैंग्वेज (HDML) में बनाई गई है। इसमें [HTML](/hi/web/html/) भाषा के समान मार्कअप टैग शामिल हैं, लेकिन इसे स्मार्टफोन और पीडीए जैसे हैंडहेल्ड इलेक्ट्रॉनिक उपकरणों के लिए डिज़ाइन किया गया है। [HDML फ़ाइल प्रारूप विनिर्देश](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) मानकीकरण के लिए W3C को सबमिट किए गए थे लेकिन मानक नहीं बन सके। HDM W3 वेबसाइट पर उपलब्ध [HDML](/hi/web/hdml/) फ़ाइल प्रारूप विनिर्देशों पर आधारित है।

## HDM फ़ाइल स्वरूप - अधिक जानकारी

एचडीएम फ़ाइल में मार्कअप टैग होते हैं जो हैंडहेल्ड डिवाइस पर दृष्टिगत रूप से डिज़ाइन की गई वेबसाइट पर प्रस्तुत किए जाते हैं। HDM फ़ाइलों को HTML पेजों के लिए उपयोग किए जाने वाले HTTP प्रोटोकॉल के बजाय HDTP (हैंडहेल्ड डिवाइस ट्रांसपोर्ट प्रोटोकॉल) प्रोटोकॉल का उपयोग करने वाले उपकरणों में कॉपी किया जाता है।

## एचडीएमएल फ़ाइल तत्व

निम्नलिखित तत्वों का एक समूह है जो एचडीएमएल के लिए रन-टाइम वातावरण प्रदान करता है और इसे उपयोगकर्ता एजेंट के रूप में संदर्भित किया जाता है।

|तत्व|विवरण|
---|---|
|कार्ड्स|यह एचडीएमएल का मूलभूत बिल्डिंग ब्लॉक है, और प्रदर्शित करता है और उपयोगकर्ता को जानकारी के कार्ड के साथ बातचीत करने की अनुमति देता है। |
| डेक | एचडीएमएल कार्ड एक साथ डेक में समूहित होते हैं। एक एचडीएमएल डेक एक एचटीएमएल पेज के समान है जिसमें इसे यूआरएल [आरएफसी1738] द्वारा पहचाना जाता है और यह एक सर्वर से अनुरोधित सामग्री की इकाई है और उपयोगकर्ता एजेंट द्वारा कैश की जाती है।
|क्रियाएँ|क्रियाएँ PREV, SOFT1-SOFT8, और HELP प्रकार की हो सकती हैं। ये सार हैं और उपयोगकर्ता एजेंट विशिष्ट तरीके से उपयोगकर्ता इंटरफ़ेस में समर्थित हैं
| क्रियाएँ | एक गतिविधि संबंधित कार्डों के समूह की तरह होती है जो एक तार्किक कार्य करते हैं। ये एक या एक से अधिक डेक फैला सकते हैं। एचडीएमएल नेविगेशन और राज्य मॉडल गतिविधियों के आसपास संरचित है
|इतिहास-आधारित नेविगेशन|उपयोगकर्ता एजेंट उपयोगकर्ता को प्रदर्शित किए जाने वाले कार्डों का इतिहास रखता है। एक्सेस किए गए प्रत्येक कार्ड को कार्ड इतिहास में जोड़ा जाता है। उपयोगकर्ता एजेंट उपयोगकर्ता को इतिहास में पिछले कार्ड पर आसानी से नेविगेट करने की अनुमति देता है

## संदर्भ

* [एचडीएमएल - विकिपीडिया](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)
* [HDML विशिष्टताएं - W3 स्कूल](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)

