{
  "date" : "2022.01.31",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"ملف P7S - رسالة بريد إلكتروني موقعة رقمياً" ,
  "description":"تعرف على تنسيق ملف P7S وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات P7S وفتحها." ,
  "linktitle" : "P7S",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
} ,
  "lastmod" : "2022.01.31"
}

## ما هو ملف P7S؟

ملف P7S هو توقيع رقمي يتم استلامه بواسطة بريد إلكتروني موقّع رقميًا. إن وجود هذا الملف كمرفق مع البريد الإلكتروني يؤكد أن البريد الإلكتروني تم إرساله من مصدر موثوق. هذا يضمن أن المرسل لديه شهادة توقيع بريد إلكتروني مثبتة على جهاز الكمبيوتر الخاص به. عندما يتم إرسال مثل هذا البريد الإلكتروني الموقع من كمبيوتر المستخدم ، يتم إرفاق ملف P7S به الذي يحتوي على اسم المرسل. يمكن لعملاء البريد الإلكتروني الذين يدعمون رسائل البريد الإلكتروني الموقعة رؤية معلومات المرسل.

## تنسيق ملف P7S - مزيد من المعلومات

تحتوي ملفات P7S S / MIME (ملحقات بريد الإنترنت الآمن / متعدد الأغراض) على المعلومات بتنسيق نص عادي يمكن قراءته بواسطة الإنسان. يدعم عملاء البريد الإلكتروني مثل Microsoft Outlook و Apple Mail و Mozilla Thunderbird لقراءة المعلومات الموقعة رقميًا من بريد إلكتروني S / MIME. يتحقق التوقيع على بريد إلكتروني من هوية المرسل ويخبر المستلم أن الرسالة أصلية. عند تنزيل رسائل البريد الإلكتروني من عملاء البريد الإلكتروني (إما كـ [EML](/ar/ email / eml /) أو [MSG](/ar/ email / msg /)) ، يتم العثور على ملفات P7S مرفقة مع رسائل البريد الإلكتروني هذه.

يحتوي ملف P7S على المعلومات التالية:

* مصدر أصل البريد الإلكتروني
* تاريخ ووقت إرسالها ،
* ما إذا كان قد تم تعديله أثناء الإرسال

يتم تضمين هذه المعلومات باستخدام تقنية تشفير المفتاح العام رقم 7 (PKCS7) لإرفاق التوقيعات المشفرة بالبريد الإلكتروني رقميًا.

## مراجع ##

* [أداة تسجيل Microsoft](https://docs.microsoft.com/en-us/windows-hardware/drivers/devtest/signtool)
