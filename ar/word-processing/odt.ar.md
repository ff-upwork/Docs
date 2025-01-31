{
  "date" : "2019-10-11",
  "keywords" :["odt file", "odt file format", "what is a odt file", "file", "odt example", "odt file extension", "extension", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"ODT - ملف نصي OpenDocument" ,
  "description":"تعرف على تنسيق ملف ODT وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات ODT وفتحها." ,
  "linktitle" : "ODT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
} ,
  "lastmod" : "2019-09-10"
}

## ما هو ملف ODT؟

ملفات ODT هي نوع من المستندات التي يتم إنشاؤها باستخدام تطبيقات معالجة الكلمات التي تستند إلى تنسيق OpenDocument Text File. يتم إنشاؤها باستخدام تطبيقات معالج الكلمات مثل OpenOffice Writer ويمكنها الاحتفاظ بمحتوى مثل النص والصور والكائنات والأنماط. ملف ODT هو لـ Writer معالج النصوص مثل [DOCX](/ar/word-processing/ docx /) لبرنامج Microsoft Word. يمكن للعديد من التطبيقات ، بما في ذلك محرّر مستندات Google ومعالج النصوص المستند إلى الويب من Google والمضمن في Google Drive ، فتح ملفات ODT للتحرير. يمكن لـ Microsoft Word أيضًا فتح ملفات ODT وحفظها بتنسيقات أخرى مثل [DOC](/ar/word-processing/ doc /) و DOCX.

## نبذة تاريخية ##

تعتمد مواصفات تنسيق ملف ODP على المعيار الذي تم تطويره كمواصفات ODF. تطورت هذه المواصفات على شكل ثلاث نسخ تم تطويرها ونشرها من قبل OASIS على النحو التالي:

** 2005 ** تم نشر الإصدار 1.0 في مايو 2005

** 2007: ** تم نشر الإصدار 1.1 في فبراير 2007

** 2011: ** تم نشر الإصدار 1.2 في سبتمبر 2011

كانت هناك تغييرات طفيفة جدًا في الانتقال من إصدارات ODF 1.0 إلى 1.1. [الإصدار 1.2 من ODF](https://www.oasis-open.org/standards#opendocumentv1.2) هو أحدث إصدار لمواصفات ODF ويجب أن يستشيره المطورون لتطوير التطبيقات المتعلقة بقراءة / كتابة نظام الوثائق الرسمية.

## مواصفات تنسيق الملف ##

يدعم تنسيق OpenDocument تمثيل المستند كمستند XML واحد بالإضافة إلى مجموعة من العديد من المستندات الثانوية داخل حزمة كأرشيف [ZIP](/ar/compression/zip/). يخزن كل ملف من أرشيف ZIP جزءًا من المستند الكامل. يخزن كل مستند ثانوي جانبًا معينًا من المستند. على سبيل المثال ، يحتوي مستند ثانوي على معلومات النمط ويحتوي مستند ثانوي آخر على محتوى المستند. يحتوي مستند ODF النموذجي على المكونات التالية:

* content.xml - محتوى المستند والأنماط التلقائية المستخدمة في المحتوى.
* styles.xml - الأنماط المستخدمة في محتوى المستند والأنماط التلقائية المستخدمة في الأنماط نفسها.
* meta.xml - معلومات تعريف المستند ، مثل المؤلف أو وقت إجراء الحفظ الأخير.
* settings.xml - الإعدادات الخاصة بالتطبيق ، مثل حجم النافذة أو معلومات الطابعة.

بالإضافة إلى ذلك ، يمكن أن تحتوي الحزمة على العديد من المستندات الثانوية الأخرى مثل الصورة المصغرة للمستند ، والصور ، وما إلى ذلك. ملفات المستندات هي المجموعة الفرعية لملفات ODF حيث يتم تخزين المحتوى (الأوراق) في //content.xml// مستند ثانوي.

## مراجع ##

* [OpenDocument - بواسطة Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

