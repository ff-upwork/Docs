{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"आरएमएल - अमृत रिपोर्ट टेम्पलेट फ़ाइल",
  "description":"RML फ़ाइल और API के बारे में जानें जो RML फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "RML",
  "menu" : {
    "docs" : {
      "identifier":"misc-rml",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## आरएमएल फाइल क्या है?

आरएमएल फ़ाइल [एलिक्सिर रिपरटॉयर](https://elixirtech.com/repertoire-2/) रिपोर्टिंग इंजन के साथ एक रिपोर्टिंग टेम्प्लेट फ़ाइल होती है। टेम्प्लेट फ़ाइल का उपयोग एलिक्जिर फ़ाइलसिस्टम से जुड़े डेटा स्रोत के साथ रिपोर्ट उत्पन्न करने के लिए किया जाता है। डेटा को RML टेम्प्लेट फ़ाइल में पढ़ा और भरा जाता है और [PDF](/hi/pdf/), [RTF](/hi/word-processing/rtf/), और स्प्रेडशीट [XLS] जैसे कई अलग-अलग फ़ाइल स्वरूपों में निर्यात किया जा सकता है। (/hi/spreadsheet/xls/)। Elixir Repertoire रिपोर्टिंग इंजन को JDBC डेटा स्रोतों की एक विस्तृत विविधता से जोड़ा जा सकता है।

## आरएमएल फ़ाइल स्वरूप

RML फ़ाइल स्वरूप की आंतरिक फ़ाइल संरचना विवरण सार्वजनिक रूप से उपलब्ध नहीं हैं। कनेक्टेड डेटा स्रोतों से पॉप्युलेट किए गए डेटा के साथ रिपोर्ट उत्पन्न करने के लिए एलिक्सिर रिपर्टोयर एप्लिकेशन द्वारा आंतरिक रूप से फाइलें उत्पन्न और सहेजी जाती हैं। RML टेम्प्लेट फ़ाइल में डेटा से उत्पन्न होने वाली अंतिम रिपोर्ट के समग्र लेआउट और प्लेसहोल्डर्स की जानकारी होती है।

## आरएमएल टेम्पलेट फ़ाइल कैसे करें?

एलिक्सिर प्रदर्शनों की सूची में आरएमएल टेम्पलेट उत्पन्न करने के लिए, निम्नलिखित चरणों का पालन किया जा सकता है।

1. JDBC डेटा स्रोत को फ़ाइल सिस्टम से कनेक्ट करें।
1. रिपोर्ट टेम्पलेट विज़ार्ड लॉन्च करें
1. डेटा स्रोत .ds फ़ाइल का पता लगाने के लिए सॉफ़्टवेयर का उपयोग करें
1. निर्यात के विकल्प के रूप में सारणीबद्ध रिपोर्ट चुनें
1. रिपोर्ट टेम्प्लेट में शामिल करने के लिए फ़ील्ड चुनें
1. अंत में, फिनिश बटन पर क्लिक करने पर, पहले रिपॉजिटरी में रिपोर्ट.आरएमएल जोड़ा जाता है और लेआउट टैब दिखाने के लिए खोला जाता है।

## संदर्भ

* [अमृत प्रदर्शनों की सूची](https://elixirtech.com/repertoire-2/)

