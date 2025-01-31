{
  "date" : "2022-03-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NUPKG फ़ाइल - NuGet पैकेज फ़ाइल",
  "description":"NUPKG फ़ाइल स्वरूप और API के बारे में जानें जो NUPKG फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "NUPKG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-09"
}

## एनयूपीकेजी फाइल क्या है?

NUPKG फ़ाइल एक पैकेज फ़ाइल है जिसमें .NET प्रोजेक्ट में उपयोग किए जाने वाले पैकेज बनाने के लिए NuGet सॉफ़्टवेयर द्वारा उपयोग किए जाने वाले स्रोत कोड होते हैं। रिपॉजिटरी होस्ट करने वाले ऑनलाइन पैकेज से पैकेज लाने के लिए माइक्रोसॉफ्ट विजुअल स्टूडियो के हिस्से के रूप में NuGet पैकेज मैनेजर घटक स्थापित किया गया है। NUPKG फ़ाइलें विकास पैकेजों को मैन्युअल रूप से डाउनलोड और इंस्टॉल करने के बजाय NuGet Package Manager का उपयोग करके [Nuget.org](https://nuget.org) से नवीनतम पैकेज लाने में डेवलपर्स की मदद करती हैं। NUPKG फ़ाइलें NUSPEC फ़ाइलों से बनाई गई हैं और, प्राप्त होने पर, उपयोगकर्ता सिस्टम पर पैकेज स्थापित करें।

## NUPKG फ़ाइल स्वरूप

NUPKG फ़ाइलें [ज़िप](/hi/compression/zip/) संग्रह हैं जिनमें इसके अंदर पैक की गई लाइब्रेरी होती हैं। जब डाउनलोड किया जाता है, तो इसे .zip में बदला जा सकता है और WinZIP, 7-Zip, और Apple संग्रह उपयोगिता जैसी किसी भी मानक ज़िप उपयोगिताओं के साथ निकाला जा सकता है।

## संदर्भ

* [Nuget.org](https://nuget.org)
* [क्विकस्टार्ट: विजुअल स्टूडियो (केवल विंडोज़) में एक पैकेज स्थापित करें और उसका उपयोग करें](https://learn.microsoft.com/en-us/nuget/quickstart/install-and-use-a-package-in-visual-studio)
* [नगेट पैकेज कैसे बनाएं और प्रकाशित करें](https://learn.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package-using-visual-studio?tabs=netcore-cli)

