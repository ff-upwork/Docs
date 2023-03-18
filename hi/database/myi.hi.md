---
date: 2020-11-11
keywords: myi, .myi, myi फ़ाइल स्वरूप, myi फ़ाइलें कैसे खोलें, .myi एक्सटेंशन, myi एक्सटेंशन
लेखक:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: MYI फ़ाइल स्वरूप
linktitle: MYI
description: "MYI फ़ाइल स्वरूप और API के बारे में जानें जो MYI फ़ाइलें बना और खोल सकते हैं।"
menu:
  docs:
    parent: "database"
lastmod: 2020-13-01
---

## एक MYI फ़ाइल क्या है? ##

MYI को MySQL MyISAM इंडेक्स फ़ाइल के रूप में भी जाना जाता है। इसका उपयोग MySQL द्वारा MyISAM तालिका के लिए अनुक्रमणिका को संग्रहीत करने के लिए किया जाता है। MySQL डेटाबेस इंडेक्स तालिका की संरचना को परिभाषित करता है और इसमें तालिकाओं की अखंडता की जांच करने के लिए नियंत्रण तंत्र होता है।

## MYI फ़ाइल स्वरूप ##

MYI फ़ाइल में दो भाग होते हैं, हेडर, और प्रमुख मान।

### MYI हैडर ###

शीर्षलेख में विकल्प, फ़ाइल आकार और कुंजियों के बारे में जानकारी होती है। MySQL में कुंजियाँ एक कमांड के साथ बनाई जाती हैं जैसे

```sql
CREATE [UNIQUE] INDEX.
```

MYI फ़ाइलें पढ़ने और लिखने वाली फ़ाइलें ./myisam निर्देशिका में हैं। इसमें निम्नलिखित फाइलें हैं:

- mi_open.c: इस फाइल में वे रूटीन हैं जो हेडर के प्रत्येक सेक्शन को लिखते हैं।
- mi_create.c: इस फ़ाइल में ऐसे रूटीन हैं जो mi_open.c रूटीन कहते हैं।
- myisamdef.h: इस फ़ाइल में संरचना परिभाषाएँ हैं।

हेडर में निम्नलिखित खंड होते हैं:

- राज्य: राज्य mi_open.c, mi_state_info_write() द्वारा लिखा जाता है। यह संरचना फ़ाइल में एक बार होती है।
- आधार: आधार mi_open.c, mi_base_info_write() द्वारा लिखा गया है। MI_BASE_INFO myisamdef.h में आधार के लिए संबंधित संरचना है। यह संरचना फ़ाइल में एक बार होती है।
- कीडेफ: कीडेफ mi_open.c, mi_keydef_write() द्वारा लिखा जाता है। MI_KEYDEF myisamdef.h में keydef के लिए संबंधित संरचना है। यह एक बहु-घटना संरचना है जो प्रत्येक सूचकांक के लिए प्रकट होती है।
- recinfo: recinfo mi_open.c, mi_recinfo_write() द्वारा लिखा गया है। MI_COLUMNDEF myisamdef.h में recinfo के लिए संगत संरचना है। यह एक बहु घटना संरचना है जो एक कुंजी में दिखाई देने वाले प्रत्येक फ़ील्ड में एक बार दिखाई देती है।

### प्रमुख मान ###

MySQL में पेज को ब्लॉक कहा जाता है। प्रमुख मान ब्लॉक में हैं। एक ब्लॉक में केवल एक इंडेक्स की जानकारी होती है। प्रत्येक कुंजी में सभी स्तंभों की संपूर्ण सामग्री होती है। सामान्य ब्लॉक लंबाई 0x0400 (1024) बाइट्स है। पॉइंटर में निश्चित-पंक्ति तालिकाओं के लिए एक निश्चित आकार (4-बाइट) संख्या होती है जिसमें एक क्रमिक पंक्ति संख्या होती है। यदि कुंजी शून्य है तो बाइट 0x00 है। एक सामान्य ब्लॉक कम से कम 65% भरा होता है और आमतौर पर 80% भरा होता है।

Myisamdef.h फ़ाइल में स्थिरांक में व्यक्त की गई निम्न जानकारी है। चाबियों की अधिकतम संख्या 32 (MI_MAX_KEY) है और एक कुंजी में खंडों की अधिकतम संख्या 16 (MI_MAX_KEY_SEG) है। कुंजी की अधिकतम लंबाई 500 (MI_MAX_KEY_LENGTH) है। ब्लॉक की अधिकतम लंबाई 16384 (MI_MAX_KEY_BLOCK_LENGTH) है।

## संदर्भ ##

- [.MYI फ़ाइल](https://dev.mysql.com/doc/internals/en/the-myi-file.html)
