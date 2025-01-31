{
  "date" : "2019-10-11",
  "keywords" :["ملف gz" , "تنسيق ملف gz" , "ما هو ملف gz" , "ملف" , "مثال gz" , "امتداد ملف gz" , "امتداد" , "تنسيق"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف GZ - ملف أرشيف جنو مضغوط" ,
  "description":"تعرف على ما هو ملف GZ وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات GZ وفتحها." ,
  "linktitle" : "GZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
} ,
  "lastmod" : "2019-09-10"
}

## ما هو ملف GZ؟

ملف GZ هو أرشيف مضغوط يتم إنشاؤه باستخدام خوارزمية الضغط القياسية [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip). قد يحتوي على العديد من الملفات المضغوطة والدلائل وأوتار الملفات. تم تطوير هذا التنسيق في البداية ليحل محل تنسيقات الضغط على أنظمة UNIX. ولا يزال أحد أكثر أنواع الأرشيفات شيوعًا على أنظمة Linux. يمكن لتطبيقات مثل [WinZip](https://www.winzip.com/en/) فتح ملفات GZ لعرض محتوياتها على كل من Windows و MacOS.

## تنسيق ملف GZ - مزيد من المعلومات

يستخدم Gzip خوارزمية [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) لضغط الأرشيف ويختلف عن تنسيق الأرشيف [ZIP](/ar/compression/zip/) في تطبيق خوارزمية الضغط على أرشيف كامل بدلا من الملفات الفردية. يحتوي الإصدار 4.3 من مواصفات تنسيق ملف GZIP المنشور بواسطة فريق مهام هندسة الإنترنت (IETF) على معلومات مفصلة حول تنسيق الملف. يتكون تنسيق الملف من:

* رأس الملف
* رؤوس اختيارية
* بيانات مضغوطة
* تذييل الملف

## رأس ملف GZ ##

يتكون رأس ملف GZ من 10 بايت على النحو التالي:

| الإزاحة | الحجم | القيمة | الوصف
---|---|---|---|
| 0 | 2 | 0x1f 0x8b | نوع ملف تعريف الرقم السحري
| 2 | 1 | | طريقة الضغط * 0-7 (محجوز) * 8 (انكماش)
| 3 | 1 | | ملف الأعلام
| 4 | 4 | | طابع زمني 32 بت
| 8 | 1 | | ضغط الأعلام
| 9 | 1 | | معرف نظام التشغيل

### أعلام الملفات ###

| القيمة | المعرف | الوصف
---|---|---|
| 0x01 | FTEXT | إذا تم تعيين البيانات غير المضغوطة ، فيجب معاملتها كنص بدلاً من بيانات ثنائية. تشير هذه العلامة إلى تحويل نهاية السطر للملفات النصية عبر الأنظمة الأساسية ولكنها لا تفرضها.
| 0x02 | FHCRC | يحتوي الملف على مجموع اختباري للرأس (CRC-16)
| 0x04 | FEXTRA | يحتوي الملف على حقول إضافية
| 0x08 | FNAME | يحتوي الملف على سلسلة اسم الملف الأصلي
| 0x10 | FCOMMENT | يحتوي الملف على تعليق
| 0x20 | | محجوز
| 0x40 | | محجوز
| 0x80 | | محجوز

### نظام التشغيل ###

| القيمة | الوصف
---|---|
| 0 | نظام ملفات FAT (MS-DOS ، OS / 2 ، NT / Win32)
| 1 | أميغا
| 2 | VMS (أو OpenVMS)
| 3 | يونكس
| 4 | VM / CMS
| 5 | Atari TOS
| 6 | نظام ملفات HPFS (OS / 2 ، NT)
| 7 | ماكنتوش
| 8 | نظام Z
| 9 | CP / M.
| 10 | TOPS-20
| 11 | نظام ملفات NTFS (NT)
| 12 | QDOS
| 13 | البلوط RISCOS
| 255 | غير معروف

## رؤوس اختيارية GZ ##

الرؤوس الإضافية الاختيارية هي تلك التي يتم الإشارة إليها بواسطة أعلام الملف وتتضمن معلومات مثل اسم الملف الأصلي والحقول الإضافية والتعليقات والمجموع الاختباري للرأس.

## بيانات مضغوطة ##

يحتوي هذا القسم على البيانات المضغوطة باستخدام خوارزمية ضغط DEFLATE.

## تذييل ملف GZ ##

حجم تذييل الملف 8 بايت ويحتوي على المعلومات التالية.

| الإزاحة | الحجم | الوصف
---|---|---|
| 0 | 4 | المجموع الاختباري (CRC-32)
| 4 | 4 | قيمة حجم البيانات غير المضغوطة بالبايت

## مراجع ##

* [gzip - ويكيبيديا](https://en.wikipedia.org/wiki/Gzip)
* [RFC1952: مواصفات تنسيق ملف GZIP](https://datatracker.ietf.org/doc/html/rfc1952) ، بواسطة IETF.

