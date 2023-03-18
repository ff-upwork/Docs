{
  "date" : "2019-10-11",
  "keywords" :["ملف rar" , "تنسيق ملف rar" , "ما هو ملف rar" , "ملف" , "rar example" , "ملحق ملف rar" , "امتداد" , "تنسيق"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"RAR" ,
  "description":"ما هو امتداد ملف RAR وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات RAR وفتحها." ,
  "linktitle" : "RAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
} ,
  "lastmod" : "2019-09-10"
}

## ما هو ملف RAR؟

الملفات ذات الامتداد .rar هي ملفات أرشيفية يتم إنشاؤها لتخزين المعلومات في شكل مضغوط أو عادي. RAR ، الذي يرمز إلى تنسيق ملف Roshal ARchive ، هو تنسيق ملف خاص تم إنشاؤه بواسطة Eugene Roshal في عام 1995 الذي كان مهندس برمجيات روسي. يستخدم التنسيق لأرشفة الملفات بطرق مختلفة بما في ذلك تقنيات الضغط المختلفة. هناك العديد من البرامج التطبيقية المتاحة لأنظمة Windows و Linux و MacOS لاستخراج ملفات RAR. برنامج WinRAR ، بواسطة RARLab ، هو أداة أرشفة ملفات البرامج المشتركة (مجانًا لمدة 40 يومًا) لمنصة Microsoft Windows ؛ تم نقل البرنامج إلى Linux (كمستخرج فقط) بواسطة نفس المؤلف ، يوجين روشال.

## تاريخ إصدارات تنسيق ملف RAR

* الإصدار 1.3 (الأصل ، لا يحتوي على توقيع "Rar!")
* الإصدار 1.5
* v2.0 - تم إصداره مع WinRAR 2.0 و Rar لـ MS-DOS 2.0
* v2.9 - تم إصداره في الإصدار 3.00 من WinRAR
* v5.0 - مدعوم بواسطة WinRAR 5.0 والإصدارات الأحدث

## الميزات الرئيسية لتنسيق RAR

كان RAR في هذا المجال لفترة طويلة جدًا وكان أحد تنسيقات ملفات الأرشفة المفضلة. الميزات الرئيسية حول تنسيق RAR هي:

** `نسبة ضغط عالية:` ** متفوقة مقارنة بـ [ZIP](/ar/ ضغط / zip /) ، قابلة للمقارنة مع تنسيق 7z و zipx.

** "تشفير قوي للملفات حسب التصميم:" ** تعتمد أرشيفات RAR4 المشفرة على التشفير المستند إلى AES-128 بينما تعتمد أرشيفات RAR5 المشفرة على تشفير AES-256 مع جدولة مفاتيح محسّنة

** إمكانيات متقدمة لتصحيح الأخطاء واستعادة البيانات: "** سجلات الاسترداد الاختيارية أثناء إنشاء الأرشيف

** حجم الملف: `** الحد الأدنى 20 بايت والحد الأقصى 2 ^ 63 بايت للحجم (8 إكسابايت من الحجم الإجمالي للأرشيف)

** "أرشيفات RAR متعددة المجلدات:" ** إمكانية تقسيم الأرشيفات الكبيرة إلى عدة ملفات أصغر لتسهيل النقل عبر الشبكة. في مثل هذه الحالة ، تتم زيادة امتدادات الملفات بمقدار 1 لتمثيل وحدات التخزين المنقسمة

## تنسيق ملف RAR

المواصفات الكاملة لتنسيق RAR غير متاحة للجمهور ولهذا السبب لا يمكن صياغة تفاصيل التنسيق بطريقة موجزة.

### تخطيط الأرشيف العام

التخطيط العام لتنسيق ملف RAR المقدم في الإصدار 5.0 هو كما يلي:

| تنسيق الملف
---|
| وحدة الاستخراج الذاتي (اختياري)
| توقيع RAR 5.0
| عنوان تشفير الأرشيف (اختياري)
| رأس الأرشيف الرئيسي
| أرشفة عنوان خدمة التعليقات (اختياري)
رأس الملف 1
| رؤوس الخدمة (NTFS ACL ، التدفقات ، إلخ) للملف السابق (اختياري)
| ...
| رأس الملف ن
| رؤوس الخدمة (NTFS ACL ، التدفقات ، إلخ) للملف السابق (اختياري)
| سجل الاسترداد (اختياري)
| نهاية رأس الأرشيف

يمكن العثور على معلومات حول كل قسم من ملف RAR المذكور أعلاه في مستند [مواصفات تنسيق ملف RAR 5.0](https://www.rarlab.com/technote.htm#arcstruct).

#### الاستخراج الذاتي لأرشيفات RAR

إذا كان ملف RAR نفسه يتم استخراجه ذاتيًا ، فسيتم احتواء معلومات الاستخراج الذاتي في بداية الملف الذي يسبق توقيع الأرشيف. لم يتم تعريف حجمها ومحتوياتها.

#### توقيع RAR 5.0

توقيع RAR هو رأس 8 بايت يتكون من الرقم السحري التالي:

0x 52 61 72 21 1A 07 00

أين

0x6152 - HEAD_CRC

0x72 - HEAD_TYPE

0x1A21 - HEAD_FLAGS

0x0007 - HEAD_SIZE

## مراجع

* [تنسيق أرشيف RAR 5.0](https://www.rarlab.com/technote.htm)
* [RAR - بواسطة Wikipedia](https://en.wikipedia.org/wiki/RAR_ (file_format))
