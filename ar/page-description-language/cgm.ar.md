{
  "date" : "2019-10-11",
  "keywords" :["CGM" , "Computer Graphics Metafile" , "File" , "Extension" , "File Format" , "Vector Graphics" , "Metafile Descriptor"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف CGM",
  "description":"تعرف على تنسيق ملف CGM وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات CGM وفتحها." ,
  "linktitle" : "CGM",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
} ,
  "lastmod" : "2021-04-23"
}

## ما هو ملف CGM؟ ##

Computer Graphics Metafile (CGM) هو تنسيق ملف تعريف قياسي دولي مجاني ومستقل عن النظام الأساسي لتخزين وتبادل الرسومات المتجهة (2D) والرسومات النقطية والنص. يستخدم CGM نهجًا موجهًا للكائنات والعديد من أحكام الوظائف لإنتاج الصور. تستخدم CGM هذه الخصائص الموجهة للكائنات لإعادة تشكيل العناصر الرسومية لتقديم صورة. يحتوي ملف التعريف على المعلومات الضرورية التي تعرّف الملفات الأخرى. في CGM ، يحتوي الملف المصدر المستند إلى النص على جميع العناصر الرسومية التي يمكن تجميعها لاحقًا في ملف ثنائي. في الأساس ، تعد CGM طريقة لتسهيل تبادل البيانات الرسومية ثنائية الأبعاد ، بشكل مستقل عن أي منصة أو جهاز معين.

يوفر تنسيق CGM عناصر مختلفة لأداء الوظائف ، والدلالة على الكائنات لضبط العناصر الأولية الهندسية والمعلومات الرسومية. على الرغم من أن CGM قد حلت محلها تنسيقات أخرى لعرض الفنون الرسومية على صفحات الويب لأنها لا تدعمها صفحات الويب جيدًا ، إلا أنها لا تزال تحظى بشعبية كبيرة بين التطبيقات الصناعية والطيران والتطبيقات التقنية الأخرى. على الرغم من قيام World Wide Web Consortium بتطوير WebCGM ، وهو نهج بديل لاستخدام CGM على الويب. كان تنفيذ CGM الأساسي توضيحًا لتسلسل العمليات الأساسية لنظام الجرافيك Kernel (GKS). لم يتم اعتماده كثيرًا في التصميمات الاحترافية ولكن تم استبداله إلى حد كبير بتنسيقات أخرى مثل DXF و SVG.

## تاريخ ##

تحولت CGM إلى معيار دولي في عام 1987 (ISO 8632-1987) وتم اعتمادها أيضًا كمعيار وطني في المملكة المتحدة من قبل BSI والولايات المتحدة الأمريكية بواسطة ANSI. بعد عدد من التعديلات في عام 1991 ، تم إصدار معيار منقح لـ CGM في عام 1992 (ISO 8632: 1992). في عام 2001 ، طور اتحاد شبكة الويب العالمية WebCGM مع قدرة معززة لاستخدامها مع صفحات الويب. في عام 2007 ، تم إطلاق الإصدار الثاني من WebCGM وتم إصدار الإصدار الثالث في عام 2010 بقدرات محسّنة.

## تنسيق ملف CGM ##

ملفات تعريف رسومات الكمبيوتر هي أساسًا قاعدة بيانات للمعلومات الرسومية وتوفر الوسائل لالتقاط البيانات الرسومية وتخزينها ونقلها. وبالتالي ، يجب أن يكون هناك مكون نظام رسومي لإنشاء قاعدة البيانات في وقت واحد مع تنفيذ أحد التطبيقات بتنسيق ملف تعريف. في معظم الحالات ، يكون هذا المكون هو منشئ ملف التعريف. إلى جانب ذلك ، هناك حاجة إلى مكون آخر يمكنه جلب البيانات الرسومية وتفسيرها وعرضها في ملف تعريف. يتم تلبية هذه الحاجة من خلال وجود مترجم ملف تعريف. يمثل الشكل التالي بيئة عمل ملف التعريف الرسومي.

يوضح الشكل أعلاه علاقة CGM بالمكونات الأخرى لنظام الرسومات النموذجي. يتضح أيضًا من الشكل أن وظيفة ملف التعريف لا تعتمد على إخراج الجهاز النهائي.

بشكل عام ، هناك فئتان من ملف التعريف: ** التقاط المقطع ** و ** التقاط الصورة **. الوظيفة الأساسية لملف تعريف التقاط الصورة هي التقاط تعريفات صور متعددة مستقلة عن الجهاز. بينما تستخدم ملفات تعريف التقاط الجلسة واجهة النظام لالتقاط حوار الإخراج في نظام رسومي. ينتمي CGM إلى فئة ملفات تعريف التقاط الصور الثابتة. يوفر CGM ترتيبًا منظمًا جيدًا للمكونات بهيكل من مستويين.

1. واصف ملف التعريف
1. مجموعة من الصور المستقلة منطقيًا

كل صورة عبارة عن مجموعة من واصفات الصورة ونص الصورة بما في ذلك تعريف الصورة. يعرّف واصف ملف التعريف المعلومات الوصفية التي تنطبق بشكل متساوٍ على كافة صور ملف التعريف هذا. تساعد هذه المعلومات المترجم على تحليل ملف تعريف بشكل صحيح والتعرف على الموارد المطلوبة للعرض الصحيح للصورة. على الرغم من أن واصف الصورة يحتوي أيضًا على المعلومات الوصفية ، إلا أنه يمكنه فقط التعرف على الصورة التي يتواجد فيها الواصف. في تنسيق الملف هذا ، يكون كل تعريف للصورة قائمًا بذاته وذو سيادة منطقيًا. وهي مستقلة عن كل تعريفات الصور الأخرى في الملف. مباشرة بعد تفسير واصف التعريف ، يمكن الوصول إلى الصور وتفسيرها بشكل عشوائي. التغيير في حالة الصور السابقة ليس له أي تأثير على من يخلفهم. استقلالية الصورة هذه هي ميزة بارزة أخرى لـ CGM. تتكون CGM من مساحة إحداثيات وهي إحداثيات ديكارتية ثنائية الأبعاد تسمى إحداثيات الجهاز الظاهري ويمكن تمثيلها من خلال الرقم أو الدقة التي تمثل النطاق والدقة. تحدد CGM كلاً من الاختيار المباشر للألوان والاختيار المستند إلى الفهرس. في السابق ، يتكون محدد اللون من RGB ثلاثي بينما لاحقًا ، يشير محدد اللون إلى فهرس في جدول ألوان.

CGM matches the needs of both communication-dependent as well as performance-dependent applications. Centralized and distributed graphics systems can use CGM in an unlimited number of ways.  It can be tailored to access graphics devices using a spooling system.