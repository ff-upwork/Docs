{
  "date" : "2021-08-11",
  "keywords" :[ "वीडीआई फाइल", "वीडीआई फाइल फॉर्मेट", "व्हाट इज ए वीडीआई फाइल", "फाइल", "वीडीआई उदाहरण", "वीडीआई फाइल एक्सटेंशन", "एक्सटेंशन", "फॉर्मेट"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"VDI फ़ाइल स्वरूप और API के बारे में जानें जो VDI फ़ाइलें बना और खोल सकते हैं।",
  "title" :"वीडीआई - वर्चुअलबॉक्स वर्चुअल डिस्क छवि फ़ाइल",
  "linktitle" : "VDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## वीडीआई फाइल क्या है?
.vdi एक्सटेंशन वाली फाइल एक वर्चुअल डिस्क इमेज होती है; Oracle के ओपन सोर्स डेस्कटॉप वर्चुअलाइजेशन प्रोग्राम के लिए विशिष्ट है जिसे VirtualBox कहा जाता है। VDI फ़ाइलें VirtualBox वर्चुअल मशीन को प्रारंभ करने के लिए उपयोग की जाती हैं। VMs उपयोगकर्ताओं को एक ही कंप्यूटर पर अतिरिक्त ऑपरेटिंग सिस्टम या प्रोग्राम चलाने की अनुमति देते हैं। इसलिए, VDI फ़ाइलों का लाभ यह है कि उपयोगकर्ता इन डिस्क छवि फ़ाइलों को अपनी हार्ड डिस्क पर सहेज सकते हैं और जब भी उन्हें आवश्यकता हो, एमुलेटर का उपयोग करके इन्हें चला सकते हैं।

## वीडीआई फ़ाइल प्रारूप
वर्चुअल डिस्क इमेज (VDI) एक सक्रिय रूप से विकसित, ओपन-सोर्स Oracle VM के लिए प्राथमिक डिस्क फ़ाइल स्वरूप है, जिसे VirtualBox के रूप में जाना जाता है, जो एक एंटरप्राइज़-क्लास वर्चुअलाइजेशन उत्पाद है। VDI फ़ाइल स्वरूप एक पोर्टेबल डिस्क छवि बनाने के लिए डिज़ाइन किया गया है जिसे अन्य वर्चुअलाइजेशन प्रोग्राम का उपयोग करके आसानी से चलाया जा सकता है। यह गतिशील रूप से आवंटित और निश्चित आकार के भंडारण दोनों का समर्थन करता है। यह आपको एक छवि फ़ाइल बनाने के बाद उसका विस्तार करने की अनुमति देता है, भले ही उसमें पहले से ही डेटा हो।

### डिस्क वर्चुअलाइजेशन
सिस्टम VDI डिस्क छवि प्रारूप में हार्ड डिस्क का अनुकरण करता है। एक वर्चुअलबॉक्स वीएम माइक्रोसॉफ्ट वर्चुअल पीसी या वीएमवेयर में बनाए गए पुराने डिस्क के साथ-साथ अपने स्वयं के मूल प्रारूप का उपयोग कर सकता है। वर्चुअलबॉक्स या तो वर्चुअल हार्ड डिस्क के रूप में उपयोग करते हुए, मेजबान पर iSCSI लक्ष्य और कच्चे विभाजन से जुड़ने में सक्षम है। वर्चुअलबॉक्स IDE (PIIX4 और ICH6 कंट्रोलर), SATA (ICH8M कंट्रोलर), SAS कंट्रोलर का अनुकरण करता है जिससे हार्ड ड्राइव को जोड़ा जा सकता है और SCSI।

वर्चुअलबॉक्स के संस्करण 2.2.0 के बाद से ओपन वर्चुअलाइजेशन फॉर्मेट (ओवीएफ) के लिए समर्थन उपलब्ध है। होस्ट-कनेक्टेड भौतिक डिवाइस और आईएसओ इमेज दोनों को सीडी या डीवीडी ड्राइव के रूप में माउंट किया जा सकता है।
डिफ़ॉल्ट रूप से वर्चुअलबॉक्स वीईएसए संगत कस्टम वर्चुअल ग्राफिक्स कार्ड के माध्यम से ग्राफिक्स का समर्थन करता है।

### ईथरनेट के लिए वर्चुअलाइजेशन समर्थन
वर्चुअलबॉक्स ईथरनेट नेटवर्क एडेप्टर के लिए निम्नलिखित नेटवर्क इंटरफेस कार्ड का वर्चुअलाइजेशन करता है:
- एएमडी पीसीनेट पीसीआई II (एम79सी970ए)
- एएमडी पीसीनेट-फास्ट III (एम79सी973)
- इंटेल प्रो/1000 एमटी डेस्कटॉप (82540EM)
- इंटेल प्रो/1000 एमटी सर्वर (82545EM)
- इंटेल प्रो/1000 टी सर्वर (82543GC)
- Paravirtualized नेटवर्क एडेप्टर (virtio-net)

एमुलेटेड नेटवर्क कार्ड अतिथि ओएस को नेटवर्किंग हार्डवेयर के लिए ड्राइवरों को खोजने और स्थापित करने की आवश्यकता के बिना चलाने में सक्षम बनाता है क्योंकि वे अतिथि ओएस के हिस्से के रूप में उपलब्ध हैं। एक विशेष पैरावर्चुअलाइज्ड नेटवर्क एडेप्टर एक विशिष्ट हार्डवेयर इंटरफेस से मेल खाने की आवश्यकता को कम करके नेटवर्क के प्रदर्शन में सुधार करता है। इसलिए, इसे अतिथि में विशेष ड्राइवर समर्थन की आवश्यकता होती है।


## संदर्भ

* [वर्चुअलबॉक्स - विकिपीडिया द्वारा](https://en.wikipedia.org/wiki/VirtualBox#VirtualBox_Disk_Image)


