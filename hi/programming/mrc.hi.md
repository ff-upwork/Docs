{
  "date" : "2021-09-14", 
  "keywords" :[ "एमआरसी", "फाइल", "एक्सटेंशन", "फाइल फॉर्मेट", "एमआरसी कार्यान्वयन", "प्रोग्रामिंग गाइड", "एमआरसी उदाहरण", "एमआईआरसी", "एमआईआरसी स्क्रिप्टिंग लैंग्वेज", "आईएनआई की फाइलें", " mSL स्क्रिप्टिंग लैंग्वेज", "mIRC लैंग्वेज", "mIRC स्क्रिप्ट्स", "स्क्रिप्टिंग लैंग्वेज" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"एमआरसी - एमआईआरसी स्क्रिप्ट लैंग्वेज फाइल",
  "description":"MRC फ़ाइल स्वरूप और API के बारे में जानें जो MRC फ़ाइलें बना और खोल सकते हैं।",
  "linktitle" : "MRC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-14"
}

## एमआरसी फाइल क्या है?

एमआईआरसी एक स्क्रिप्टिंग भाषा है जो विंडोज ऑपरेटिंग सिस्टम में आईआरसी क्लाइंट (इंटरनेट रिले चैट) के रूप में एम्बेडेड है। यह व्यक्तिगत और चैनल उपयोग के लिए स्पैमिंग से सुरक्षा की सुविधा प्रदान करता है। उपयोगकर्ता संगतता का बेहतर अनुभव प्रदान करने के लिए, यह एमआईआरसी स्क्रिप्टिंग भाषा संवाद विंडो बनाने की अनुमति देती है। जिन फाइलों में स्क्रिप्ट होती हैं, ज्यादातर सादे पाठ प्रारूप में होती हैं, उन्हें MRC के विस्तार के साथ या [INI](/hi/system/ini/) की फाइलों के रूप में संग्रहित किया जाता है। इस भाषा के कार्यों को कमांड और पहचानकर्ता के रूप में जाना जाता है (जब वे मान लौटाते हैं)।

एमआईआरसी भाषा एक समय में एकाधिक स्क्रिप्ट फ़ाइलों को लोड करने की सुविधा प्रदान करती है। दूसरी ओर, एक फ़ाइल के एक साथ लोड होने पर दूसरी फ़ाइल का अब उपयोग नहीं किया जा सकता है। आदेश सहेजे जाते हैं और वे आईआरसी में स्वचालित रूप से मौजूद हो सकते हैं। इस भाषा में प्रयुक्त आदेश और उपनाम किसी भी वर्ण की पूर्वता शामिल नहीं करते हैं।

एमआईआरसी का व्यापक रूप से उपयोग किया जाता है ताकि बॉट स्वचालित रूप से एक चैनल का प्रबंधन कर सकें लेकिन इसे एमएसएल स्क्रिप्टिंग भाषा द्वारा भी संशोधित किया जा सकता है। यह मैक्रोज़, संगीत बजाने की क्षमता, छोटे मैक्रोज़ और फ़ंक्शंस, बुनियादी गेम या छोटे अनुप्रयोगों के संचालन जैसी कई नई सुविधाएँ पेश कर सकता है।


## संक्षिप्त इतिहास ##

यह स्क्रिप्टिंग भाषा पहली बार 1995 में खालिद एडम बे द्वारा विकसित की गई थी। स्क्रिप्टिंग लैंग्वेज का डिजाइन भी खालिद ने ही बनाया था। इस भाषा का लक्ष्य इवेंट-संचालित प्रोग्रामिंग था। प्रारंभ में, इस प्रोग्रामिंग भाषा की फ़ाइलों के लिए उपयोग किया जाने वाला फ़ाइल एक्सटेंशन .mrc और .ini था। इसके अलावा, इसे मालिकाना सॉफ्टवेयर के लाइसेंस के तहत विकसित किया गया था।

## तकनीकी विशिष्टता ##

कुछ कार्यों को इस एमआईआरसी भाषा के माध्यम से कस्टम स्क्रिप्ट किया गया है और उपनाम के रूप में जाना जाता है। जब ये उपनाम मान लौटाते हैं तो उन्हें कस्टम पहचानकर्ता के रूप में जाना जाता है। इस एमआईआरसी भाषा में निहित सभी चर गतिशील रूप से टाइप किए गए हैं। सिगिल का उपयोग एमआईआरसी लिपियों द्वारा किया जाता है। इस स्क्रिप्टिंग भाषा की एक अन्य विशेषता पॉप-अप है। उपयोगकर्ता केवल पॉप-अप का चयन करके उन्हें कॉल कर सकते हैं। कुछ घटनाओं के लिए रिमोट निर्दिष्ट हैं। सापेक्ष घटना होने पर रिमोट को बुलाया जाता है।

इस भाषा के कोड की प्रत्येक पंक्ति को तोड़ने के लिए स्पेस सीमांकित टोकन का उपयोग किया जाता है। एमआईआरसी फाइलों के लिए उपयोग किए जाने वाले कुछ अन्य लोकप्रिय एक्सटेंशन हैं जैसे एमडीएक्स (एमआईआरसी डायलॉग एक्सटेंशन) और डीसीएक्स (डायलॉग कंट्रोल एक्सटेंशन)। ये दोनों संवाद विस्तार हैं और तुलनात्मक रूप से अधिक लोकप्रिय हैं। इस स्क्रिप्टिंग भाषा के नामकरण द्वारा भाषा निर्माणों को संदर्भित किया जाता है। MIRC भाषा में स्क्रिप्टिंग भाषा के विभिन्न पहलू शामिल होते हैं जैसे स्थानीय और वैश्विक चर, बाइनरी चर, हैश टेबल और फ़ाइल हैंडलिंग।


## एमआरसी फ़ाइल स्वरूप उदाहरण ##

```

;Defines the alias 'hello' in the remote script

;Note: if this is placed in an alias script,
;the 'alias' part must be removed (result: hello {)
;Usage: /hello

alias hello {

  ;Displays(/hi/echo) 'Hello World!' into the active window(-a)
  echo -a Hello World!

}

```

```
;Placed in a remote script

;When a user types Hello! in a channel,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:#:{ msg $chan Hello, $nick $+ ! }

;When a user types Hello! in a private message,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:?: { msg $nick Hello, $nick $+ ! }

;Here is a script which automatically gives voice to a user
;who joins a particular channel (The Bot or user should have HOP)

on *:JOIN:#?: { mode $chan +v $nick }

;A bad word script

on *:Text:die*:#: { .mode $chan +b $nick | kick $chan $nick Dont say that again }

```

## संदर्भ ##

* [एमआईआरसी - विकिपीडिया द्वारा](https://en.wikipedia.org/wiki/MIRC_scripting_language)


