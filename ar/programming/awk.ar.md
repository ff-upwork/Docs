{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف AWK - ملف البرنامج النصي AWK" ,
  "description":"تعرف على تنسيق ملف AWK وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات AWK وفتحها." ,
  "linktitle" : "AWK",
  "menu" : {
    "docs" : {
      "identifier" : "programming-awk",
      "parent" : "programming"
}
} ,
  "lastmod" : "2022-04-03"
}

## AWK ما ه

ملف AWK هو ملف نصي تم إنشاؤه لتطبيق معالجة النصوص ** AWK ** والذي يأتي مرفقًا مع أنظمة تشغيل Unix و Linux. يحتوي على إرشادات منطقية لتنفيذ إجراءات على نص أو محتويات ملف مثل مطابقة النص واستبداله وطباعته. يساعد هذا في إنشاء تقارير ونص منسق من ملف الإدخال. توجد الأداة المساعدة awk عادةً في / usr / bin / awk في معظم توزيعات Linux / unix.

## كيفية إنشاء برنامج AWK Script؟

يمكن إنشاء ملف AWK أو فتحه في أي محرر نصوص على Linux / Unix OS. يمكن إنشاء ملف نصي جديد AWK على النحو التالي.

```
$ vi script.awk
```

سيؤدي هذا إلى فتح ملف AWK في محرر النصوص. أدخل بعض العبارات في محرر النص على النحو التالي.

```
#!/usr/bin/awk -f
BEGIN { printf "%s\n","Writing my first Awk executable script!" }
```
يتم شرح السطر الأول من محتوى النص هذا على النحو التالي.

* \ #! - يشار إليها باسم "Shebang" ، والتي تحدد مترجمًا للتعليمات في النص
* / usr / bin / awk - هو المترجم
* -f - خيار المترجم ، يستخدم لقراءة ملف البرنامج

## كيف يتم تنفيذ البرنامج النصي AWK؟

احفظ الملف واجعل البرنامج النصي قابلاً للتنفيذ بإصدار الأمر أدناه:
```
$ chmod +x script.awk
```

يمكن بعد ذلك تشغيل البرنامج النصي على النحو التالي.

```
$ ./script.awk
```

ينتج عنه الإخراج التالي.

```
Writing my first Awk executable script!
```

## المرجعي ##

* [اكتب نصوصًا باستخدام لغة برمجة Awk] (https://www.tecmint.com/write-shell-scripts-in-awk-programming/)
