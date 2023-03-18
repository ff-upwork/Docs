{
  "date" : "2021-09-15", 
  "keywords" :["erb", "फ़ाइल", "विस्तार", "फ़ाइल स्वरूप", "erb कार्यान्वयन", "प्रोग्रामिंग गाइड", "erb उदाहरण", "eRuby", "eRuby फ़ाइल स्वरूप", "eRuby भाषा स्क्रिप्ट", " eRuby टेम्प्लेट", "erb भाषा", "ERB रूबी भाषा", "eRuby भाषा" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ईआरबी - ईरूबी भाषा फ़ाइल",
  "description":"ईआरबी फ़ाइल प्रारूप और एपीआई के बारे में जानें जो ईआरबी फाइलें बना और खोल सकते हैं।",
  "linktitle" : "ERB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-15"
}

## एक ईआरबी फ़ाइल क्या है?

eRuby भाषा एक टेंपलेटिंग सिस्टम है जो रूबी को टेक्स्ट डॉक्यूमेंट में एम्बेड करता है। ईरूबी का टेंपलेटिंग सिस्टम रूबी कोड और प्लेन टेक्स्ट को फ्लो कंट्रोल और वेरिएबल सब्स्टीट्यूशन प्रदान करने के लिए जोड़ता है, जिससे इसे बनाए रखना आसान हो जाता है। यह अक्सर एक [एचटीएमएल](/hi/वेब/एचटीएमएल/) दस्तावेज़ में रूबी कोड को एम्बेड करने के लिए प्रयोग किया जाता है, एएसपी, [जेएसपी](/hi/प्रोग्रामिंग/जेएसपी/) और [पीएचआर](/hi/प्रोग्रामिंग/पीएचपी/) और अन्य सर्वर के समान -साइड स्क्रिप्टिंग लैंग्वेज। ईआरबी रूबी आमतौर पर वेब पेज बनाती है।

रूबी ऑन रेल्स का दृश्य मॉड्यूल एक ब्राउज़र पर प्रतिक्रिया या आउटपुट प्रदर्शित करने के लिए उत्तरदायी है। अपने सरलतम रूप में, एक दृश्य HTML कोड का एक टुकड़ा हो सकता है जिसमें कुछ स्थिर सामग्री होती है। अधिकांश अनुप्रयोगों के लिए, केवल स्थिर सामग्री होना पर्याप्त नहीं हो सकता है। कई रेल अनुप्रयोगों को उनके विचार में प्रदर्शित करने के लिए नियंत्रक द्वारा बनाई गई गतिशील सामग्री की आवश्यकता होगी। यह एंबेडेड रूबी का उपयोग करके टेम्प्लेट उत्पन्न करने के लिए संभव है, जिसमें डायनेमिक सामग्री शामिल हो सकती है।

एंबेडेड रूबी रूबी कोड को एक दृश्य दस्तावेज़ में एम्बेड करने की अनुमति देता है। यह कोड रन टाइम पर कोड के निष्पादन से उत्पन्न उचित मूल्य के साथ बदल जाता है। लेकिन, एक दृश्य दस्तावेज़ में कोड एम्बेड करने की क्षमता होने से हम MVС फ़्रेम में मौजूद स्पष्ट विभाजन को पाटने का जोखिम उठाते हैं। इस प्रकार यह सुनिश्चित करने के लिए डेवलपर की जिम्मेदारी है कि मॉडल के बीच जिम्मेदारी का एक स्पष्ट पृथक्करण है, मॉडल के दृश्य और नियंत्रक मॉड्यूल।



## संक्षिप्त इतिहास ##

Ruby को 1990 के दशक के मध्य में Yukihirо Mаtsumоtо द्वारा डिज़ाइन किया गया था। युकिहिरो मात्सुमोतो रूबी के पिता हैं और रूबी समुदाय में, वह मात्ज़ के रूप में प्रसिद्ध हैं। रूबी लिपि को शुरू में 1995 में पेश किया गया था और रूबी का पहला संस्करण रूबी 95 था जो 1995 में जारी किया गया था।

युकीहिरो मात्सुमोतो एक पूरी तरह से ऑब्जेक्ट ओरिएंटेड प्रोग्रामिंग लैंग्वेज चाहते थे, जिसे स्क्रिप्टिंग लैंग्वेज के रूप में आसानी से इस्तेमाल किया जा सकता है। इसलिए, उन्होंने eRuby भाषा डिजाइन की। युकीहिरो मात्सुमतो और कीजु इशितशुका के चैट सत्र में दो नामों को प्रोग्रामिंग भाषा के लिए सूचीबद्ध किया गया था जो "सोरल" और "रूबी" है, बाद में युकीहिरो मात्सुमोतो ने "रूबी" नाम चुना।


## तकनीकी विशिष्टता ##

eRuby फ़ाइल स्वरूप ऑब्जेक्ट ओरिएंटेड प्रोग्रामिंग аррrоасh जैसे क्लास, इनहेरिटेंस, एब्स्ट्रैक्शन, पॉलीमॉरिज़्म और एनसार्सुलेशन, आदि के विभिन्न प्रकारों को पसंद करता है। वस्तु उन्मुख प्रोग्रामिंग दृष्टिकोण की विशेषता रखरखाव और विकास को आसान बनाती है। eRuby भाषा की स्क्रिप्ट भी рrосedurаl рrоgrаmming аррrоасh की विशेषता का समर्थन करती है। प्रक्रियात्मक प्रोग्रामिंग में एक विशेष समस्या को हल करने के लिए हर कार्यक्रम के लिए निर्दिष्ट चरण होते हैं।

eRuby टेम्प्लेट रिच क्लास इनबिल्ट लाइब्रेरी की एक विशाल रेंज प्रदान करता है, जिसके साथ प्रोग्रामर किसी भी वेब एप्लिकेशन या प्रोग्राम को आसानी से और जल्दी से विकसित कर सकते हैं। eRuby एक सामान्य उद्देश्य या बहुउद्देश्यीय प्रोग्रामिंग भाषा है, जिसका अर्थ है कि इसका उपयोग प्रोग्रामर्स द्वारा अनुप्रयोगों और कार्यक्रमों के विभिन्न प्रकारों को विकसित करने में किया जा सकता है।

ईआरबी रूबी भाषा एक सरल और एक सामान्य स्रोत प्रोग्रामिंग भाषा है और आप इसे अपनी परियोजना आवश्यकताओं के अनुसार संशोधित भी कर सकते हैं। यह विभिन्न प्रकार के रिच इनबिल्ट फीचर्स और टूल्स प्रदान करता है। भाषा भी स्वचालित कचरा संग्रहकर्ता की सुविधा प्रदान करती है।

अन्य प्रोग्रामिंग भाषाओं की तुलना में ईरूबी में कोडिंग बहुत तेज है। और यह एक लचीली प्रोग्रामिंग भाषा भी है क्योंकि यह प्रत्येक उपयोगकर्ता को अपनी आवश्यकताओं के अनुसार अपने भागों को संशोधित करने की अनुमति देती है। यह सिंगल इनहेरिटेंस और मिक्सिन्स फीचर का समर्थन करता है और अपने उपयोगकर्ताओं को डायनामिक टाइपिंग फीचर भी प्रदान करता है। eRuby एक संवेदनशील प्रोग्रामिंग भाषा है और इसकी संवेदनशीलता के कारण इसका एक बड़ा सहायक समुदाय है।


## ईआरबी फ़ाइल स्वरूप उदाहरण ##

ईआरबी टेम्प्लेट में निम्नलिखित प्रकार के टैग हैं:

### अभिव्यक्ति ###

```
<%= %>
```

```
require 'erb'
x = 500
template = ERB.new("The value of x is: <%= x %>")
puts template.result(binding)
```

### कार्यान्वयन ###

```
<% %>
```

```
<ul>
<% 4.times do %>

  <li>list item</li>

<% end %>
</ul>
```

### टिप्पणियाँ ###

```
<%# %>
```

```
<%# ruby code %>
```

### अन्य टैग ###

```
<%2.times do -%> 
    <%= @name %>
<% end -%>

```

### कक्षा उदाहरण ###

```
class ERBExample
  attr_accessor:variable1
  
  # using bind to access class variables
  def render()
    renderer.result(binding)
  end

  def initialize(variable1)
    @variable1 = variable1
  end

  # Expose private binding() method.
  def get_binding
    binding()
  end
end

example = ERBExample.new(variable1)
renderer = ERB.new(template)
puts output = renderer.result(example.get_binding)

```

## संदर्भ ##

* [ईआरबी - विकिपीडिया द्वारा](https://en.wikipedia.org/wiki/ERuby)


