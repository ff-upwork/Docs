{
  "date" : "2019-10-11",
  "keywords" :["ملف djvu" , "تنسيق ملف djvu" , "ما هو ملف djvu" , "ملف" , "مثال djvu" , "امتداد ملف djvu" , "امتداد" , "تنسيق"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف DJVU" ,
  "description":"تعرف على تنسيق ملف DJVU وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات DJVU وفتحها." ,
  "linktitle" : "DJVU",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
} ,
  "lastmod" : "2019-09-10"
}

## ما هو ملف DJVU؟

يُنطق DjVu باسم "déjà vu" ، وهو تنسيق ملف رسومي مخصص للوثائق والكتب الممسوحة ضوئيًا وخاصة تلك التي تحتوي على مزيج من النصوص والرسومات والصور والصور الفوتوغرافية. تم تطويره بواسطة AT&T Labs. يستخدم تقنيات متعددة مثل فصل طبقة الصور للنص وصور الخلفية ، والتحميل التدريجي ، والتشفير الحسابي والضغط المفقود للصور البتونية. نظرًا لأن ملف DJVU يمكن أن يحتوي على صور ملونة وصور فوتوغرافية ونصوص ورسومات مضغوطة وعالية الجودة ويمكن حفظها في مساحة أقل ، يتم استخدامه على الويب ككتب إلكترونية وكتيبات وصحف ومستندات قديمة وما إلى ذلك.

يمكن تصنيف DjVu كبديل ممتاز لـ [PDF](/ar/pdf/). امتدادات الملفات المرتبطة بـ DjVu هي .DJVU أو .DJV. يمكن أن يحقق DjVu نسب ضغط حوالي 5-10 أفضل من الطرق الحالية مثل [JPEG](/ar/image/jpeg/) و [GIF](/ar/image/gif/) للمستندات الملونة و 3 - 8 مرات أفضل من [TIFF]( / image / tiff /) في المستندات بالأبيض والأسود. يمكن ضغط المستندات الممسوحة ضوئيًا بدقة 300 نقطة في البوصة بألوان كاملة حتى 25 ميجابايت حتى 30 إلى 100 كيلوبايت. وبالمثل ، يمكن ضغط المستندات بالأبيض والأسود حتى 5 إلى 30 كيلوبايت. يمكن أن يصل متوسط صفحة HTML إلى 50 كيلوبايت ، وبالتالي ، يمكن تحميل هذه المستندات على الشبكة دون أي مشكلة.

## نبذة تاريخية ##

تم تطوير تقنية DjVu في معامل AT&T بواسطة [Yann LeCun](https://en.wikipedia.org/wiki/Yann_LeCun) ، [Léon Bottou](https://en.wikipedia.org/wiki/L%C3%A9on_Bottou) و Patrick Haffner و Paul G من عام 1996 إلى عام 2001. وقد مر تنسيق ملف DjVu عبر العديد من المراجعات ، كان آخرها من عام 2005.


| الإصدار | تاريخ الإصدار | ملاحظات
---|---|---|
| 1–19 | 1996-1999 | هذه هي الإصدارات التطويرية.
| 20 | أبريل 1999 | تم تغيير الصفحة الواحدة إلى تنسيق Multipage.
| 23 | يوليو 2002 | مقطع CID
| 24 | فبراير 2003 | LTAnno قطعة
| 21 | سبتمبر 1999 | تم استبدال تنسيق التخزين غير المباشر. تمت إضافة طبقة البحث عن النص.
| 22 | أبريل 2001 | اتجاه الصفحة ، اللون JB2
| 25 | مايو 2003 | جزء NAVM. تمت إضافة دعم الإشارات المرجعية DjVu.
| 26 | أبريل 2005 | تعليقات توضيحية نصية / سطرية

## تنسيق ملف DjVu ##

مستندات DjVu هي ملفات IFF85. يوفر الهيكل تسلسلًا هرميًا للحاويات التي تحتوي على معلومات في ملف DjVu. وتسمى هذه الحاويات أيضًا "القطع". يصف نوع القطعة ومعرف المجموعة كيفية استخدام القطعة. يوجد رأس 4 بايت متبوعًا ببنية IFF. أول أربع بايتات من ملف DjVu هي 0x41 0x54 0x26 0x54. يناقش هذا القسم الأنواع المختلفة لوثائق DjVu والأجزاء المقابلة التي تتكون منها.


| معرف المجموعة | الاستخدام
---|---|
| FORM | المقطع المركب الذي يحتوي على أول أربع بايتات بيانات من مقطع FORM والتي تعتبر معرفًا ثانويًا.
| FORM: DJVM | مستند DjVu متعدد الصفحات. قطعة مركبة تحتوي على جزء DIRM.
| FORM: DJVU | مستند DjVu ذو صفحة واحدة. قطعة مركبة تحتوي على الأجزاء التي تشكل صفحة في مستند djvu.
| FORM: DJVI | ملف DjVu "مشترك" والذي يتم تضمينه عبر مقطع INCL. التعليقات التوضيحية المشتركة وقاموس الأشكال.
| النموذج: THUM | قطعة مركبة تحتوي على TH44 أجزاء وهي الصور المصغرة المضمنة.
| DIRM | معلومات اسم الصفحة للمستندات متعددة الصفحات.
| NAVM | معلومات مرجعية
| ANTa و ANTz | التعليقات التوضيحية بما في ذلك إعدادات العرض الأولية والارتباطات التشعبية المتراكبة ومربعات النص وما إلى ذلك.
| TXTa ، TXTz | معلومات تخطيط ونص Unicode.
| Djbz | جدول الشكل المشترك.
| Sjbz | بيانات بيتونية JB2 مضغوطة BZZ تُستخدم لتخزين القناع.
| FG44 | بيانات IW44 المستخدمة لتخزين المقدمة
| BG44 | بيانات IW44 المستخدمة لتخزين الخلفية
| TH44 | بيانات IW44 المستخدمة لتخزين الصور المصغرة المضمنة
| WMRM | بيانات JB2 مطلوبة لإزالة العلامة المائية
| FGbz | لون بيانات JB2. يوفر لونًا لكل (blit أو شكل؟) في مقطع Sjbz المقابل.
| INFO | معلومات حول صفحة DjVu
| INCL | معرّف النموذج المضمن: قطعة DJVI.
| BGjp | خلفية JPEG مشفرة
| FGjp | المقدمة المشفرة بتنسيق JPEG
| Smmr | القناع المشفر G4

### ضغط DJVU

تنقسم الصورة الفردية إلى صور مختلفة ، ثم يتم ضغط كل صورة على حدة. لإنشاء ملف DjVu ، يتم أولاً فصل الصورة إلى ثلاث صور وخلفية ومقدمة وصورة قناع. عادةً ما تكون صور الخلفية والمقدمة عبارة عن صور ملونة منخفضة الدقة ؛ لكن صورة القناع هي صورة عالية الدقة وعادة ما يتم تخزين النص هناك. بعد الفصل ، يتم ضغط الصور الأمامية والخلفية من خلال خوارزمية ضغط تعتمد على الموجة IW44 ، بينما يتم ضغط صورة القناع باستخدام طريقة أخرى تسمى JB2.

تعمل طريقة الترميز JB2 على التخلص من الكثير من التكرار في صورة النص عن طريق تحديد الأشكال المتطابقة على الصفحة ، مثل التكرارات المتعددة لحرف في خط معين. يقوم JB2 أولاً بترميز الصورة النقطية لكل شكل فريد من خلال الاستفادة من التكرار بين الأشكال المتشابهة. ثم يقوم بترميز المواقع التي يظهر فيها كل شكل على الصفحة. يعتمد كل من JB2 و IW44 على نوع جديد من المبرمج الحسابي الثنائي التكيفي يسمى ZP-coder الذي يزيل أي فائض متبقي في حدود نسبة قليلة من حد شانون. المبرمج ZP قابل للتكيف ، وأسرع من المبرمجين الحسابيين التقريبيين الآخرين.

## مراجع ##

* [DjVu - Wikipedia](https://en.wikipedia.org/wiki/DjVu)
* [تنسيق ملف DjVu](https://www.cuminas.jp/docs/techinfo/DjVu3Spec.pdf)

