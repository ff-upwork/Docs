{
  "date" : "2019-10-11",
  "keywords" :["ملف qlr" , "تنسيق ملف qlr" , "ما هو ملف qlr" , "ملف" , "qlr مثال" , "امتداد ملف qlr" , "امتداد" , "تنسيق"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"ملف تعريف طبقة QLR - QGIS" ,
  "description":"تعرف على تنسيق ملف QLR وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات QLR وفتحها." ,
  "linktitle" : "QLR",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
} ,
  "lastmod" : "2021-03-14"
}

## ما هو ملف QLR؟

الملف الذي يحتوي على .qlr هو ملف تعريف الطبقة الذي يحتوي على مؤشر لمصدر بيانات الطبقة. هذا بالإضافة إلى معلومات نمط [QGIS](https://www.qgis.org/en/site/) للطبقة. وجود مراجع لجميع الأنماط ذات الصلة ، يتم استخدام هذا الملف كمصدر واحد للبيانات لاستخدامها في الحصول على معلومات التصميم. باستخدام ملفات QLR ، يمكن وضع المعلومات الخاصة بمصادر البيانات في هذا الملف الفردي الذي يمكن قراءته بواسطة التطبيقات الأخرى لتحميل معلومات التصميم. يمكن فتح ملفات QLR باستخدام أي محرر نصوص مثل Notepad ++.

## تنسيق ملف QLR

QLR ، على غرار [QGS](/ar/ gis / qgs /) ، هو ملف XML يحتوي على مؤشرات لمصدر بيانات الطبقة في شكل علامات XML. إنه مشابه لملف ArcGIS .lyr. علامات المستوى الأعلى لملف QML موضحة في الصورة أدناه.

{{< figure src="../qlr.png" title="" >}}

## مراجع

* [QGIS](https://www.qgis.org/en/site/)
* [QLR](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)
