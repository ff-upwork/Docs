{
  "date" : "2021-06-16",
  "keywords" :["LZO" , "مضغوط" , "ملف" , "امتداد" , "تنسيق الملف" , "Lempel-Ziv-Oberhume"] ,
  "author" : {
    "display_name" : "Sami Cheema"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف LZO" ,
  "description":"تعرف على تنسيق ملف LZO وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات LZO وفتحها." ,
  "linktitle" : "LZO",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
} ,
  "lastmod" : "2021-06-16"
}

## ما هو ملف LZO؟ ##

يتم دمج ملف بامتداد .lzo مع ميزات أرشفة الملفات التي يمكن أن تقلل حجم جميع الملفات في الملف المضغوط. قد تشتمل جميع الملفات المضغوطة على ملف واحد أو أكثر أو حتى مجموعات من المجلدات مع ملفات متعددة من أنواع وأبعاد مختلفة. حجم الملف المضغوط أصغر مقارنة بالحجم المشترك لجميع الملفات والمجلدات المخزنة في ملف مضغوط LZO. يتم تخزين جميع ملفات LZO المضغوطة بتنسيق LZO ويتم تنفيذها بشكل صريح باستخدام ميزات الضغط التي يستخدمها برنامج ضغط وفك ضغط الملفات LZOP. يتم دمج جميع مواصفات الضغط في برنامج ضغط وفك ضغط الملفات هذا الذي نشأ من مكتبة ضغط الملفات Lempel-Ziv-Oberhume. يتم أيضًا دمج سرعة فك الضغط الأسرع ونسب الضغط المتقدمة في ملفات LZO هذه.

## مواصفات LZO ##

قام ماركوس فرانز زافير يوهانس أوبرهومر بتطوير خوارزمية "lzop" الأصلية ، بناءً على خوارزميات سابقة قام بها أبراهام ليمبل وجاكوب زيف ، في عام 1996. تطبق هذه المكتبة مجموعة متنوعة من الخوارزميات بالخصائص التالية:

* ضغط أسرع من DEFLATE
* تخفيف الضغط السريع
* مخازن مؤقتة إضافية مطلوبة أثناء الضغط (بحجم 8 كيلو بايت أو 64 كيلو بايت ، اعتمادًا على مستوى الضغط)
* المخازن المؤقتة للمصدر والوجهة هي كل الذاكرة المطلوبة لفك الضغط
* يوفر التحكم في كل من نسبة الضغط وسرعة الضغط

بصفتها خوارزمية لضغط الكتلة ، تقوم LZO بتنفيذ ضغط متداخل بالإضافة إلى فك الضغط في الموضع. لتحقيق ضغط متداخل ، يجب أن يتطابق حجم الكتلة لكل من الضغط وإلغاء الضغط. تقوم خوارزمية ضغط LZO بتقسيم بيانات الإدخال إلى مطابقات (قاموس منزلق) وحرفية غير متطابقة ، مما يعطي نتائج جيدة مع بيانات زائدة عن الحاجة ونتائج مقبولة مع بيانات غير قابلة للضغط ، ويزيد فقط البيانات غير القابلة للضغط بمقدار 1/64 من الأصل بحجم.

## مشاكل في فتح ملف LZO ##

فيما يلي بعض المشكلات التي قد تتسبب في ضعف عمل تنسيق ملف LZO:
  


* قد يكون الملف تالفًا. لحل هذه المشكلة ، قم بتنزيل الملف مرة أخرى أو اطلب من المرسل إعادة إرسال الملف مرة أخرى
* السبب الثاني هو إصابة الملف في هذه الحالة بفحص الملف بشكل صحيح
* روابط غير صحيحة إلى ملف LZO
* إزالة وصف LZO
* لا توجد موارد أجهزة كافية
* السائقين الذين عفا عليهم الزمن للمعدات
  


## مراجع ##

* [LZO - بواسطة Wikipedia](https://en.wikipedia.org/wiki/Lempel٪E2٪80٪93Ziv٪E2٪80٪93Oberhumer)
