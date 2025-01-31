{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файлу PDF/VT",
  "description":"Дізнайтеся про формат файлу PDF/VT та API, які можуть створювати та відкривати файли PDF/VT.",
  "linktitle" : "PDF/VT",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Що таке PDF/VT? #

PDF/VT, опублікований як [ISO 16612-2](https://www.iso.org/standard/46428.html) у серпні 2010 року як стандарт, призначений для забезпечення друку змінних документів (VDP) у різноманітних середовищ. Основою стандарту є друк змінної інформації та транзакцій. Друк змінних даних використовується, коли частина інформації різна для кожного одержувача вмісту. Транзакційний друк включає рахунки-фактури, виписки та інші документи, які поєднують платіжну інформацію з маркетинговою інформацією. Це призводить до поєднання покращеної обробки зображень, тексту та інших типів вмісту. PDF/VT забезпечує надійне та динамічне керування сторінками для даних друку великого обсягу транзакцій (HVTO) за допомогою концепції метаданих частини документа (DPM). Файли PDF/VT можна відкривати у засобі перегляду Adobe Acrobat без необхідності додавання будь-яких інших компонентів.

## Ієрархія частин документа ##

Ієрархія частини документа (DPart) схожа на деревоподібну структуру вузлів частини документа, яка базується на всіх сторінках документа. Елементи цього дерева називаються вузлами DPart. Кожен внутрішній вузол містить інші вузли DPart, і кожен кінцевий вузол визначає одну або більше сторінок для одержувача. По суті, ієрархія DPart визначає послідовність і взаємозв’язок документів або фрагментів документів у файлі PDF/VT. Деревоподібна структура вузлів DPart легко представляє внутрішній вміст документа PDF/VT, оскільки він може містити піддокументи для багатьох одержувачів, і кожна частина документа відповідає сторінкам для одного одержувача. Ієрархія DPart потрібна для файлів PDF/VT.

## Метадані частини документа (DPM) ##

Метадані частини документа (DPM) пов’язані з кожним вузлом в ієрархії частин документа та можуть використовуватися для передачі інформації про піддокумент конкретного одержувача та його частини. Зокрема, DPM може містити інформацію про властивості або інформацію про одержувачів у закодованій формі.

## Рівні відповідності ##

PDF/VT надається за такими трьома рівнями відповідності. Усі вони базуються на [PDF](/uk/pdf/) 1.6.

* `PDF/VT-1` – засновано на PDF/X-4 і містить усі ресурси, необхідні для візуалізації документа PDF.
* `PDF/VT-2` – розроблені для обміну кількома файлами, документи PDF/VT-2 можуть посилатися на зовнішні наміри виводу, зовнішній вміст або обидва. Документ PDF/VT і всі PDF-файли, на які він посилається, і зовнішні наміри виведення разом називаються набором файлів PDF/VT-2. Acrobat 9 і підтримують цю функцію.
* `PDF/VT-2s` - підтримує пряму трансляцію PDF/VT-2. Це дозволяє обробляти сегментовані розділи даних.

## Посилання ##

* [PDF/VT – Вікіпедія](https://en.wikipedia.org/wiki/PDF/VT)
* [ISO 16612-2 Графічна технологія](https://www.iso.org/standard/46428.html)

