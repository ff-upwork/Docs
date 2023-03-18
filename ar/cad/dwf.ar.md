{
  "date" : "2020-03-16",
  "keywords" :["DWF" , "تنسيق الملف" , "فتح" , "قراءة" , "إنشاء" , "CAD"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "description" :"تعرف على تنسيق ملف DWF وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات DWF وفتحها." ,
  "title" :"تنسيق ملف DWF" ,
  "linktitle" : "DWF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
} ,
  "lastmod" : "2019-09-10"
}

## ما هو ملف DWF؟

يمثل تنسيق تصميم الويب (DWF) رسمًا ثنائي الأبعاد / ثلاثي الأبعاد بتنسيق مضغوط لعرض ملفات التصميم أو مراجعتها أو طباعتها. يحتوي على رسومات ونصوص كجزء من بيانات التصميم وتقليل حجم الملف بسبب تنسيقه المضغوط. يجعل حجم الملف المنخفض توزيع بيانات التصميم الثرية وإيصالها أمرًا فعالاً. لا يتطلب DWF من المستلم معرفة استخدام برنامج CAD الذي أنشأ الرسم الأصلي. يمكن أن تكون محتويات تنسيق ملف DWF بسيطة وتتضمن ورقة واحدة فقط أو معقدة بما يكفي للحصول على الخطوط والألوان والصور.

## نبذة تاريخية ##

قدم Autodesk تنسيق ملف DWF في عام 1995 كجزء من البرنامج الإضافي Netscape Navigation ، WHIP. تطور التنسيق من تنسيق ثنائي الأبعاد فقط ليشمل محتويات ثلاثية الأبعاد مع مرور الوقت. تستفيد العديد من تطبيقات الجهات الخارجية أيضًا من هذا التنسيق.

## تنسيق ملف DWF ##

DWF هو تنسيق مفتوح وآمن مصمم خصيصًا لمشاركة بيانات التصميم الهندسي الثرية. وهي مستقلة عن برامج التطبيق والأجهزة ونظام التشغيل الأصلي المستخدم لإنشاء بيانات التصميم هذه. يتيح ذلك لأعضاء الفريق الذين لا يستخدمون تطبيقات CAD المشاركة في العمليات الرقمية من خلال عرض تصميمات المباني أو نظم المعلومات الجغرافية أو المنتجات. يتكون أرشيف ملف DWF من عدة ملفات XML وملفات ثنائية يتم تجميعها معًا في أرشيف مضغوط تم إنشاؤه بضغط [ZIP](/ar/ compression / zip /). يمكنك إعادة تسمية امتداد ملف DWF إلى ZIP وعرض محتويات الملف. يمكن أن تحتوي حزمة DWF على العديد من أنواع بيانات التصميم مثل الرسومات ثنائية الأبعاد والرسومات ثلاثية الأبعاد والبيانات الوصفية للحزمة والقسم وملفات الموارد الأخرى.

** ملفات البيانات الوصفية DWF ** - ملفات XML التي تحتوي على معلومات تتعلق بالبيانات الوصفية والهيكل (المؤلف ، العنوان ، وقت الإنشاء ، تبعيات القسم ، ترتيب الأقسام ، أوصاف ملف الموارد ، الأدوار ، أنواع المحاكاة ، إلخ) وتتعلق بالقسم (الصفحة المعلومات وتصميم البيانات الوصفية وما إلى ذلك). تُستخدم البيانات الوصفية الهيكلية لإنشاء كائنات منطقية (مجموعات من الملفات لتمثيل جزء أو صفحة ، وما إلى ذلك).

** ملفات الموارد ** - الوسائط أو ملفات المحتوى الأخرى المشار إليها من البيانات الوصفية للحزمة / القسم وعادة ما تكون عروض تقديمية لبيانات التصميم بتنسيقات مختلفة (ZGL ، W2D ، [JPG](/ar/ image / jpeg /) ، [PNG](/ar/ image / png /) ، AVI ، XML ، [TXT](/ar/ معالجة الكلمات / txt /) ، [DOC](/ar/ معالجة الكلمات / doc /) ، إلخ.)

### تفاصيل تنسيق الملف ###

تم تنظيم ملفات DWF في ثلاثة أقسام رئيسية كما هو موضح أدناه.

* رأس تعريف الملف
* كتلة بيانات الملف
* مقطورة إنهاء الملف

#### رأس معرف الملف ####

يسمح رأس معرف الملف بالتعرف على ملفات DWF حسب التطبيقات. كما أنه يحدد أي إصدار من مواصفات DWF تم استخدامه لتشفير الملف. وهو عبارة عن رأس 12 بايت يتم ترتيبه على النحو التالي:


| بايت | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11
--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- |
| شخصية | (| D | W | F | (مسافة) | V | 0 | 0 |. | 3 | 0 |)

فيما يلي ملخص لهذا الجدول:

* تمثل البايتات الستة الأولى من الرأس دائمًا أحرف ASCII "(DWF V"
* تحتوي 5 بايت التالية على معلومات حول رقم الإصدار ، على سبيل المثال "00.30" مع قيمة الإصدار الرئيسي والثانوي للتنسيق

يجب أن تحدد التطبيقات التي تنشئ ملف DWF أقل رقم إصدار ممكن يحتاجه تطبيق القارئ لدعمه من أجل استخدام البيانات بشكل صحيح.

#### كتلة بيانات الملف ####

تبدأ كتلة بيانات الملف عند 13 بايت من ملف DWF ، وهي سلسلة من أزواج كود التشغيل والمعاملات ، كما هو موضح في الجدول التالي.

| حقل 1 | حقل 2 | حقل 3 | حقل 4 | حقل 5 | حقل 5
--- | --- |--- | --- |--- | --- |
| كود التشغيل | المعامل | كود التشغيل | المعامل | كود التشغيل | المعامل

يمكن أن يحتوي ملف DWF على أزواج معامِل وكود تشغيل مثل ASCII قابل للقراءة بالإضافة إلى رمز ثنائي أو مزيج من الاثنين معًا. تحتوي جميع عمليات DWF على نموذج تشغيل / معامل ASCII قابل للقراءة ، كما تحتوي معظم العمليات أيضًا على كود تشغيل / نموذج تشغيل ثنائي مشفر. أكواد التشغيل في بايت واحد مما يسمح بأكثر من 200 عملية. ASCII الممتد والثنائي الممتد هي حالات استثنائية. يمكن أن تتراوح قيم أكواد التشغيل من 0-255 مع بعض الاستثناءات. باستثناء النوعين الخاصين من أكواد التشغيل الممتدة ASCII والثنائي الممتد ، يجب أن يعرف قارئ الملف كيفية حساب طول المعامل.

##### أكواد التشغيل المحظورة #####

لا يمكن استخدام تمثيلات ASCII لما يلي كأكواد تشغيل:

لا يمكن استخدام تمثيلات ASCII التالية كرموز تشغيل:

* مسافة (0x20)
* علامة تبويب (0x09)
* واصلة (0x2D)
* أرقام ASCII من 0 إلى 9 (0x30 - 0x39)
* إرجاع السطر (0x0D)
* تغذية الخط (0x0A)
* علامة اقتباس مفردة (0x27)
* علامة اقتباس مزدوجة (0x22)
* الفترة (0x2E)
* أقواس (0x28 و 0x29)
* الأقواس المتعرجة (0x7B و 0x7D)
* الأقواس المربعة (0x5B و 0x5D)
* شرطة مائلة للخلف (0x5C)

#### مقطورة إنهاء الملف ####

مقطورة إنهاء الملف لـ DWF هي مجرد كود تشغيل خاص يشير إلى نهاية الملف. يمكن لبعض التطبيقات تخزين بيانات غير DWF بعد رمز التشغيل الإنهاء. المقطع الدعائي كما هو موضح أدناه:


| بايت | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9
---|---|---|---|---|---|---|---|---|---|---|
| شخصية | (| E | n | d | 0 | f | D | W | F |)

## مراجع ##

* [DWF - بواسطة Wikipedia](https://en.wikipedia.org/wiki/Design_Web_Format)
* [تنسيق بيانات WHIP](http://paulbourke.net/dataformats/whip/)
* [http://blogs.msdn.com/opc/archive/2009/05/18/adventures-in-packaging-episode-1.aspx](http://blogs.msdn.com/opc/archive/2009 /05/18/adventures-in-packaging-episode-1.aspx)
