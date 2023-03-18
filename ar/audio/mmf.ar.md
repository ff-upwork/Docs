{
  "date" : "2021-08-09",
  "keywords" :["mmf", "file", "extension", "format", "audio", "smaf", "mmf extension", "mmf files", "mobile music file", "yamaha"],
  "author" : {
    "display_name" : "Sami Cheema"
} ,
  "draft" : "false",
  "toc" : true,
  "description" :"تعرف على تنسيق ملف MMF وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات MMF وفتحها." ,
  "title" :"MMF - تنسيق ملف الموسيقى المحمول" ,
  "linktitle" : "MMF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
} ,
  "lastmod" : "2021-08-09"
}

## ما هو ملف MMF؟

MMF هو امتداد ملف مرتبط بملف SMAF. يرمز MMF إلى Mobile Music File بينما يرمز SMAF إلى تنسيق تطبيق الهاتف المحمول للموسيقى الاصطناعية. تحتوي ملفات MMF الموجودة في الهاتف الذكي على نغمات رنين وصوت ويمكن أن تحتوي أيضًا على رسومات وعرض نص. يحتوي MMF أيضًا على ثلاثة أنواع من معلمات الأداة بما في ذلك FM و PCM و Stream PCM. تتوافق تنسيقات الملفات هذه مع نظام Windows الأساسي. يتم تصنيف ملفات MMF كملفات بيانات. عادةً ما يدعم Microsoft Mail ملفات MMF. يمكن نسخ الملف الذي يحتوي على لاحقة MMF إلى أي جهاز محمول أو نظام أساسي.

علاوة على ذلك ، فإن حجم هذه الملفات أصغر بكثير مقارنة بملفات تنسيق MIDI القياسية. يمكن تحويل ملفات [WAV](/ar/ audio / wav /) و [MID](/ar/ audio / mid /) إلى تنسيق MMF الذي يمكن مشاركته وتوزيعه كمحتوى صوتي. يمكن استلام هذه الملفات عبر البريد الإلكتروني مباشرة إلى الهواتف وأجهزة الكمبيوتر.


## تاريخ موجز لتنسيق ملف MMF

طورت Yamaha أدوات SMAF كملفات صوتية بحيث يمكن للهواتف الذكية تخزين عدد أكبر من نغمات الرنين الفريدة. قدمت Yamaha SMAF بإنتاج رقائق الصوت MA-1 و MA-2 و MA-3 و MA-5 و MA-7 LSI. أصبحت كل هذه التنسيقات مألوفة تمامًا بين الهواتف المحمولة في سوق شرق آسيا خلال أوائل عام 2000.

على المستوى الدولي ، تمت الموافقة على تنسيق MMF من قبل Samsung. بمساعدة تنسيق MMF ، تمكنت Samsung من تصميم مجموعة واسعة من نغمات الرنين متعددة الألحان لاستخدامها في هواتف Samsung الذكية.

أرادت Yamaha جعل التنسيق أكثر شيوعًا وهكذا في ملفات Yamaha SMAF الرسمية ، قامت بنشر المزيد من الأدوات المتوافقة مع هذا التنسيق. مع هذا يمكن للمستخدمين الآن بسهولة تشغيل ملفات MMF على أجهزة الكمبيوتر الخاصة بهم.


## مواصفات تنسيق ملف MMF ##

يتم تصنيف ملفات MMF إلى أقسام البيانات. يتم استخدام بنية مسبوقة حول 8 بايت لوصف كل مقطع.
يشتمل الملصق المكون من 4 بايت على CNTI و OPDA و MSTR و MTR و ATR. حجم البيانات زائد 8 بايت هو حجم القطعة ؛ يتم حساب حجم الملف بالكامل عن طريق جمع كل أحجام المقاطع. إذا لم يتم إتلاف الملف ، يجب أن يكون حجم الملف المجمع هو نفس حجم الرأس الأساسي.

### العنوان ###

```
struct SMAF_Header
{
    uint32   SignatureMMMD;     // Signature: "MMMD"
    uint32   SizeSMAF;      // 4 byte data size, big-endian order
};
```

فيما يلي مثال على ملف MMF:

![](../mmf.png)

## مراجع

* [MMF - بواسطة Wikipedia](https://en.wikipedia.org/wiki/Synthetic_music_mobile_application_format)
