{
  "date" : "2019-12-10",
  "keywords" :["DIF", "file", "extension", "file format", "Data Interchange File", "Spreadsheet"],
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "description" :"دليل تنسيق الملف الخاص بك لمعرفة ما هو امتداد ملف DIF وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات DIF وفتحها." ,
  "title" :"DIF - تنسيق ملف تبادل البيانات" ,
  "linktitle" : "DIF",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
} ,
  "lastmod" : "2019-12-10"
}

## ما هو ملف DIF؟

يرمز DIF إلى تنسيق تبادل البيانات المستخدم لاستيراد / تصدير بيانات جداول البيانات بين التطبيقات المختلفة. وتشمل هذه Microsoft Excel و OpenOffice Calc و StarCalc وغيرها الكثير. يقوم بتخزين البيانات الموجودة في جدول بيانات واحد وهو القيد الوحيد لتنسيق الملف هذا.

## تاريخ موجز لتنسيق ملف DIF ##

تم تطوير تنسيق ملف DIF بواسطة شركة Software Arts، Inc. في أوائل الثمانينيات. تم تضمين مواصفات تنسيق الملف لـ DIF في VisiCalc الذي كان أول برنامج جداول بيانات لأجهزة الكمبيوتر الشخصية. هذه المواصفات محمية بحقوق الطبع والنشر في عام 1981 وكانت علامة تجارية مسجلة لشركة Software Arts Products Corp.

## تنسيق ملف DIF ##

يقوم DIF بتخزين محتويات جدول البيانات في ملف نصي ASCII يسمح بعرضها وتحريرها باستخدام محرر نصوص. يحتل التنسيق مكانه في قائمة تنسيقات تسلسل البيانات لخصائصه في تبادل البيانات. يتكون ملف DIF من قسمين ؛ رأس والبيانات.

يتم تمثيل كل شيء في DIF بقطعة مكونة من 2 أو 3 أسطر. تحصل الرؤوس على مقطع مكون من 3 أسطر ؛ البيانات ، 2.

* تبدأ أجزاء الرأس بمعرف نص يتكون من أحرف استهلالية كاملة وأحرف أبجدية فقط وأقل من 32 حرفًا. يجب أن يكون السطر التالي عبارة عن زوج من الأرقام ، ويجب أن يكون السطر الثالث عبارة عن سلسلة مقتبسة.
* تبدأ قطع البيانات بزوج أرقام والسطر التالي عبارة عن سلسلة مقتبسة أو كلمة رئيسية.

### قيم ###

تحتل القيمة سطرين ، الأول زوج من الأرقام والثاني إما سلسلة أو كلمة أساسية. يشير الرقم الأول من الزوج إلى النوع:

* −1 - نوع التوجيه ، يتم تجاهل الرقم الثاني ، السطر التالي هو أحد هذه الكلمات الأساسية:
** BOT - بداية الصف (بداية الصف)
** التخلص من الذخائر المتفجرة - نهاية البيانات
* 0 - نوع رقمي ، القيمة هي الرقم الثاني ، السطر التالي هو أحد هذه الكلمات الرئيسية:
** V - صالح
** غير متوفر - غير متوفر
** خطأ - خطأ
** TRUE - قيمة منطقية حقيقية
** FALSE - قيمة منطقية خاطئة
* 1 - نوع السلسلة ، يتم تجاهل الرقم الثاني ، والسطر التالي هو السلسلة بين علامتي اقتباس

### قطعة رأس DIF ###

يتكون مقطع الرأس لملف DIF من سطر معرف متبوعًا بسطرين من القيمة. تستخدم القيم الرقمية في أجزاء الرأس سلسلة فارغة فقط بدلاً من الكلمات الأساسية الصالحة. فيما يلي تفاصيل أجزاء الرأس هذه.

* TABLE - تتبع القيمة الرقمية للإصدار ، يحتوي السطر الثاني غير المستخدم من القيمة على تعليق منشئ
* المتجهات - يتبع عدد الأعمدة كقيمة عددية
* TUPLES - يتبع عدد الصفوف كقيمة عددية
* البيانات - بعد القيمة الرقمية 0 الوهمية ، تتبع بيانات الجدول ، كل صف يسبقه قيمة BOT ، وينتهي الجدول بأكمله بقيمة EOD

### مثال DIF ###

يوضح المثال التالي محتويات ورقة عمل بسيطة وتمثيل DIF المكافئ لها.


| الاسم | العمر
---|---|
| بوب | 34
| شيتال | 22

```
TABLE
0,1
"EXCEL"
VECTORS
0,3
""
TUPLES
0,2
""
DATA
0,0
""
-1,0
BOT
1,0
"Name"
1,0
"Age"
-1,0
BOT
1,0
"Bob"
0,34
V
-1,0
BOT
1,0
"Sheetal"
0,22
V
-1,0
EOD
```

## مراجع ##

* [DIF - بواسطة Wikipedia](https://en.wikipedia.org/wiki/Data_Interchange_Format)
