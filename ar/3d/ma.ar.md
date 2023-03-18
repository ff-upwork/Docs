{
  "date" : "2019-10-11",
  "keywords" :["ma", "ma file", "ma file format", "file format", "3d", "ma file download", ".ma file", ".ma"],
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "description":"تعرف على تنسيق ملف MA وواجهات برمجة التطبيقات التي يمكنها فتح وإنشاء ملفات MA." ,
  "title" :"تنسيق ملف MA" ,
  "linktitle" : "MA",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
} ,
  "lastmod" : "2021-06-04"
}

## ما هو ملف MA؟

الملف بامتداد .ma هو ملف مشروع ثلاثي الأبعاد تم إنشاؤه باستخدام تطبيق Autodesk Maya. يحتوي على قائمة كبيرة من الأوامر النصية لتحديد معلومات حول الملف. يمكن فتح ملف **. ma ** وتحريره في أي محرر نصوص لإصلاح أي مشكلات في الأوامر في حالة تلف أحد الملفات. تحتوي هذه الملفات على معلومات لتحديد معلومات المشهد ثلاثي الأبعاد مثل الهندسة والإضاءة والرسوم المتحركة والعرض.

## تنسيق ملف MA

يتم حفظ ملفات MA على القرص بتنسيق نصي ASCII بخلاف ملفات MB التي يتم حفظها بتنسيق ملف ثنائي على القرص. يتوفر مرجع مفصل لتنسيق ملف MA في [Autodesk Maya Documentation](https://download.autodesk.com/us/maya/2010help/index.html؟url=Glossary_M_ma_file_format.htm،topicNumber=d0e192001) ويمكن الرجوع إليه كمرجع للمطور.

### رأس ملف MA

يبدأ رأس ملف MA بقسم من التعليقات يعطي معلومات إنشاء الملف وتاريخ التعديل. يتجاهل قراء ملفات Maya هذه الكتلة لأنها تستخدم فقط لغرض المعلومات فقط. يجب أن يبدأ العنوان بأول ستة أحرف مثل "// Maya" بالرغم من ذلك.

يبدو رأس ملف ASCII كما يلي.

```
//Maya ASCII 1.0 scene
//Name: solstice.ma
//Last modified: Sun, Dec 21, 97 10:18:26 AM
```
### مراجع الملف

يحتوي قسم مراجع الملف في ملف .ma على معلومات حول كافة ملفات Maya الأخرى التي يتم الرجوع إليها في هذا الملف. يمكن قراءة كل ملف مرجعي باستخدام أمر ملف واحد موجود في نفس الملف. بناء جملة الأمر file عند استخدامه للإشارة هو:

```
file -r -rpr prefixString fileName;
```
أو

```
file -r -ns nameSpace fileName
```
هنا مثال على سلسلة.

```
file -r -rpr "solar" "/u/sally/work/solar.ma";
```
يوضح هذا المثال أن كائن الشمس الموجود في الملف `solar` يمكن الوصول إليه في هذا الملف باستخدام الاسم" solar_sun ".

### متطلبات

يتكون قسم المتطلبات في ملف .ma من سلسلة من الأوامر المطلوبة ويخبر معلومات مايو مثل معلومات الإصدار والإضافات المطلوبة لقراءة الملفات. مثال على قسم المتطلبات على النحو التالي.

```
requires maya "2.0";
requires specialPlugIn "1.2";
```


القسم التالي يحدد المتطلبات. يتكون هذا من سلسلة من أوامر يتطلب. يخبر هذا القسم من الملف Maya بالبرنامج المطلوب لتحميل الملف بشكل صحيح. على وجه التحديد ، ما هو إصدار Maya ، وما المكونات الإضافية.

## تحميل ملف MA
من الصعب بعض الشيء العثور على ملف MA الخاص بنموذج ثلاثي الأبعاد وتنزيله. لذلك ، يمكنك تنزيل نموذج ملف MA من هنا:

- [Sample.ma](../ sample.ma)


## مراجع

* [تنظيم ملفات Maya ASCII - Autodesk](https://download.autodesk.com/us/maya/2010help/index.html؟url=Glossary_M_ma_file_format.htm،topicNumber=d0e192001)
