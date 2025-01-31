{
  "date" : "2019-10-11",
  "keywords" :["xaml", "xaml फ़ाइल", "xaml फ़ाइल स्वरूप", "xaml फ़ाइल प्रकार", "फ़ाइल", "प्रकार", "एक xaml फ़ाइल क्या है"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"एक्सएएमएल - एक्सएमएल आधारित मार्कअप लैंग्वेज",
  "description":"XAML फ़ाइल स्वरूप और API के बारे में जानें जो XAML फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "XAML ",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## एक एक्सएएमएल फ़ाइल क्या है?

XAML, एक्स्टेंसिबल एप्लिकेशन मार्कअप लैंग्वेज, एक्सटेंशन फाइलें विंडोज प्रेजेंटेशन फाउंडेशन (WPF) पर आधारित सॉफ्टवेयर एप्लिकेशन के लिए यूजर इंटरफेस तत्वों का वर्णन करती हैं। हालांकि एक भाषा, इसे प्रोग्राम करने की आवश्यकता नहीं है क्योंकि यह **[XML](/hi/web/xml/)** के मानक प्रारूप पर आधारित है जिसका उपयोग करना और समझना आसान है। XAML ("ज़मेल" के रूप में उच्चारित) Microsoft द्वारा उपयोगकर्ता इंटरफ़ेस बनाने के विशिष्ट उद्देश्य के साथ विकसित किया गया था। इसका संक्षिप्त नाम एक्सटेंसिबल एवलॉन मार्कअप लैंग्वेज के लिए खड़ा था, जहां एवलॉन डब्ल्यूपीएफ के लिए कोड-नाम था। XAML फ़ाइलें कभी-कभी XOML एक्सटेंशन के साथ भी सहेजी जाती हैं।

## एक्सएएमएल एप्लीकेशन

XAML .NET फ्रेमवर्क 3.0 और .NET फ्रेमवर्क 4.0 तकनीकों जैसे WPF, सिल्वरलाइट, विंडोज वर्कफ्लो फाउंडेशन (WF) और कुछ अन्य में उपयोग का विकल्प है। यूआई तत्वों, डेटा बाइंडिंग, घटनाओं और अन्य सुविधाओं को डब्ल्यूपीएफ में एक्सएएमएल रूपों द्वारा परिभाषित किया गया है। इसी तरह, WF में वर्कफ़्लोज़ को XAML का उपयोग करके परिभाषित किया जा सकता है। XML पर आधारित होने के कारण इसे टूल द्वारा आसानी से संसाधित किया जाता है। चूंकि यह एक घोषणात्मक भाषा है और संकलन की आवश्यकता नहीं है, बहुत सारे उत्पाद उभर रहे हैं जो एक्सएएमएल-आधारित अनुप्रयोगों पर आधारित हैं। XAML में जो कुछ भी बनाया या लागू किया गया है, उसे अधिक पारंपरिक .NET भाषा, जैसे C# या Visual Basic .NET का उपयोग करके व्यक्त किया जा सकता है।

## एक्सएएमएल फ़ाइल स्वरूप

XAML पूरी तरह से XML फॉर्मेट पर आधारित है। [XAML ऑब्जेक्ट मैपिंग](https://download.microsoft.com/download/0/A/6/0A6F7755-9AF5-448B-907D-13985ACCF53E/%5BMS-XAML%5D.pdf) के शुरुआती विनिर्देश इसमें प्रकाशित किए गए थे 2006, इसके बाद दूसरा [संस्करण](https://download.microsoft.com/download/0/A/6/0A6F7755-9AF5-448B-907D-13985ACCF53E/%5BMS-XAML-2009%5D.pdf) प्रकाशित हुआ 2009. ये विनिर्देश दो सार सूचना मॉडल को परिभाषित करते हैं:

* XAML स्कीमा सूचना सेट मॉडल
* XAML सूचना सेट मॉडल

Xaml सूचना सेट (संक्षिप्त में 'Xaml Infoset') उस सूचना की संरचना को परिभाषित करता है जिसे एक Xaml उदाहरण प्रस्तुत कर सकता है। Xaml स्कीमा सूचना सेट विशिष्ट Xaml शब्दावली को परिभाषित करने की अनुमति देता है। यह विनिर्देश XML दस्तावेज़ को Xaml सूचना सेट में बदलने के लिए नियमों के एक सेट को भी परिभाषित करता है। एक्सएमएल, एक्सएमएल के लिए एक सामान्य प्रारूप है। ("Xaml दस्तावेज़" शब्द एक XML दस्तावेज़ को संदर्भित करता है जो एक Xaml सूचना सेट का प्रतिनिधित्व करता है।) लेकिन जब यह विनिर्देश किसी अन्य प्रतिनिधित्व को परिभाषित नहीं करता है, तब तक किसी भी भौतिक प्रतिनिधित्व का उपयोग किया जा सकता है जब तक कि यह Xaml सूचना सेट में जानकारी का प्रतिनिधित्व कर सकता है। .

## संदर्भ

* [XAML - विकिपीडिया द्वारा](https://en.wikipedia.org/wiki/Extensible_Application_Markup_Language)
* [XAML फ़ाइल स्वरूप निर्दिष्टीकरण](https://download.microsoft.com/download/0/A/6/0A6F7755-9AF5-448B-907D-13985ACCF53E/%5BMS-XAML-2009%5D.pdf)

