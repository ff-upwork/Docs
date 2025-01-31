{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файлу WMV",
  "description":"Дізнайтеся про формат файлу WMV та API, які можуть створювати та відкривати файли WMV.",
  "linktitle" : "WMV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-16"
}

## Що таке файл WMV?

Advanced Systems Format (ASF) — це цифровий мультимедійний контейнер, призначений головним чином для зберігання та передачі медіапотоків. Microsoft Windows Media Video (WMV) — це формат стисненого відео, а Microsoft Windows Media Audio (WMA) — це формат стисненого аудіо разом із додатковими метаданими в контейнері ASF, розробленому Microsoft. Якщо файли WMV або WMA закодовано за допомогою кодеків Windows Media Video та Windows Media Audio, вони представлені розширенням .asf. WMV стискає великі файли для кращої швидкості передачі через мережу, зберігаючи при цьому якість відео. WMV спеціально розроблено для роботи на всіх пристроях Windows. Після стандартизації Товариством інженерів кіно та телебачення (SMPTE) WMV тепер вважається відкритим стандартним форматом.

## Історія ##

За допомогою власних кодеків корпорації Майкрософт у 1999 році було розроблено новий формат стисненого відео, відомий як WMV7, який базувався на MPEG-4, частина 2. Удосконалення були додані в наступні дві версії, тобто WMV8 і 9. Корпорація Майкрософт представила 9^^ту^^ версію від WMV до SMPTE для стандартизації в 2003 році, який зрештою був стандартизований у 2006 році як SMPTE 421M, також відомий як VC-1. Ідея, що лежить в основі WMV, полягала в тому, щоб розробити медіаформат, який міг би підтримуватися всім апаратним і програмним забезпеченням, що підтримується Microsoft. Крім того, ще однією важливою метою була передача відеопотоків через Інтернет за оптимальним сценарієм. Після стандартизації від SMPTE WMV також став відеоформатом для дисків Blu-ray.

## Специфікації формату файлу

### Контейнер

Як правило, WMV упаковується в контейнер ASF, але крім того, контейнер Matroska або AVI також може підтримувати його з розширеннями .mkv і .avi відповідно.

### Windows Media Video 9

Хоча в серії Windows Media Video 9 доступні різні аудіо- та відеокодеки для створення та відтворення цифрових медіа, кодек WMV-9 є найновішим і найкращим відеокодеком, оскільки він може досягти оптимального стиснення з дуже низьких бітрейтів, тобто 160 x Від 120 зі швидкістю 10 Кбіт/с до 1920 x 1080 зі швидкістю 4–8 Мбіт/с для різних HD-відео.

### Структура кодека

WMV-9 має 8-бітний формат внутрішнього кольору 4:2:0. Як і всі інші популярні стандарти стиснення відео MPEG-1 і H.261, WMV-9 використовує блочну компенсацію руху та схему просторового перетворення. Загалом можна сказати, що ці стандарти виконують поблочну компенсацію руху від попереднього реконструйованого кадру за допомогою 2-D величини, яка називається вектором руху (MV), щоб сигналізувати про просторове зміщення. Поточний блок формується за допомогою передбачення значень з попереднього реконструйованого кадру такого ж розміру, який зміщений від поточної позиції вектором руху. Зрештою, залишкова помилка обчислюється як різниця між прогнозованим блоком з компенсацією руху та фактичним блоком. Ця залишкова помилка перетворюється за допомогою лінійного перетворення з ущільненням енергії, потім квантується та ентропійно кодується.

Квантовані коефіцієнти перетворення піддаються ентропійному декодуванню, деквантуванню та зворотному перетворенню для отримання наближеної оцінки залишкової помилки на стороні декодера, яка потім додається до передбачення з компенсацією руху для створення реконструкції. Загальний опис кодека показано на наступному зображенні.

У решті розділу буде обговорено нові вдосконалення WMV-9, які відрізняють його від решти рішень кодування відео, таких як стандарти MPEG. WMV-9 має внутрішні (I), передбачені (P) і двонаправлені передбачені (B) кадри. Внутрішні кадри – це ті, які кодуються незалежно і не залежать від інших кадрів. Прогнозовані кадри – це кадри, які залежать від одного кадру в минулому. Декодування передбаченого кадру може відбуватися лише після того, як усі опорні кадри перед поточним кадром, починаючи з останнього (I) кадру, були декодовані. B-кадри — це кадри, які мають дві посилання — одну в тимчасовому минулому й одну в тимчасовому майбутньому. B-кадри передаються після своїх посилань, що означає, що B-кадри надсилаються не по порядку, щоб гарантувати, що їхні посилання доступні під час декодування. Кадри B у WMV-9 не використовуються як посилання для наступних кадрів. Це розміщує B-кадри поза циклом декодування, дозволяючи використовувати ярлики під час декодування B-кадрів без дрейфу або довготривалих візуальних артефактів. Наведене вище визначення кадрів I, P і B справедливе як для прогресивних, так і для послідовностей із чергуванням.

Продуктивність відеокодеків порівнюється з їх графіком швидкості спотворення (RD). Це двовимірна крива, яка показує спотворення, спричинене стисненням із певним бітрейтом.

WMV-9 вирішив цю проблему, ввівши низку методів, перелічених нижче:

1. Адаптивне перетворення розміру блоку

2. Набір перетворень обмеженої точності

3. Компенсація руху

4. Квантування та деквантування

5. Розширене ентропійне кодування

6. Петлева фільтрація

7. Розширене кодування кадрів B

8. Черезрядкове кодування

9. Згладжування нахлестом

10. Низькотарифні інструменти

11. Компенсація загасання

## Посилання ##

* [https://bytescout.com/blog/2018/02/windows-media-video-format.html](https://bytescout.com/blog/2018/02/windows-media-video-format.html)
* [https://en.wikipedia.org/wiki/Windows_Media_Video](https://en.wikipedia.org/wiki/Windows_Media_Video)

