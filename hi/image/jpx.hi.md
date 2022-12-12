{
  "date" : "2021-02-10",
  "keywords" :["जेपीएक्स फाइल", "जेपीएक्स फाइल फॉर्मेट", "जेपीएक्स फाइल क्या है", "फाइल", "जेपीएक्स उदाहरण", "जेपीएक्स फाइल एक्सटेंशन", "एक्सटेंशन", "फॉर्मेट"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"जेपीएक्स - छवि फ़ाइल स्वरूप",
  "description":"JPX फ़ाइल स्वरूप और API के बारे में जानें जो JPX फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "JPX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-10"
}

## जेपीएक्स फाइल क्या है? ##

.Jpx एक्सटेंशन वाली फाइल JPEG 2000 फाइल फॉर्मेट का एक्सटेंशन है। यह मुख्य रूप से जेपीईजी 2000 संपीड़न का उपयोग करता है और एक छवि के लिए कई परतें, विभिन्न रंग रिक्त स्थान, अस्पष्टता और खंडित कोड स्ट्रीम जैसी उन्नत सुविधाएं भी प्रदान करता है। JPX JPEG 2000 कम्प्रेशन के अलावा JBIG, CCITT Group3, CCITT Group4, आदि जैसे अन्य कंप्रेशन की भी अनुमति देता है। JPX फ़ाइल फ़ॉर्मैट को [ISO/IEC 15444-2](https://www.iso.org/standard/33160.html) मानक के तौर पर मंज़ूरी दी गई थी, लेकिन [JPEG के व्यापक इस्तेमाल की वजह से इसे पसंद नहीं किया जा सका ](/hi/छवि/जेपीईजी/) फ़ाइल प्रारूप। जेपीएक्स फाइलें खोलने वाले अनुप्रयोगों में कोरल पेंटशॉप प्रो, एडोब फोटोशॉप 2020, एडोब इलस्ट्रेटर 2020 और कोरलड्रा ग्राफिक्स सूट 2020 शामिल हैं।

## संक्षिप्त इतिहास

2000 में, संयुक्त फोटोग्राफिक विशेषज्ञ समूह समिति ने JP2 को इस नए वेवलेट-आधारित पद्धति के साथ अपने स्वयं के असतत कोसाइन ट्रांसफ़ॉर्म-आधारित JPEG मानक में सुधार करने के उद्देश्य से डिज़ाइन किया। JPEG समिति का लक्ष्य उनके आधारभूत तरीकों को लाइसेंस शुल्क से मुक्त करना था। JP2 लाइसेंस प्राप्त करने वाली 20 कंपनियों के बीच प्रतिस्पर्धा में, वे बहुत कम अंतर से जीते। जेपीईजी 2000 को आईएसओ मानक के रूप में घोषित किया गया है, हालांकि अधिकांश वेब ब्राउज़र 2017 से जेपीईजी 2000 को हाथ देने के लिए तैयार नहीं हैं। 2004 में, आईएसओ/आईईसी 15444-2 प्रारूप को जेपी2 फ़ाइल प्रारूप के विस्तार के रूप में सार्वजनिक रूप से स्वीकार किया गया था।

## जेपीएक्स फ़ाइल प्रारूप

JPX फ़ाइल स्वरूप उन अनुप्रयोगों की आवश्यकताओं को पूरा करने के लिए तैयार किया गया था जिन्हें [JP2](/hi/image/jp2/) फ़ाइल प्रारूप द्वारा परिभाषित कार्यक्षमता से परे डेटा संरचनाओं की आवश्यकता थी। गैर-संगत एक्सटेंशन वाली JP2 फ़ाइल बाज़ार में भ्रम पैदा कर सकती है जहाँ कुछ पाठक कुछ JP2 फ़ाइलों की व्याख्या कर सकते हैं लेकिन अन्य नहीं। जेपीएक्स अनुप्रयोगों में ऐसी समस्याओं से बचने का उत्तर है।

### फ़ाइल पहचान

JPX फ़ाइलें पारंपरिक कंप्यूटर फ़ाइल सिस्टम में संग्रहीत होने पर [JPF](/hi/image/jpf/) के रूप में संग्रहीत की जाती हैं। इसीलिए JPF की तुलना में JPX टर्म का कम से कम इस्तेमाल किया जाता है। एक जेपीएक्स फ़ाइल निम्न बाइट्स से शुरू होती है:

`00 00 00 0c 6a 50 20 20 0d 0a 87 0a ?? ?? ?? ?? 66 74 79 70 6a 70 78 20`

### फ़ाइल संगठन

JP2 के समान, एक JPX फ़ाइल एक बाइनरी संरचना वाले बक्सों का एक संग्रह है जिसमें एक सन्निहित क्रम में बक्सों की व्यवस्था की गई है। पहला बॉक्स फ़ाइल को उसके पहले बाइट के साथ प्रारंभ करता है और अंतिम बॉक्स का अंतिम बाइट फ़ाइल के अंतिम बाइट का प्रतिनिधित्व करता है।
JPX फ़ाइल में एक बॉक्स की बाइनरी संरचना [JP2](/hi/image/jp2/) फ़ाइल प्रारूप में परिभाषित के समान है।

### जेपीएक्स में कोडस्ट्रीम का भंडारण

जेपीएक्स फ़ाइल प्रारूप छवि कोडस्ट्रीम को टुकड़ों में विभाजित करने की अनुमति देता है। यह छवि की एक टाइल को संशोधित करना संभव बनाता है और पूरी फ़ाइल को फिर से लिखे बिना संशोधित टाइल को फ़ाइल के अंत में लिखना संभव बनाता है। मूल [JP2](/hi/image/jp2/) फ़ाइल स्वरूप फ़ाइल के एक निकटस्थ हिस्से में संग्रहीत होने के लिए संपूर्ण कोडस्ट्रीम को प्रतिबंधित करता है, जो छवि संपादन अनुप्रयोगों के लिए समस्याग्रस्त हो सकता है जो छवि की एक टाइल को संशोधित करने और प्राप्त करने की इच्छा रख सकते हैं जेपीएक्स फ़ाइल प्रारूप द्वारा उपरोक्त समर्थन। छवि कोडस्ट्रीम का विखंडन JPX फ़ाइल स्वरूप को JP2 फ़ाइल स्वरूप से बेहतर बनाता है। इसके अलावा, जेपीएक्स फ़ाइल प्रारूप कई कोडस्ट्रीम को संयुक्त करने और प्रदान किए गए परिणाम का उत्पादन करने की अनुमति देता है। कोडस्ट्रीम को कंपोज़िटिंग और एनीमेशन के रूप में जोड़ा जा सकता है।

## संदर्भ ##

* [जेपीईजी 2000 का अवलोकन](https://jpeg.org/jpeg2000)
