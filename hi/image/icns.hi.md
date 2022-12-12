{
  "date" : "2021-06-29",
  "keywords" :["आईसीएनएस", "एक्सटेंशन", "फाइल", "फॉर्मेट", "इमेज", "एप्पल आइकन इमेज", "मैकओएस", "एप्पल", "आइकन"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"आईसीएनएस - एप्पल आइकॉन इमेज",
  "description":"आईसीएनएस फ़ाइल स्वरूप और एपीआई के बारे में जानें जो आईसीएनएस फाइलें बना और खोल सकते हैं।",
  "linktitle" : "ICNS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-06-29"
}

## आईसीएनएस फाइल क्या है? ##

MacOS प्रोग्राम द्वारा उपयोग किए जाने वाले आइकन प्रारूप को ICNS फ़ाइल कहा जाता है। यह 1-बिट और 8-बिट अल्फा बैंड की अनुमति देता है और आमतौर पर [PNG](/hi/image/png) दस्तावेजों से बने एक या अधिक चित्रों को सहेजता है। MacOS ब्राउज़र और इंटरफ़ेस में प्रोग्राम आइकन ICNS फ़ाइलों का उपयोग करके प्रदर्शित होता है।

स्थान के आधार पर, एक ही शैली के आइकन में कई सेटिंग्स हो सकती हैं। ICNS प्रारूप में कई परिवर्तन हुए हैं और यह उस बिंदु तक विकसित हुआ है जहाँ अब इसे विभिन्न संगत स्वरूपों के आधार के रूप में उपयोग किया जा सकता है। यहाँ कुछ अन्य महत्वपूर्ण बिंदु हैं जिन्हें आपको जानना आवश्यक है:

* IconFamily Resource, Macintosh Icon, Macintosh OS X Icon, Mac OS Icon, Apple Icon, Mac OS X Icon Resource, और Mac OS Icons संसाधन कुछ अन्य नाम हैं।
* आइकन जानकारी के लिए संसाधन शाखा में एक स्रोत का उपयोग किया जाता है।
* ज्यादातर मामलों में, एक फाइल में कई छवियां होती हैं। 1612 पिक्सेल वर्ग और 1024, 512, 256, 128, 48, 32, और 16 पिक्सेल वर्ग समर्थित चित्र आकार हैं।


## ICNS फ़ाइल स्वरूप ##

आईसीएनएस डेटा प्रारूप एक या अधिक छवियों के लिए एक कैप्सूल है, जो 1-बिट बैंड और कई छवि राज्यों का समर्थन करता है।
ऑपरेटिंग सिस्टम आवश्यक प्रदर्शन आकार को फिट करने के लिए आइकन चित्रों का आकार बदल सकता है। बड़े आइकन चित्र आमतौर पर [JPEG](/hi/image/jpeg/) 2000 या [PNG](/hi/image/png) फ़ाइलों के रूप में सहेजे जाते हैं। एक प्रकार की कंप्रेस्ड और असम्पीडित ICNS फाइलें संभव हैं।

एक हेडर और बाइनरी आइकन डेटा एक ICNS फ़ाइल की संरचना बनाते हैं। हेडर में 8 बाइट्स डेटा होता है, जिनमें से चार मैजिक लिटरल हैं और जिनमें से चार फ़ाइल की लंबाई हैं। प्रत्येक आइकन चित्र का प्रकार और आकार आइकन डेटा अनुभाग में संग्रहीत किया जाता है, जिसके बाद बाइनरी छवि डेटा होता है। तस्वीर का आकार बाइनरी सेक्शन के आकार को निर्धारित करता है।

## तकनीकी विशिष्टता ##

### हैडर ###

| ऑफसेट | आकार | उद्देश्य
---|---|---|
|0|4|जादुई शाब्दिक, "आईसीएनएस" होना चाहिए (0x69, 0x63, 0x6e, 0x73)
|4|4|फ़ाइल की लंबाई, बाइट्स में, msb पहले


### चिह्न डेटा ###

| ऑफसेट | आकार | उद्देश्य
---|---|---|
|0|4|आइकन प्रकार
|4|4|डेटा की लंबाई, बाइट्स में (प्रकार और लंबाई सहित), msb पहले
|8|चर|आइकन डेटा

### संपीड़न ###

पिक्सेल डेटा कुछ हद तक संकुचित होता है। 32-बिट ("is32", "il32", "ih32", "it32") और ARGB ("ic04", "ic05") पिक्सल अक्सर पैकबिट्स के समान (प्रति चैनल) संकुचित होते हैं।

|लीड वैल्यू|टेल बाइट्स|परिणाम (असम्पीडित)
---|---|---|
|0 - 127|1 - 128|1 - 128 बाइट्स
|128 - 255|1 बाइट|3 - 130 प्रतियां

## संदर्भ ##

* [आईसीएनएस - विकिपीडिया] (https://en.wikipedia.org/wiki/Apple_Icon_Image_format)
