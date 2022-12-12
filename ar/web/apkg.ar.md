{
  "date" : "2019-10-11",
   "keywords" :["apkg" , "ملف apkg" , "تنسيق ملف apkg" , "نوع ملف apkg" , "ملف" , "النوع" , "ما هو ملف APKG"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"APKG - تنسيق ملف Anki Flashcard Deck" ,
  "description" :"تعرف على ما هو ملف APKG وواجهات برمجة التطبيقات التي يمكنها إنشاءها وفتحها." ,
  "linktitle" : "APKG",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2021-06-16"
}

## ما هو ملف APKG؟

الملف بامتداد .apkg هو مجموعة من البطاقات التعليمية التي تم إنشاؤها لاستخدامها في تطبيق برمجي [Anki] (https://ankiweb.net/about) وهو برنامج تعليمي قائم على البطاقات التعليمية. يحتوي على نص [HTML] (/ar/ web / html /) ليتم تحميله وعرضه في تطبيق Anki ويمكن أن يحتوي أيضًا على صور وأصوات للتعلم المرئي والمسموع. يسمح Anki للمستخدمين بإنشاء مجموعات بطاقات Anki التعليمية الخاصة بهم بالإضافة إلى استيراد مجموعات البطاقات التعليمية الخاصة بالمستخدمين الآخرين.

## تنسيق ملف APKG

يتم إنشاء مجموعات بطاقات Anki من قوالب مكتوبة بلغة HTML ، وهي لغة مشهورة وشائعة لإنشاء صفحات الويب. يتم تصميم بطاقات سطح السفينة باستخدام CSS وهي اللغة المستخدمة لتصميم صفحات الويب. يتضمن التصميم تعديلات على:

* font-family - اسم الخط المراد استخدامه على البطاقة.
* حجم الخط - حجم الخط بالبكسل.
* محاذاة النص - تحدد ما إذا كان يجب محاذاة النص في الوسط أو اليسار أو اليمين.
* اللون - يحدد لون النص الذي يمكن أن يكون أسماء ألوان بسيطة مثل "أزرق" أو "أحمر" أو ما إلى ذلك أو رموز ألوان HTML.
* لون الخلفية - يحدد لون خلفية البطاقة

تتم مشاركة معلومات التصميم بين جميع البطاقات ، مما يؤثر على جميع البطاقات عند إجراء تغيير. سيستخدم المثال التالي خلفية صفراء على جميع البطاقات باستثناء الأولى:

```CSS
.card {
  background-color: yellow;
}
.card1 {
  background-color: blue;
}
```

يمكن التحكم في تغيير حجم الصور في بطاقة Anki على النحو التالي.

```CS
img {
  max-width: none;
  max-height: none;
}
```

## تضمين جافا سكريبت في بطاقات أنكي

من الممكن تضمين [Javascript] (/ar/ web / js /) في بطاقة Anki باستخدام قوالب البطاقة. ومع ذلك ، نظرًا للمستوى المتقدم لـ Javascript ، لم يتم توفير دعمها. علاوة على ذلك ، قد تُظهر أجهزة العرض تأثير تنفيذ Javascript في البطاقة بشكل مختلف ، مما يؤدي إلى الحاجة إلى اختبار التنفيذ على جميع الأجهزة. بعض ميزات Javascript معينة مثل window.alert ، مما يجعل من الصعب تصحيح أخطاء كود Javascript الذي كتبته.

## مراجع ##

* [وثائق Anki] (https://docs.ankiweb.net/intro.html)
