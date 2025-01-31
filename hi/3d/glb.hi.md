{
  "date" : "2019-12-03",
  "keywords" :[ "जीएलबी", "फाइल", "फॉर्मेट", "फाइल टाइप", "एक्सटेंशन", "जीएलबी फाइल क्या है?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"जीएलबी",
  "description":"जीएलबी फ़ाइल प्रारूप और एपीआई के बारे में जानें जो जीएलबी फाइलें खोल और बना सकते हैं।",
  "linktitle" : "GLB",
  "menu" : {
    "docs" : {
      "identifier":"3d-glb",
      "parent" : "3d"
}
},
  "lastmod" : "2020-09-01"
}

## जीएलबी फाइल क्या है?

GLB, GL ट्रांसमिशन फॉर्मेट ([glTF](/hi/3d/gltf/)) में सहेजे गए 3D मॉडल का बाइनरी फ़ाइल स्वरूप प्रतिनिधित्व है। बाइनरी प्रारूप में नोड पदानुक्रम, कैमरा, सामग्री, एनिमेशन और मेश जैसे 3D मॉडल के बारे में जानकारी। यह बाइनरी प्रारूप glTF संपत्ति (JSON, .bin और छवियों) को बाइनरी ब्लॉब में संग्रहीत करता है। यह फ़ाइल आकार में वृद्धि के मुद्दे से भी बचता है जो कि glTF के मामले में होता है। GLB फ़ाइल प्रारूप के परिणामस्वरूप कॉम्पैक्ट फ़ाइल आकार, तेज़ लोडिंग, पूर्ण 3D दृश्य प्रतिनिधित्व और आगे के विकास के लिए एक्स्टेंसिबिलिटी होती है। प्रारूप मॉडल/gltf-बाइनरी को MIME प्रकार के रूप में उपयोग करता है।

## GLB फ़ाइल स्वरूप - अधिक जानकारी

GlTF द्वारा उपयोग की जाने वाली सामग्री वितरण विधियों के परिणामस्वरूप बेस -64 एन्कोडेड बाइनरी डेटा को डीकोड करने के लिए अतिरिक्त प्रसंस्करण होता है और फ़ाइल का आकार भी 33% बढ़ जाता है। इन वितरण विधियों, जिन्होंने GLB फ़ाइल स्वरूप के निर्माण में योगदान दिया, में शामिल हैं:

* glTF JSON बाहरी बाइनरी डेटा (ज्यामिति, की-फ़्रेम, स्किन) और इमेज की ओर इशारा करता है।
* glTF JSON बेस64-एन्कोडेड बाइनरी डेटा और डेटा यूआरआई का उपयोग करके छवियों को इनलाइन एम्बेड करता है।

GLB को एक कंटेनर प्रारूप के रूप में बाइनरी फ़ाइल स्वरूप के रूप में पेश किया गया था ताकि glTF के कारण होने वाली समस्याओं से बचने के लिए बाइनरी ब्लॉब में glTF संपत्ति का प्रतिनिधित्व किया जा सके। जीएलबी फ़ाइल प्रारूप [विनिर्देश](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0#glb-file-format-specification) को किसी भी पाठक/लेखक द्वारा अनुप्रयोग विकास के लिए लागू करने के लिए संदर्भित किया जाना चाहिए .

## GLB फ़ाइल संरचना

GLB फ़ाइल स्वरूप छोटे एंडियन पर आधारित है और इसकी संरचना से पता चलता है कि इसमें शामिल हैं:

* एक 12-बाइट प्रस्तावना, शीर्षक शीर्षक।
* एक या अधिक भाग जिनमें JSON सामग्री और बाइनरी डेटा शामिल हैं।

#### जीएलबी हैडर

GLB फ़ाइल स्वरूप शीर्षलेख में तीन 4-बाइट प्रविष्टियाँ होती हैं:

* uint32 जादू - जादू 0x46546C67 के बराबर है। यह ASCII स्ट्रिंग glTF है, और इसका उपयोग डेटा को बाइनरी glTF के रूप में पहचानने के लिए किया जा सकता है
* uint32 संस्करण - बाइनरी glTF कंटेनर प्रारूप के संस्करण को इंगित करता है
* uin32 लंबाई - बाइनरी glTF की कुल लंबाई, जिसमें हेडर और बाइट्स में सभी भाग शामिल हैं

#### चंक्स

GLB फ़ाइल में प्रत्येक खंड में निम्नलिखित संरचना होती है:

|uint32|uint32|ubyte[]
---|---|---|
|चंकलेंथ|चंकटाइप|चंकडाटा

* `chunkLength` - बाइट्स में चंकडेटा की लंबाई
* `chunkType` - चंक के प्रकार को इंगित करता है
* `chunkData` - चंक का बाइनरी पेलोड

जहां खंड प्रकार हैं:

|# |चंक प्रकार|ASCII|विवरण|घटनाएँ
---|---|---|---|---|
|1.|0x4E4F534A|JSON|संरचित JSON सामग्री|1
|2.|0x004E4942|BIN|बाइनरी बफर|0 या 1

प्रत्येक चंक की शुरुआत और अंत को 4-बाइट सीमा से जोड़ा जाना चाहिए और इस उद्देश्य के लिए पैडिंग का उपयोग किया जाना चाहिए।

##### संरचित JSON सामग्री

यह बाइनरी glTF एसेट का सबसे पहला हिस्सा होना चाहिए और कार्यान्वयन को बाद के हिस्सों से संसाधनों को उत्तरोत्तर पुनर्प्राप्त करने में सक्षम बनाता है। यह बाइनरी glTF एसेट से संसाधनों के केवल एक चयनित सबसेट को पढ़ने की क्षमता भी प्रदान करता है जैसे कि मेष का सबसे मोटा LOD। संरेखण आवश्यकताओं को पूरा करने के लिए, इस खंड को अनुगामी अंतरिक्ष वर्णों (0x20) के साथ गद्देदार किया जाना चाहिए।

##### बाइनरी बफर #####

इस खंड में ज्यामिति, एनीमेशन कुंजी फ्रेम, खाल और छवियों के लिए बाइनरी पेलोड होता है। यह बाइनरी glTF संपत्ति का दूसरा हिस्सा होना चाहिए और संरेखण आवश्यकताओं को पूरा करने के लिए अनुगामी शून्य (0x00) के साथ गद्देदार होना चाहिए।

## संदर्भ ##

* [जीएलबी फ़ाइल प्रारूप विनिर्देश - ख्रोनोस](/hi/3d/gltf/)

