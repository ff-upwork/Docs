{
  "date" : "2020-03-02",
  "keywords" :[ "SVG", "файл", "формат файлу", "Мова опису сторінки", "Скаляр" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Дізнайтеся про формат файлу SVG та API, які можуть створювати та відкривати файли SVG.",
  "title" :"Що таке файл SVG?",
  "linktitle" : "SVG",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2020-03-02"
}

## Що таке файл SVG? ##

Файл SVG — це файл скалярної векторної графіки, який використовує текстовий формат на основі XML для опису вигляду зображення. Слово «масштабований» означає, що SVG можна масштабувати до різних розмірів без втрати якості. Текстовий опис таких файлів робить їх незалежними від роздільної здатності. Це один із найбільш використовуваних форматів для створення веб-сайту та друку графіки з метою досягнення масштабованості. Формат можна використовувати лише для двовимірної графіки. Файли SVG можна переглядати/відкривати майже в усіх сучасних браузерах, включаючи Chrome, Internet Explorer, Firefox і Safari.

## Коротка історія ##

Специфікації SVG доступні як відкритий стандарт Консорціумом Всесвітньої павутини (W3C) з 1999 року. До цього схожі специфікації формату файлів у шести різних форматах надсилалися до W3C до 1998 року. Оновлення специфікацій було застосовано до специфікацій у 2011 році, і вона мала версію 1.1 . У 2016 році SVG 2 було опубліковано як новішу версію, яка включає функції на додаток до тих, які є у SVG 1.1.

## Специфікації формату файлу ##

Об’єктна модель документа SVG (DOM) закладає основу для всіх специфікацій та інтерфейсів, які відповідають окремим розділам специфікацій. Переглядачі SVG повинні реалізувати інтерфейси SVG DOM, як визначено в специфікаціях W3C. Його DOM надає кілька інтерфейсів для різних типів даних і елементів.

### Фігури SVG ###

SVG має деякі попередньо визначені елементи форми, які можуть використовуватися розробниками:

* Прямокутник<rect>
* Коло<circle>
* Еліпс<ellipse>
* Лінія<line>
* Ломана<polyline>
* Багатокутник<polygon>
* Шлях<path>

Виходячи з цих форм і специфікацій, функціональні області SVG такі.

**Контури** – контури використовуються для зображення простих і складних контурів фігур. Кодування використовується для визначення характеру роботи. Наприклад, M використовується для переміщення до, L використовується для лінії до, Z використовується для закриття шляху тощо.

**Основні фігури** – можна малювати прямолінійні шляхи та контури, що складаються з серії з’єднаних прямолінійних сегментів (ламаних), а також замкнені багатокутники, кола та еліпси. Прямокутники та прямокутники із заокругленими кутами також є стандартними елементами.

**Текст** – представлення тексту виражається як дані символів XML, де до тексту можна застосувати багато візуальних ефектів. Специфікації дозволяють обробляти двонаправлений текст, вертикальний текст і символи вздовж вигнутого шляху.

**Малювання** – фігури можна заливати та/або обводити кольором, градієнтом або візерунком, що дозволяє зробити їх непрозорими або мати будь-який ступінь прозорості. Об’єкти кінця лінії, такі як наконечники стрілок або символи, що з’являються у вершинах багатокутника, представлені маркерами.

**Колір** – специфікації SVG дозволяють застосовувати кольори до всіх видимих елементів SVG безпосередньо або через заливку, обведення та інші властивості. Для вказівки можна використовувати різні кодування кольорів, як-от чорний або синій, шістнадцяткове подання, десяткове чи відсоткове значення у формі RGB.

**Градієнти та візерунки** – фігури у файлі SVG можна заливати або окреслювати суцільними кольорами, градієнтами або повторюваними візерунками.

**Ефекти фільтра** – насправді це серія графічних операцій, які застосовуються до вихідної векторної графіки для отримання зміненого результату.

**Інтерактивність** - користувачі можуть взаємодіяти з файлами SVG, змінюючи фокус, клацаючи мишею, прокручуючи або масштабуючи зображення. Інтерактивність дозволяє зображенням SVG взаємодіяти з користувачами різними способами, як зазначено вище.

**Посилання** – зображення SVG можуть мати гіперпосилання на інші документи. Це досягається за допомогою XML Linking Language або XLink. Це дозволяє створювати певні стани перегляду, які використовуються для збільшення/зменшення певної області або обмеження перегляду певним елементом.

**Сценарії** – Подібно до HTML, усі аспекти документа SVG доступні для маніпулювання за допомогою сценаріїв. Об’єкти SVG DOM містять вказівки щодо досягнення цього за допомогою елемента та атрибута SVG. Сценарії вкладено в елементи тегу `script` і можуть запускатися у відповідь на події вказівника, клавіатури або документа, якщо потрібно.

**Анімація** – елементи DOM<animate> ,<animateMotion> і<animateColor> дозволяє включати анімацію для вмісту SVG. Звичайно, цього неможливо досягти без використання скриптів і вбудованих таймерів. Ці анімації можуть бути безперервними і їх можна зациклювати, а також повторювати, одночасно реагуючи на події користувача.

**Шрифти** – текст у SVG може посилатися на зовнішні файли шрифтів, наприклад системні шрифти. За відсутності таких шрифтів текст у форматі SVG не відображатиметься на виході. Це можна подолати шляхом включення необхідних гліфів у такий файл як шрифт, який потім візуалізується за допомогою<text> елемент.

## Приклади ##
У наступних рядках показано, як коло представлено за допомогою сценарію SVG.

```
<html>
<body>

<h1>My first SVG</h1>

<svg width#"100" height#"100">
  <circle cx#"50" cy#"50" r#"40" stroke#"green" stroke-width#"4" fill#"yellow" />
</svg>

</body>
</html>
```

Наступні рядки коду показують, як використовувати<text> блок для відтворення тексту у SVG.

```
<svg height#"30" width#"200">
  <text x#"0" y#"15" fill#"red">I love SVG!</text>
</svg>
```

## Посилання ##

* [Специфікації W3C SVG](https://www.w3.org/TR/SVG2/Overview.html)
* [SVG – Вікіпедія](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics)
