{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف القفل - ما هو ملف القفل؟" ,
  "description":"تعرف على تنسيق ملف LOCK و." ,
  "linktitle" : "LOCK",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
} ,
  "lastmod" : "2022-01-26"
}

## ما هو ملف LOCK؟

ملف ** LOCK ** هو ملف تمت إعادة تسميته تستخدمه التطبيقات وأنظمة التشغيل لوضع علامة على ملف أو بعض الأجهزة على أنها مقفلة. يخبر هذا التطبيقات الأخرى بعدم استخدام الملف ما لم يكن خاليًا من التطبيق الذي يستخدمه. في معظم الحالات ، تكون ملفات التأمين هذه فارغة ، ولكن في حالات أخرى ، قد تحتوي على معلومات متعلقة بالقفل مثل الخصائص والإعدادات.

في بعض الأحيان ، يتم استخدام ملف .lock بواسطة .NET Framework من Microsoft لإنشاء نسخ ** lockeed ** من ملف قاعدة البيانات. في مثل هذه الحالة ، سيتم فتح نسخة من ملف قاعدة البيانات بامتداد .lock. لا يسمح هذا للمستخدم بإجراء تغييرات على الملف أثناء استخدامه من قبل مستخدم آخر.

## تنسيق ملف القفل - مزيد من المعلومات

يتم إنشاء ملف LOCK بواسطة كل تطبيق ويكون تنسيق ملفه خاصًا بالتطبيق. يمكن حفظ ملفات القفل هذه بتنسيق نصي وملف ثنائي.

يمنع وجود ملفات القفل الوصول المتزامن لمورد إلى عدة ملفات تحاول الوصول إلى هذا المورد. يتم إنشاء نسخة من الملف الأصلي بملحق .lock ملحق باسمه. هذا يخبر التطبيقات الأخرى أن يكون لها حق الوصول للقراءة فقط إلى الملف. على سبيل المثال ، سوف تصبح Resource.dat Resource.data.lock.

بالنسبة إلى لغة برمجة Ruby ، قد تصادف الملف ** gemfile.lock **. هذا هو المكان الذي يحتفظ فيه Bundler بسجل للإصدارات الدقيقة التي تم تثبيتها. وبالتالي ، عندما يتم نقل مشروع / مكتبة إلى جهاز آخر ، ستنظر الحزمة قيد التشغيل في Gemfile للحصول على الإصدار المناسب بالضبط.

## قفل الملف في لينكس

يدعم Linux نوعين من أقفال الملفات: أقفال استشارية وأقفال إلزامية.

* ** أقفال إرشادية **: نوع القفل الذي لا يتم فرضه. في هذه الحالة ، تتعاون العمليات المشاركة مع بعضها البعض بشكل صريح للحصول على أقفال. إذا لم يكن ذلك ممكنًا ، فسيتم تجاهل الأقفال الإرشادية.

* ** إقفال إلزامي **: في حالة القفل الإلزامي ، يفرض نظام التشغيل قفل الملف عن طريق منع العمليات الأخرى من قراءة الملف أو كتابته. هذا لا يتطلب أي تعاون بين العمليات.

لا يتطلب القفل الإلزامي أي تعاون بين العمليات المشاركة. بمجرد تنشيط القفل الإلزامي على الملف ، يمنع نظام التشغيل العمليات الأخرى من قراءة الملف أو كتابته.

## مراجع

* [GemFile و Gemfile.lock في Ruby](https://medium.com/never-hop-on-the-bandwagon/gemfile-and-gemfile-lock-in-ruby-65adc918b856)
* [Locking in Linux](https://www.baeldung.com/linux/file-locking#:~:text=File٪20locking٪20is٪20a٪20mechanism،very٪20dangerous٪20command٪20in٪20Linux.)
