{
  "date" : "2022-07-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"INC फाइल एक्सटेंशन - INC फाइल क्या है?",
  "description":"INC के बारे में जानें फ़ाइल स्वरूप और API शामिल करें जो INC फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "INC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-07-14"
}

## आईएनसी फाइल क्या है?

एक INC फ़ाइल एक सम्मिलित फ़ाइल है जिसका उपयोग सॉफ़्टवेयर प्रोग्राम के स्रोत कोड द्वारा हेडर सूचना को संदर्भित करने के लिए किया जाता है। यह [.h फ़ाइल स्वरूप](/hi/programming/h/) के समान है और इसमें घोषणाएं, फ़ंक्शन, हेडर या मैक्रोज़ शामिल हैं जिन्हें C++ जैसी स्रोत कोड फ़ाइलों द्वारा पुन: उपयोग किया जा सकता है। C, [C++](/hi/programming/cpp/), Pascal, [PHP](/hi/programming/php/), और [Java](/hi/programming/java/) जैसी विभिन्न प्रोग्रामिंग भाषाओं द्वारा INC फ़ाइलों का उपयोग किया जाता है। माइक्रोसॉफ्ट नोटपैड, नोटपैड++, और टेक्स्टएडिट जैसे पाठ संपादकों का उपयोग आईएनसी फाइलें खोलने के लिए किया जा सकता है।

## INC फ़ाइल स्वरूप - अधिक जानकारी

घोषणा सिंटैक्स के अनुसार शामिल सभी घोषणाओं के साथ एक INC फ़ाइल सादे पाठ फ़ाइल के रूप में सहेजी जाती है। एक INC फ़ाइल अन्य INC फ़ाइलों को भी संदर्भित कर सकती है। एक बार बन जाने के बाद, INC फ़ाइल प्रोजेक्ट का हिस्सा बन जाती है और इसे C++ जैसी स्रोत फ़ाइलों से संदर्भित किया जा सकता है। किसी भी दोहराव से बचने के लिए इसे कई स्रोत फ़ाइलों द्वारा संदर्भित किया जा सकता है।

## आईएनसी फ़ाइल सामग्री

आईएनसी फाइलों में निम्नलिखित जानकारी शामिल हो सकती है।

**`Variables`** - ऑब्जेक्ट ओरिएंटेड प्रोग्रामिंग (OOP) के मामले में, एक क्लास हेडर फ़ाइल में सभी क्लास लेवल वेरिएबल्स की परिभाषाएँ होती हैं जो कार्यान्वयन स्रोत कोड फ़ाइलों में पहुँच योग्य होती हैं

**`मेथड्स डिक्लेरेशन`** - सभी मेथड्स डिक्लेरेशन को .h हेडर फाइल्स में शामिल किया जाता है ताकि मल्टीपल इम्प्लीमेंटेशन फाइल्स में एक्सेस किया जा सके।

**`गैर-इनलाइन फ़ंक्शन परिभाषाएं`** - हेडर फ़ाइलों में गैर-इनलाइन विधियों की परिभाषाएं भी हो सकती हैं।

## PHP में INC फ़ाइल का उपयोग करने का नुकसान

PHP सर्वर साइड स्क्रिप्ट हैं जो सर्वर पर चलती हैं और कॉलिंग वेबपेजों पर परिणाम लौटाती हैं। यदि एक PHP फ़ाइल एक INC फ़ाइल को संदर्भित कर रही है और सर्वर .inc फ़ाइलों को पार्स करने के लिए कॉन्फ़िगर नहीं किया गया है (जो कि बहुत सामान्य है), एक उपयोगकर्ता URL निर्देशिका पर जाकर .inc फ़ाइल में php स्रोत कोड देख सकता है। इसलिए, INC फ़ाइलों का उपयोग करते समय सावधान रहना चाहिए क्योंकि PHP में फ़ाइलें शामिल हैं।

## संदर्भ

* [PHP में INC का उपयोग करना](https://stackoverflow.com/questions/7129842/what-is-an-inc-and-why-use-it)

