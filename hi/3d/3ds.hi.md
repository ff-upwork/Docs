{
  "date" : "2019-10-11",
  "keywords" :[ "3DS", "फ़ाइल", "प्रारूप", "फ़ाइल प्रकार", "एक्सटेंशन", "3DS फ़ाइल क्या है?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"3DS फ़ाइल स्वरूप और API के बारे में जानें जो 3DS फ़ाइलें खोल और बना सकते हैं।",
  "title" :"3DS फ़ाइल स्वरूप",
  "linktitle" : "3DS",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## 3DS फ़ाइल क्या है?

.3ds एक्सटेंशन वाली फ़ाइल Autodesk 3D Studio द्वारा उपयोग किए जाने वाले 3D Sudio (DOS) मेश फ़ाइल स्वरूप का प्रतिनिधित्व करती है। Autodesk 3D Studio 1990 के दशक से 3D फ़ाइल स्वरूप बाज़ार में है और अब 3D मॉडलिंग, एनीमेशन और रेंडरिंग के साथ काम करने के लिए 3D Studio MAX में विकसित हो गया है। एक 3DS फ़ाइल में दृश्यों और छवियों के 3D प्रतिनिधित्व के लिए डेटा होता है और यह 3D डेटा आयात और निर्यात के लिए लोकप्रिय फ़ाइल स्वरूपों में से एक है। यह कैमरा लोकेशन, मेश डेटा, लाइटिंग इंफॉर्मेशन, व्यूपोर्ट कॉन्फिगरेशन, स्मूथिंग ग्रुप डेटा, बिटमैप रेफरेंस और एट्रिब्यूट्स जैसी सूचनाओं पर विचार करता है ताकि एक सीन को रेंडर करने के लिए वर्टिस और पॉलीगॉन बनाया जा सके।

## 3DS फ़ाइल स्वरूप - अधिक जानकारी
इसके आधार पर, 3DS एक बाइनरी फ़ाइल स्वरूप है और डेटा के भंडारण और पुनर्प्राप्ति के लिए एक पूर्वनिर्धारित संरचना का अनुसरण करता है। बाइनरी फ़ाइल स्वरूप पाठ-आधारित फ़ाइल स्वरूपों की तुलना में 3DS फ़ाइल स्वरूप को तेज़ी से छोटा करने में सक्षम बनाता है। 3DS फ़ाइल के अंदर डेटा को विखंडू के रूप में संग्रहीत किया जाता है।

### 3DS चंक

3DS फ़ाइल में प्रत्येक खंड डेटा का एक ब्लॉक होता है जिसमें एक आईडी, अगले ब्लॉक के स्थान के लिए ब्लॉक की लंबाई और डेटा ही होता है। चंक आईडी 3DS फ़ाइल स्वरूप पाठकों को उन ब्लॉकों को छोड़ने देता है जिन्हें वे नहीं पहचानते हैं। यह प्रारूप की एक्स्टेंसिबिलिटी में भी मदद करता है। प्रत्येक चंक आकार, प्रकाश और देखने की जानकारी से संबंधित जानकारी संग्रहीत करता है जो एक साथ दृश्य को प्रस्तुत करता है। टुकड़ों को एक 3DS फ़ाइल में एक पदानुक्रमित संरचना में व्यवस्थित किया जाता है और प्रतिनिधित्व में XML दस्तावेज़ ऑब्जेक्ट ट्री जैसा दिखता है।

**चंक आईडी:** चंक के पहले दो बाइट एक चंक पहचानकर्ता का प्रतिनिधित्व करते हैं जो फ़ाइल रीडर को यह तय करने देता है कि इसे पढ़ने के दौरान इस पर विचार करना है या इसे छोड़ना है।

**चंक की लंबाई:** चंक आईडी के बाद 4-बाइट पूर्णांक (छोटे-एंडियन में) होता है जो चंक की लंबाई के लिए होता है। इस लंबाई में डेटा की लंबाई, इसके उप-ब्लॉक की लंबाई और 6-बाइट हेडर भी शामिल हैं।

**पेलोड:** चंक की लंबाई के बाद चंक के लिए डेटा के वास्तविक बाइट्स होते हैं, इसके बाद उसी पदानुक्रमित संरचना में इसके उप-खंड होते हैं जिन्हें कई स्तरों तक गहराई तक बढ़ाया जा सकता है।

### एक हिस्से की संरचना

एक साधारण चंक की पदानुक्रमित संरचना नीचे दी गई है:

**एक हिस्सा**

|प्रारंभ|अंत|आकार|नाम
--- | --- | --- | ---
|0|1|2|चंक आईडी
|2|5|4|अगला हिस्सा

चंक्स पर एक पदानुक्रम लगाया जाता है जिसे इसकी आईडी से पहचाना जाता है। एक 3ds फ़ाइल में प्राथमिक चंक आईडी 4D4Dh है। यह हमेशा फ़ाइल का पहला हिस्सा होता है। साथ में प्राइमरी चंक में मुख्य विखंडू होते हैं।

**मुख्य भाग**

|आईडी|विवरण
--- | ---
|3D3D|ऑब्जेक्ट मेश डेटा की शुरुआत।
|B000|कीफ्रेमर डेटा की शुरुआत।

आईडी ब्लॉक के बाद अगला चंक पॉइंटर अगले मुख्य खंड की ओर इशारा करता है।
एक मुख्य खंड के ठीक बाद एक और हिस्सा है। यह किसी अन्य प्रकार का हिस्सा हो सकता है जो इसके मुख्य भाग के दायरे में स्वीकार्य हो।
मेष विवरण (3D3D) के लिए वे कोई भी गुणक हो सकते हैं।

**3D3D के उपखंड - मेश ब्लॉक**


|आईडी|विवरण
--- | ---
|1100|अज्ञात
|1200|पृष्ठभूमि रंग।
|12201|अज्ञात
|1300|अज्ञात
|1400|अज्ञात
|1420|अज्ञात
|1450|अज्ञात
|1500|अज्ञात
|2100|एम्बिएंट कलर ब्लॉक
|2200|कोहरा?
|2201|कोहरा?
|2210|कोहरा?
|2300|अज्ञात
|3000|अज्ञात
|4000|ऑब्जेक्ट ब्लॉक
|7001|अज्ञात
|एएफएफएफ|अज्ञात

**4000 के उपखंड - वस्तु विवरण ब्लॉक**
Subchunk 4000 का पहला आइटम ऑब्जेक्ट नाम का ASCIIZ स्ट्रिंग है।
याद रखें कि कोई वस्तु जाली, प्रकाश या कैमरा हो सकती है।

|आईडी|विवरण
--- | ---
|4010|अज्ञात
|4012|छाया?
|4100|त्रिकोणीय बहुभुज वस्तु
|4600|लाइट
|4700|कैमरा

## संदर्भ

* [ज्यामिति फ़ाइल प्रारूप - ऑटोडेस्क](https://help.autodesk.com/view/3DSMAX/2015/ENU/?guid=GUID-566E59EE-8221-4AC6-824B-5062C5AE0B32)
* [3डीएस - विकिपीडिया द्वारा](https://en.wikipedia.org/wiki/.3ds)
