{
  "date" : "2021-03-01",
  "author" : {
    "display_name" : "Muhammad Umar"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"RDL - ملف لغة تعريف التقرير" ,
  "keywords" :["rdl" , "لغة تعريف التقرير" , "XmlTextWriter" , "XSD" , "عنصر RDL"] ,
  "description":"تعرف على تنسيق ملف RDL وهو تمثيل XML لتعريف تقرير SQL Server Reporting Services." ,
  "linktitle" : "RDL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
} ,
  "lastmod" : "2021-03-01"
}

## ما هو ملف RDL؟ ##

RDL (لغة تعريف التقرير) هي معيار معياري وضعته Microsoft لتحديد التقارير. يتكون ملف RDL من عنصر RDL واحد أو أكثر. في حين أن عنصر RDL يتكون من نوع بياناته وأصله. يمكن أن يكون العنصر بسيطًا أو معقدًا. لا يحتوي العنصر البسيط على أي عنصر أو سمات فرعية ، في حين أن العنصر المعقد لا يحتوي على عناصر فرعية وسمات اختيارية.

## تعريف مخطط XML لـ RDL
يتحقق ملف تعريف مخطط XML (XSD) من صحة ملف RDL. يحدد المخطط القواعد الخاصة بأماكن ظهور عناصر RDL في ملف .rdl. يمكن أن يكون عنصر RDL بسيطًا أو معقدًا. لا يحتوي العنصر البسيط على عناصر فرعية أو سمات ، ولا يحتوي العنصر المعقد على عناصر فرعية وخواص اختيارية.

## إنشاء RDL
نظرًا لأن RDL مفتوح وقابل للتوسيع بطبيعته ، يمكن إنشاء العديد من التطبيقات والأدوات التي تنشئ ملفات RDL بناءً على مخطط XML الخاص بها. تتمثل إحدى أبسط الطرق لإنشاء RDL من أحد التطبيقات في استخدام فئات Microsoft .NET Framework من مساحة الاسم ** System.Xml ** ومساحة الاسم System.Linq. على وجه الخصوص ، يمكن استخدام فئة ** XmlTextWriter ** لكتابة RDL. يمكنك إنشاء تعريف تقرير كامل من البداية إلى النهاية في أي تطبيق .NET Framework باستخدام ** XmlTextWriter **. يمكن للمطورين أيضًا إضافة عناصر تقرير مخصصة بخصائص مخصصة لتوسيع RDL.

## أنواع RDL
يسرد الجدول التالي الأنواع والسمات المستخدمة في عناصر RDL.

| النوع | الوصف |
---|---|
| ثنائي | خاصية ذات قيمة ثنائية مشفرة بالأساس 64. |
| منطقي | خاصية مع صواب أو خطأ كقيمة للكائن. ما لم يتم تحديد خلاف ذلك ، فإن قيمة الكائن المنطقي الاختياري المحذوف هي False. |
| التاريخ | خاصية ذات تاريخ محدد بالكامل أو قيمة تاريخ ووقت محدد بتنسيق التاريخ ISO8601: YYYY-MM-DD [THH: MM [: SS [.S]]].
| تعداد | خاصية ذات قيمة نصية لسلسلة يجب أن تكون واحدة من قائمة القيم المعينة. |
| تعويم | خاصية ذات قيمة عائمة. النقطة (.) تستخدم كفاصل عشري اختياري. |
| عدد صحيح | خاصية ذات قيمة عدد صحيح (int32). |
| اللغة | خاصية ذات قيمة نصية تحتوي على رمز لغة وثقافة ، مثل "en-us" للغة الإنجليزية الأمريكية. يجب أن تكون القيمة إما لغة معينة أو لغة محايدة يتم تحديد لغة افتراضية لها في Microsoft .NET Framework
| الاسم | خاصية ذات قيمة نصية لسلسلة. يجب أن تكون الأسماء فريدة داخل مساحة اسم العنصر. إذا لم يتم تحديده ، فإن مساحة الاسم الخاصة بالعنصر هي الكائن الأعمق الذي يحتوي على اسم. |
| NormalizedString | خاصية ذات قيمة نصية لسلسلة تم تسويتها. |
| الحجم | يجب أن يحتوي عنصر الحجم على رقم (مع استخدام حرف نقطة كفاصل عشري اختياري). يجب أن يتبع الرقم محددًا لوحدة طول CSS مثل cm أو mm أو in أو pt أو pc. المسافة بين الرقم والمميز اختيارية. لمزيد من المعلومات حول مصممي الحجم ، راجع مرجع الوحدات وقيم CSS. في RDL ، الحد الأقصى لقيمة الحجم هو 160 بوصة. الحد الأدنى للحجم هو 0 بوصة.
| سلسلة | خاصية ذات قيمة نصية لسلسلة. |
| UnsignedInt | خاصية ذات قيمة عدد صحيح بدون إشارة (uint32). |
| المتغير | خاصية بأي نوع XML بسيط. |

## أنواع بيانات RDL
في RDL ، يحدد تعداد نوع البيانات نوع بيانات السمة أو التعبير أو المعلمة. يوضح الجدول التالي كيف تتوافق أنواع بيانات CLR مع أنواع بيانات RDL.

| أنواع CLR | نوع البيانات المقابلة |
---|---|
| منطقي | منطقي |
| DateTime ، DateTimeOffset | DateTime |
| Int16 ، Int32 ، UInt16 ، بايت ، SByte | عدد صحيح |
| مفرد ، مزدوج | عائم |
| String، Char، GUID، Timespan | سلسلة |


## مراجع ##

- [لغة تعريف التقرير (ويكيبيديا)](https://en.wikipedia.org/wiki/Report_Definition_Language)
- [لغة تعريف التقرير (SSRS)](https://learn.microsoft.com/en-us/sql/reporting-services/reports/report-definition-language-ssrs)

