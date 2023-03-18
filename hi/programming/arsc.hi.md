{
  "date" : "2019-10-11",
  "keywords" :[ "एआरएससी", ".एआरएससी", "एआरएससी फाइल क्या है", "एआरएससी फाइल कैसे खोलें", "एक्सटेंशन", "फाइल", "एआरएससी फाइल", "एआरएससी फाइल फॉर्मेट", "एआरएससी फाइल एक्सटेंशन" ,"arsc फ़ाइल उदाहरण"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"एआरएससी - एंड्रॉइड पैकेज रिसोर्स टेबल फाइल",
  "description":"एआरएससी फ़ाइल प्रारूप और एपीआई के बारे में जानें जो एआरएससी फ़ाइल बना और खोल सकते हैं।",
  "linktitle" : "ARSC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-22"
}

## एआरएससी फाइल क्या है?

एक ARSC फ़ाइल एक Android संसाधन तालिका फ़ाइल है जिसमें तालिका-प्रारूप में संसाधनों की एप्लिकेशन की सूची होती है। इसमें संसाधन नाम, गुण और आईडी जैसी जानकारी शामिल है। ARSC फाइलें एपीके पैकेज का हिस्सा हैं जिनका उपयोग इन Android ऐप्स को इंस्टॉल करने के लिए किया जाता है। एपीके फ़ाइल उत्पन्न होने पर एंड्रॉइड एप्लिकेशन में सभी संसाधन जैसे छवियां, लेआउट, शैलियों और स्ट्रिंग्स को बाइनरी फाइलों में परिवर्तित कर दिया जाता है। एआरएससी फ़ाइल भी उसी पर उत्पन्न होती है, जिसमें प्रोग्राम के सभी संकलित संसाधनों और उनकी आईडी की सूची होती है।

## एआरएससी फ़ाइल स्वरूप

.arsc एक्सटेंशन फाइलें कंपाइलर के बाद उत्पन्न बाइनरी फाइलें हैं, जैसे एएनटी (एक्लिप्स) या ग्रैडल (एएस), एंड्रॉइड एप्लिकेशन कोड को [एपीके](/hi/संपीड़न/एपीके/) फ़ाइल बनाने के लिए संकलित करता है। आप इसकी सामग्री को देखने के लिए WinZip जैसी किसी भी संग्रह उपयोगिता का उपयोग करके एपीके फ़ाइल को निकाल सकते हैं, जो कि संकलित जावा क्लास फ़ाइलें हैं, अर्थात क्लास.डेक्स। इनके अतिरिक्त, इसमें यह एआरएससी फ़ाइल भी शामिल है जिसमें इसके बारे में मेटा-सूचना शामिल है:

* एक्सएमएल नोड्स
* गुण
* संसाधन आईडी

एपीके फ़ाइल में संसाधनों को संसाधन आईडी द्वारा संदर्भित किया जाता है, जबकि विशेषताओं को रनटाइम पर एक मान में हल किया जाता है। Android aapt टूल बिल्ड के समय फ़ाइल में परिभाषित सभी संसाधनों को एकत्र करता है और उन्हें संसाधन आईडी प्रदान करता है। संकलित संसाधनों को पहचानकर्ता निर्दिष्ट किए जाने के बाद, एक R.java फ़ाइल स्रोत कोड के साथ-साथ Resources.arsc से उत्पन्न होती है।

## संदर्भ

* [द्विआधारी संसाधन तालिका संरचना](https://stackoverflow.com/questions/27548810/android-compiled-resources-resources-arsc)
