{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDB", "розширення", "файл", "формат файлу", "Тип файлу бази даних", "Формат файлу бази даних", "Файли бази даних" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Дізнайтеся про формат файлу ACCDB та API, які можуть створювати та відкривати файли ACCDB.",
  "title" :"Формат файлу ACCDB - файл бази даних Microsoft Access 2007",
  "linktitle" : "ACCDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## Що таке файл ACCDB?

Файл із розширенням .accdb — це файл бази даних Microsoft Access 2007, який зберігає дані користувачів у таблицях. Він підтримує зберігання
спеціальні форми, запити SQL та інші дані. Файли ACCDB замінили файли [MDB](/uk/database/mdb/) після того, як Microsoft перейшла на файлову структуру на основі XML. Файли ACCDB все ще можна конвертувати в MDB зі старою сумісністю. Проте ACCDB зараз є широко використовуваним форматом файлів бази даних Access. Корпорація Майкрософт також підтримує додаткові функції у форматі ACCDB, такі як можливість зберігання вкладених файлів, двійкових даних і підтримки багатозначних полів.

## Формат файлу ACCDB

Як і MDB, для формату файлу ACCDB немає загальнодоступних специфікацій. Microsoft підтримує програмний доступ до цих файлів через стандарт Open Database Connectivity (ODBC) і Visual Basic for Applications (VBA).

### Інсайт

Шістнадцятковий дамп простого файлу ACCDB свідчить про загальну схожість структури з останніми версіями попередника MDB Format Family. Обидва формати файлів використовують фіксовані розміри сторінок 4096 байт. Ще одна подібність між ACCDB і MDB полягає у формі магічного числа, яке включає рядок «Стандартний ACE DB» для ACCDB. Версія або код сумісності знаходяться в одному місці в обох форматах. Інструменти mdbtools | У файлі HACKING зазначено, що «Offset 0x14 містить Jet-версію цієї бази даних», і неофіційний посібник MDB погоджується. Інформація в цих джерелах разом із записом у Вікіпедії для [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine) свідчить про те, що значення 0x02 вказує на ACE 12 (Access 2007), а 0x03 вказує на ACE 14 (Access 2010). Однак мінімальна база даних, створена в Access 2010, і подібна база даних, створена в Access 2016, мають 0x02 у цьому місці. Мінімальна база даних, створена в Access 2016, але в якій визначено стовпець із нещодавно введеним типом даних «велике ціле», мала значення 0x05. У файлах ACCDB цей індикатор відображає сумісність файлу, а не версію механізму ACE, який використовується для його створення.

## Список літератури

* [Формат файлу доступу](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41?redirectSourcePath=% 252fen-us%252farticle%252fIntroduction-to-the-Access-2007-file-format-8cf93630-0b68-4a40-a13c-7528b9f074b6&ui=en-US&rs=en-US&ad=US)
* [Технічні характеристики Access 2016](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c?ui=en-us&rs=en-us&ad=us)
* [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)
* [Який формат файлу Access слід використовувати?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41?ui=en-us&rs=en-us&ad=us)