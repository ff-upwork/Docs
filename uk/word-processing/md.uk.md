{
  "date" : "2019-10-11",
  "keywords" :[ "файл md", "формат файлу md", "що таке файл md", "файл", "приклад md", "розширення файлу md", "розширення", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MD - мовний файл MarkDown",
  "description":"Дізнайтеся про формат файлу MD та API, які можуть створювати та відкривати файли MD.",
  "linktitle" : "MD",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Що таке файл MD?

Текстові файли, створені за допомогою діалектів мови Markdown, зберігаються з розширенням **.md** або **.MARKDOWN**. Файли MD зберігаються у форматі простого тексту, який використовує мову Markdown, яка також містить вбудовані текстові символи, що визначають спосіб форматування тексту, наприклад відступи, форматування таблиці, шрифти та заголовки. Файли MD можна конвертувати в HTML за допомогою програми під назвою Markdown. Мова Markdown випущена Джоном Грубером.

Файли MD також можна віднести до категорії файлів розробників, які в основному використовуються Markdown для перетворення текстових файлів у версії HTML, щоб користувачі могли створювати файли, які легко читати та писати. Нижче наведено програми, які можуть відкрити файл .md:

* Microsoft Notepad
* Блокнот 2
* Apple TextEdit
* Microsoft WordPad

Застереження: не перейменовуйте розширення файлів .md. Якщо так, це не призведе до зміни типу файлу, оскільки існують спеціальні програми для перетворення файлів, які дозволяють змінити тип файлу на інший. Як обговорювалося вище, файли .MD є розширеннями файлів, створених програмним забезпеченням мови Markdown. **Markdown** – це [спрощена мова розмітки](https://en.wikipedia.org/wiki/Lightweight_markup_language), призначена для однієї мети: використовувати її для форматування тексту в Інтернеті за допомогою синтаксису форматування простого тексту. Зазначимо, що Markdown не є заміною HTML, оскільки його синтаксис дуже малий і містить дуже невелику підмножину тегів HTML. Причина Markdown полягає в тому, щоб полегшити читання, написання та редагування прози. Іншими словами, ми можемо сказати, що HTML – це формат публікації, а Markdown – це формат написання.

Зараз Markdown є однією з найпопулярніших мов розмітки у світі. Під час використання Microsoft Word форматування слів і фраз відбувається за допомогою натискання кнопок, і зміни одразу видно. Але Markdown не такий. Коли створюється файл у форматі Markdown, синтаксис Markdown додається до тексту, щоб вказати, які слова та фрази можуть виглядати інакше. Наприклад, щоб показати заголовок, перед ним додається знак числа (наприклад, # Заголовок один). Для виділення жирним реченням перед і після нього додаються дві зірочки (наприклад, **цей текст виділено жирним шрифтом**). Синтаксис Markdown можна побачити через деякий час у тексті.

## Коротка історія

Джон Грубер і Аарон Шварц у 2004 році створили мову Markdown з ідеєю дозволити людям «писати, використовуючи простий текстовий формат, який легко читати та писати, і з можливістю конвертувати його в XHTML або HTML. Метою його дизайну є читабельність – мову можна читати такою, якою вона є, не схоже на те, що вона була позначена чи додана інструкціями форматування, як це робиться в мовах розмітки, таких як RTF або HTML, де теги та інструкції форматування очевидні. Основним джерелом натхнення є використання існуючих угод для розмітки звичайного тексту в електронній пошті.

Відтоді Markdown було повторно реалізовано іншими, а також у [модулі] Perl (https://en.wikipedia.org/wiki/Modular_programming), доступному на [CPAN](https://en.wikipedia.org/ wiki/CPAN) та різними іншими мовами програмування. Він поширюється за [ліцензією у стилі BSD](https://en.wikipedia.org/wiki/BSD_license) і входить до кількох [систем керування вмістом](https://) або доступний як плагін для них. en.wikipedia.org/wiki/Content_management_system).

## Технічні характеристики

Коли щось написано в Markdown, текст спочатку зберігається у відкритому текстовому файлі з розширенням .md або .markdown, а потім програма Markdown, така як Dillinger, використовується для обробки файлу Markdown для перетворення відформатованого тексту Markdown у HTML для відображення в Інтернеті браузери. Програми Markdown використовують //процесор Markdown// (який також зазвичай називають «аналізатором» або «реалізацією»), щоб отримати текст у форматі Markdown і вивести його у формат HTML. Схема процесу така:

Коротше кажучи, це чотириетапний процес, який виглядає наступним чином:

1. По-перше, створення файлів Markdown за допомогою текстового редактора або програми Markdown із розширенням .md або .markdown.
1. Потім файл Markdown відкривається в програмі Markdown.
1. Програма Markdown використовується для перетворення файлу Markdown на документ HTML.
1. Потім файл HTML переглядається у веб-браузері або використовується програма Markdown, щоб конвертувати його в інший формат файлу, як-от PDF.

Markdown дозволяє швидко та легко робити нотатки, писати вміст для веб-сайтів, створювати готові документи для друку, видавати книги, генерувати презентації та створювати документи.

Деякі з версій у розмітці мали значний вплив на інші версії настільки, що їх часто можна побачити як частину інших версій. Наприклад, бібліотеки згадують підтримку CommonMark (GFM). Давайте коротко розглянемо їх.

### GFM
Markdown настільки популярний серед розробників, тому що платформа спільного доступу з відкритим кодом Github прийняла та розширила мову версією під назвою Github Flavored Markup (GFM), яка включає блоковані блоки коду, автоматичне посилання URL-адрес, закреслення, таблиці та створення завдань.

### CommonMark
Розробники Markdown нещодавно спробували стандартизувати Markdown, вони об’єдналися, щоб створити версію, тести та документацію для мови, яка є більш надійною та називається CommonMark. Цей формат трохи новий і не підтримує багато функцій, але незабаром буде додано багато функцій MultiMarkdown.

### Multi-Markdown
Multi-Markdown додав різні функції до мови, які підтримуються іншими версіями. Спочатку він був написаний на Perl, але пізніше перейшов на C. Він підтримує виділені кодові блоки, підсвічування синтаксису, таблиці, метадані, посилання на фрагменти/перехресні посилання, виноски, закреслення, списки визначень, математику.

## Список літератури

* [Опанування MarkDown](https://guides.github.com/features/mastering-markdown/)
