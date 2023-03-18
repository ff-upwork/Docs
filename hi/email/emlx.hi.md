{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ईएमएलएक्स - ऐप्पल मेल फ़ाइल प्रारूप",
  "description":"ईएमएलएक्स फ़ाइल प्रारूप और एपीआई के बारे में जानें जो ईएमएलएक्स फाइलें बना और खोल सकते हैं।",
  "linktitle" : "EMLX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## ईएमएलएक्स फ़ाइल क्या है?

EMLX फ़ाइल स्वरूप Apple द्वारा कार्यान्वित और विकसित किया गया है। Apple मेल एप्लिकेशन ईमेल निर्यात करने के लिए EMLX फ़ाइल स्वरूप का उपयोग करता है। ऐसे अन्य अनुप्रयोग भी हैं जो EMLX फ़ाइलें खोल सकते हैं और इन्हें अन्य फ़ाइल स्वरूपों में परिवर्तित कर सकते हैं।

## EMLX फ़ाइल स्वरूप का संक्षिप्त इतिहास

मैक ओएस एक्स ऑपरेटिंग सिस्टम ने नेक्स्ट द्वारा बनाए गए मौजूदा ईमेल प्रोग्राम, नेक्स्टमेल को नेक्स्टस्टेप ऑपरेटिंग सिस्टम के हिस्से के रूप में अपनाया। नेक्स्ट का अधिग्रहण करने के बाद ऐप्पल ने अपनी सुविधाओं का उत्थान किया और यह अब डिफ़ॉल्ट मेल क्लाइंट के रूप में इस्तेमाल होने वाला ऐप्पल मेल ईमेल एप्लिकेशन बन गया। Apple मेल के माध्यम से निर्यात किए गए ईमेल सीधे EMLX फ़ाइलों के रूप में सहेजे जाते हैं। इसके अलावा, यह EMLX फ़ाइलों के लिए डिफ़ॉल्ट मेल क्लाइंट है जब कोई मैक ओएस पर डबल-क्लिक करके इन्हें खोलता है।

## ईएमएलएक्स फ़ाइल प्रारूप

ईएमएलएक्स फाइलें साधारण टेक्स्ट आधारित फाइलें हैं जिन्हें नोटपैड जैसे किसी भी टेक्स्ट एडिटर में खोला जा सकता है। EMLX फ़ाइल संरचना में तीन भाग होते हैं:

* संदेश के लिए एक बाइट गिनती - संदेश की लंबाई, ASCII में दशमलव में लिखा गया, 0x0a द्वारा समाप्त किया गया
*संदेश ही
* संदेश मेटाडेटा एक्सएमएल प्लिस्ट के रूप में

ऐप्पल मेल से ईएमएलएक्स के रूप में निकाले गए नमूना ईमेल और टेक्स्ट एडिटर में खोलने की मदद से इन्हें बेहतर ढंग से समझाया जा सकता है।

### ईएमएलएक्स उदाहरण

```
875       
X-Spam-Checker-Version: SpamAssassin 3.3.2 (2011-06-06) on ******.*********.***
X-Spam-Level:
X-Spam-Status: No, score#-3.2 required#4.2 tests#BAYES_00,RP_MATCHES_RCVD,
        SPF_PASS,TVD_SPACE_RATIO autolearn#ham version#3.3.2
Received: from [127.0.0.1](******.*********.*** [***.**.**.**])
        by ******.*********.*** (8.14.5/8.14.5) with ESMTP id r2TN8m4U099571
        for <****@*********.***>; Fri, 29 Mar 2013 19:08:48 -0400 (EDT)
        (envelope-from ****@*********.***)
Subject: very simple
From: Sender <****@*********.***>
Content-Type: text/plain; charset#us-ascii
Message-Id: <4E83618E-BB56-404F-8595-87352648ADC7@*********.***>
Date: Fri, 29 Mar 2013 19:09:06 -0400
To: Reciever <****@*********.***>
Content-Transfer-Encoding: 7bit
Mime-Version: 1.0 (Apple Message framework v1283)
X-Mailer: Apple Mail (2.1283)

message Foo
--
Sender
http://www.la-grange.net/karl/

<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version#"1.0">
<dict>
        <key>date-sent</key>
        <real>1364598546</real>
        <key>flags</key>
        <integer>8590195713</integer>
        <key>original-mailbox</key>
        <string>imap://********@127.0.0.1:11143/mail/2013/03</string>
        <key>remote-id</key>
        <string>41147</string>
        <key>subject</key>
        <string>very simple</string>
</dict>
</plist>
```

इस उदाहरण में, 875 संदेश की कुल लंबाई दिखाता है। संदेश मेटाडेटा में संलग्न है<plist> टैग और झंडे निम्नानुसार वर्णित हैं:

|फ़ील्ड|विवरण|मूल्य
---|---|---|
|0|पढ़ें|1 << 0
|1|हटाया गया|1 << 1
|2|उत्तर दिया|1 << 2
|3|एन्क्रिप्टेड|1 << 3
|4|ध्वजांकित|1 << 4
|5|हालिया|1 << 5
|6|ड्राफ्ट|1 << 6
|7|प्रारंभिक (अब उपयोग नहीं किया गया)|1 << 7
|8|अग्रेषित|1 << 8
|9|पुनर्निर्देशित|1 << 9
|10-15|अटैचमेंट काउंट|3F << 10 (6 बिट)
|16-22|प्राथमिकता स्तर|7F << 16 (7 बिट)
|23|हस्ताक्षरित|1 << 23
|24|जंक है|1 << 24
|25|जंक नहीं है|1 << 25
|26-28|फ़ॉन्ट आकार डेल्टा|7 << 26 (3 बिट)
|29|जंक मेल स्तर रिकॉर्ड किया गया|1 << 29
|30|टोक में टेक्स्ट हाइलाइट करें|1 << 30
|31|(अप्रयुक्त)|

## यह सभी देखें ##

* [ईएमएल](/hi/ ईमेल/ईएमएल/)
* [एमएसजी](/hi/ ईमेल/संदेश/)
