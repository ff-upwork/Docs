{
  "date" : "2022-01-04",
  "keywords" :[ ".dst", "файл", "формат", "розширення", "API", "Набір аркушів AutoCAD" ],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DST - файл аркушів AutoCAD",
  "description" :"Дізнайтеся про файл .dst і API, які можуть створювати та відкривати файли DST.",
  "linktitle" : "DST",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2022-01-04"
}

## Що таке файл DST?

Файл DST — це файл AutoCAD, який містить асоціації та інформацію для визначення наборів аркушів. Вони зберігаються в стандартній папці зберігання аркушів AutoCAD Sheet Sets. Файли DST не містять фактичних макетів креслення, але посилаються на них із вибраних файлів [DWG](/uk/cad/dwg/) і [DWT](/uk/cad/dwt/), пов’язаних із цими аркушами. У мережевому середовищі всі члени команди повинні мати мережевий доступ до цих пов’язаних файлів. Файли DST зберігаються на диск у форматі [XML](/uk/web/xml/).

## Формат файлу DST – Додаткова інформація

Файли DST створюються за допомогою інструменту AutoDesk Sheet Set Manager (SSM). Коли хтось із команди отримує доступ до файлу, файл DST ненадовго відкривається, а потім зберігається з оновленою інформацією. Одночасним доступом до того самого файлу DST керує інструмент SSM, який показує піктограму замка, коли доступ до файлу доступний.

У будь-який конкретний час статус аркуша може бути в будь-якому з наступних станів.

* Аркуш доступний для редагування.
* Аркуш заблокований.
* Аркуш відсутній або знайдений у неочікуваному місці папки.

## Список літератури

* [Про використання наборів таблиць DST](https://knowledge.autodesk.com/support/autocad-lt/learn-explore/caas/CloudHelp/cloudhelp/2017/ENU/AutoCAD-LT/files/GUID-577D8EA0-85F2 -4829-B4F9-8CAD6F7AAACC-htm.html)
* [Докладніше про набори аркушів](https://knowledge.autodesk.com/support/autocad-lt/learn-explore/caas/CloudHelp/cloudhelp/2017/ENU/AutoCAD-LT/files/GUID-34D889BC-19AD- 4CD1-ADB1-F359D9B515FB-htm.html)
* [Опанування наборів аркушів AutoCAD](https://damassets.autodesk.net/content/dam/autodesk/www/cad-manager-center/articles/Mastering-AutoCAD-Sheet-Sets_Preview_EN.pdf)
