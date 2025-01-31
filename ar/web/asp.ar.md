{
  "date" : "2019-10-11",
  "keywords" :["asp" , "ملف asp" , "تنسيق ملف asp" , "نوع ملف asp" , "ملف" , "نوع" , "ما هو ملف asp"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"ASP - تنسيق ملف صفحات الخادم النشط" ,
  "description" :"تعرف على ما هو ملف ASP وواجهات برمجة التطبيقات التي يمكنها إنشاءهما وفتحهما." ,
  "linktitle" : "ASP",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2019-09-10"
}

## ما هو ملف ASP؟

يرمز ASP إلى Active Server Pages وهو إطار تطوير لإنشاء صفحات الويب. إنه يمكّن رمز الكمبيوتر ليتم تنفيذه بواسطة خادم داخلي لخدمة طلبات الويب. عندما يتم إنشاء طلب لملف ASP بواسطة مستعرض الويب ، يقرأ الخادم الملف وينفذ أي كود / نص برمجي بداخله لإنشاء النتيجة ** [HTML](/ar/web/html/) ** التي يتم إرجاعها إلى متصفح للعرض.

على عكس صفحات HTML ، وهي صفحات ثابتة يخدمها الخادم ، تنشئ ملفات ASP محتويات ديناميكية في وقت التشغيل والتي قد تتضمن طلبات للبيانات من قاعدة بيانات. تستخدم صفحات ASP عادةً ملحق .asp بدلاً من .html. نظرًا لأن الكود / البرنامج النصي داخل ملف ASP يتم تنفيذه على جانب الخادم ، فإن طلب المتصفح لا يمكنه رؤية الكود المستخدم لبناء الصفحة المعروضة. جميع المتصفحات الحديثة قادرة على عرض الصفحات التي تم إنشاؤها نتيجة لذلك. نظرًا لكونها مبنية على تقنية Microsoft ، تتم استضافة الصفحات التي تم إنشاؤها باستخدام ASP على خوادم Microsoft Internet Information Services (IIS).

## تاريخ موجز لتنسيق ملف ASP
لقد مرت ASP بمراجعات قليلة فقط حيث تم استبدالها بواسطة ASP.NET وهي طريقة أكثر حداثة وأكثر فاعلية لتطوير وإدارة الصفحات الجانبية للخادم. يتم تضمين دعم ASP بشكل افتراضي مع خدمات معلومات الإنترنت (IIS). تم نشر ASP في ثلاثة إصدارات مختلفة مع تحسينات في كل نسخة.

* تم إصدار ASP 1.0 في ديسمبر 1996 كجزء من IIS 3.0
* تم إصدار ASP 2.0 في سبتمبر 1997 كجزء من IIS 4.0
* تم إصدار ASP 3.0 في نوفمبر 2000 كجزء من IIS 5.0

## كائنات ASP الوظيفية

تستخدم ملفات ASP كائنات جانب الخادم لمعالجة طلبات المستخدم وإنشاء صفحات الإخراج ليتم تقديمها للمستخدمين. يحتوي كل كائن على مجموعة من المجموعات والخصائص والطرق لمعالجة الطلبات والاستجابات. تشمل هذه الأشياء:

### طلب كائن

عندما يطلب المستعرض صفحة من الخادم ، يطلق عليه طلب. يتم استخدام كائن الطلب للحصول على معلومات من الزائر.

### كائن الاستجابة

يتم استخدام كائن ASP Response لإرسال الإخراج إلى المستخدم من الخادم.

### كائن الخادم

يتم استخدام كائن خادم ASP للوصول إلى الخصائص والأساليب الموجودة على الخادم. يسمح بالاتصال بقواعد البيانات (ADO) ونظام الملفات واستخدام المكونات المثبتة على الخادم.

### كائن الجلسة

كائن الجلسة يشبه الارتباط بين متصفح المستخدم الذي يطلب صفحة من الخادم والخادم نفسه. يتم تحقيق ذلك من خلال ملف تعريف ارتباط تم إنشاؤه بواسطة ASP وإرساله إلى كمبيوتر المستخدم. يقوم كائن Session بتخزين معلومات حول أو تغيير الإعدادات لجلسة مستخدم. يتم تخزين المعلومات في كائن Session ويتم مشاركتها عبر جميع صفحات التطبيق. المعلومات الشائعة المخزنة في متغيرات الجلسة هي الاسم والمعرف والتفضيلات. يقوم الخادم بإنشاء كائن Session جديد لكل مستخدم جديد ، ويدمر كائن Session عند انتهاء صلاحية الجلسة.

### كائن التطبيق

يحتفظ كائن التطبيق بالمعلومات التي سيتم استخدامها بواسطة العديد من الصفحات في التطبيق (مثل معلومات اتصال قاعدة البيانات). يمكن الوصول إلى المعلومات من أي صفحة. يمكن أيضًا تغيير المعلومات في مكان واحد ، وستنعكس التغييرات تلقائيًا على جميع الصفحات. يتم استخدام كائن التطبيق لتخزين المتغيرات والوصول إليها من أي صفحة ، تمامًا مثل كائن Session.

### كائن ASPError

تم تنفيذ كائن ASPError في ASP 3.0 وهو متوفر في IIS5 والإصدارات الأحدث يتم استخدام كائن ASPError لعرض معلومات مفصلة عن أي خطأ يحدث في البرامج النصية في صفحة ASP.

** ملاحظة: ** يتم إنشاء كائن ASPError عند استدعاء Server.GetLastError ، لذلك لا يمكن الوصول إلى معلومات الخطأ إلا باستخدام طريقة Server.GetLastError.

## مراجع

* [ASP - By W3C](https://www.w3schools.com/asp/default.asp)
* [إنشاء صفحات ASP بسيطة](https://learn.microsoft.com/en-us/previous-versions/iis/6.0-sdk/ms524741(v=vs.90))

