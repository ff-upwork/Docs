{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف PDF / UA" ,
  "description":"تعرف على تنسيق ملف PDF / UA وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات PDF / UA وفتحها." ,
  "linktitle" : "PDF/UA",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
} ,
  "lastmod" : "2019-09-10"
}

# ما هو ملف PDF / UA؟ #

تم نشر PDF / UA باعتباره [معيار ISO 14289-1](https://en.wikipedia.org/wiki/ISO_14289) في أغسطس 2012 وهو إلى حد بعيد أول تعريف كامل لمجموعة من المتطلبات لمستندات PDF التي يمكن الوصول إليها عالميًا. يشير مصطلح "يمكن الوصول إليه عالميًا" إلى فهم أن المعلومات الواردة في مستند [PDF](/ar/ pdf /) يجب أن تكون متاحة بشكل متساو ومستقل للجميع بشكل عام وللأشخاص ذوي الإعاقة بشكل خاص. يمكن اعتبار تقديم معيار PDF / UA خطوة رئيسية لإنشاء الأدوات والتطبيقات من أجل إنشاء محتوى PDF وقراءته.

## متطلبات تنسيق الملف ##

يحتوي PDF / UA على بعض المتطلبات المحددة في قاعدته والتي تعمل بمثابة جوهر هذا المعيار. بشكل أساسي ، تستند هذه إلى تمييز ملفات PDF مما يعني أنه يجب تمييز جميع مستندات PDF / UA بشكل صحيح. كما يتطلب أيضًا أن تكون العلامات مناسبة لغويًا وفي ترتيب منطقي. هذا يضمن أن المستند النهائي الذي تم إنشاؤه باستخدام مواصفات PDF / UA أكثر موثوقية ويمكن الوصول إليه. قد يدفع هذا مؤلفي PDF للتساؤل عما إذا كانوا بحاجة إلى معرفة كل شيء عن كل هذه المتطلبات؟ لحسن الحظ ، الأمر ليس كذلك لأن أدوات توافق PDF / UA تتحمل مسؤولية إضافة وحفظ إمكانية الوصول إلى PDF.

متطلبات تنسيق الملف لـ PDF / UA هي كما يلي.

* يُصنف المحتوى بإحدى طريقتين: المحتوى الهادف والقطع الأثرية مثل عناصر الصفحة المزخرفة. يجب وضع علامات على كل المحتوى ذي المعنى ودمجها في شجرة الهيكل لجميع العلامات داخل المستند. من ناحية أخرى ، لا يجب وضع علامة على المصنوعات اليدوية إلا على هذا النحو.
* يجب تمييز المحتوى ذي المعنى بعلامات ، وإنشاء شجرة بنية كاملة مع العلامات الأخرى في المستند.
* يجب تمييز المحتوى ذي المعنى بعلامات دلالية مناسبة.
* يجب أن تعكس شجرة الهيكل التي تم إنشاؤها بواسطة علامات المستند ترتيب القراءة المنطقي للمستند.
* يمكن استخدام العلامات القياسية المحددة في PDF 1.7 فقط ؛ في حالة استخدام أي علامات أخرى ، يجب أن يسجل إدخال تعيين الدور العلامة القياسية التي يمثلها كل واحد.
* لا يجوز نقل المعلومات باستخدام الوسائل المرئية وحدها (مثل التباين أو اللون أو الموضع على الصفحة).
* لا يُسمح بالمحتوى الوامض أو الوامض أو الوامض ، سواء كتأثيرات يتم التحكم فيها بواسطة JavaScript أو كجزء من أي مقاطع فيديو مضمنة في ملف PDF.
* يجب إعطاء عنوان المستند ، ويجب إعداد المستند بحيث يظهر العنوان (بدلاً من اسم الملف) في عنوان النافذة.
* يجب الإشارة إلى لغة المحتوى بالكامل ، كما يجب تمييز تغييرات اللغة على هذا النحو صراحة.

## توافق PDF / UA ##

يحدد معيار PDF / UA مواصفات المحتوى والقراء والتكنولوجيا المساعدة. ترتبط هذه الجوانب الثلاثة ببعضها البعض بناءً على محتويات الوثيقة. متطلبات المطابقة لكل من هذه كما هو مذكور أدناه.

## ملفات مطابقة ##

يجب أن تحتوي الملفات المتوافقة مع معيار PDF / UA على ميزات صالحة وفقًا لمواصفات [PDF 1.7](http://www.adobe.com/go/pdfreference). ومع ذلك ، يجب استبعاد الميزات المحظورة بواسطة PDF / UA على وجه التحديد.

## توافق القراء ##

يجب أن يلتزم القارئ المطابق بالقواعد المنصوص عليها في مواصفات PDF 1.7. على وجه التحديد ، يجب أن تدعم:

* جميع العلامات والسمات والقيم الأساسية المحددة لإمكانية الوصول. يجب أن تتمتع أيضًا بالقدرة على معالجة وتمثيل التوقيعات الرقمية والتعليقات التوضيحية والمحتوى الاختياري.
* معالجة وتمثيل التوقيعات الرقمية والتعليقات التوضيحية والمحتوى الاختياري
* التنقل في المستند بعدة طرق

## مطابقة التكنولوجيا المساعدة ##

التكنولوجيا المساعدة المطابقة ملزمة لدعم ميزات PDF / UA. تتضمن هذه ، على سبيل المثال ، ميزات المحتوى والقارئ ، ويجب أن تسمح بالتنقل عن طريق تسميات الصفحة أو بنية المستند أو المخطط التفصيلي. يجب أن يسمح أيضًا للمستخدم بتجاوز تكبير التنقل الافتراضي.

## مراجع ##

* [PDF / UA - بواسطة Wikipedia](https://en.wikipedia.org/wiki/PDF/UA)
* [PDF / UA in a Nutshell](http://www.pdfa.org/publication/pdfua-in-a-nutshell/)
