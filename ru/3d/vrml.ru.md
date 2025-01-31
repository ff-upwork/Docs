{
  "date" : "2019-10-11",
  "keywords" :[ "файл vrml", "формат файла vrml", "что такое файл vrml", "файл", "пример vrml", "расширение файла vrml", "расширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файла VRML",
  "description":"Узнайте о формате файла VRML и API-интерфейсах, которые могут открывать и создавать файлы VRML.",
  "linktitle" : "VRML",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## .VRML вариант №
Язык моделирования виртуальной реальности (VRML) — это файловый формат для представления интерактивных [3D](/ru/3d/) объектов мира во всемирной паутине (www). Он находит свое применение в создании трехмерных представлений сложных сцен, таких как иллюстрации, определение и презентации виртуальной реальности. Формат был заменен [X3D](/ru/3d/x3d/). Многие приложения для 3D-моделирования могут сохранять объекты и сцены в формате VRML.

## Формат файла VRML

VRML — это формат текстового файла, в котором указывается такая информация, как вершины и ребра трехмерного многоугольника, а также такая информация, как цвет поверхности, текстуры с УФ-отображением, блеск, прозрачность и т. д. Он может представлять статические и анимированные объекты в дополнение к гиперссылкам на другие медиафайлы, такие как звук, фильмы и изображения. Это позволяет открывать элементы с гиперссылками, когда пользователь нажимает на эти объекты.

Файлы TVRML в общепринятой терминологии называются «мирами» и имеют расширение .wrl. Текстовый характер этих файлов позволяет уменьшить размер файла с помощью форматов сжатия, таких как gzip, что делает их более удобными для быстрой передачи через Интернет. Спецификации формата файла для [VRML v 2.0](http://gun.teipir.gr/VRML-amgem/spec/index.html) служат справочным материалом для разработчиков по созданию приложений, совместимых для чтения/записи этих файлов.

## Критерий дизайна ##

Цель и дизайн VRML вращаются вокруг следующих требований.

* **Авторизация** — позволяет разрабатывать генераторы и редакторы приложений, а также импортировать данные из других промышленных форматов.
* **Полнота** — предоставляет всю информацию, необходимую для внедрения, и предоставляет полный набор функций для широкого признания в отрасли.
* **Composability** — возможность использовать элементы VRML в комбинации и, таким образом, обеспечить возможность повторного использования.
* **Расширяемость** — возможность добавлять новые элементы.
* **Реализуемость** - Возможность реализации на широком спектре систем.
* **Многопользовательский потенциал** — не должно препятствовать реализации многопользовательских сред.
* **Ортогональность** — элементы VRML должны быть независимы друг от друга, или любые зависимости должны быть структурированы и четко определены.
* **Производительность** — элементы должны быть разработаны с упором на интерактивную производительность на различных вычислительных платформах.
* **Масштабируемость** — элементы VRML должны быть рассчитаны на бесконечно большие композиции.
* **Стандартная практика** — стандартизировать следует только те элементы, которые отражают существующую практику, необходимы для поддержки существующей практики или необходимы для поддержки предлагаемых стандартов.
* **Хорошо структурированный** — Элемент должен иметь четко определенный интерфейс и просто сформулированную безусловную цель. Следует избегать многоцелевых элементов и побочных эффектов.

## Использованная литература ##

* [VRML — Википедия](https://en.wikipedia.org/wiki/VRML)
* [Спецификации формата файла VRML v 2.0](http://gun.teipir.gr/VRML-amgem/spec/index.html)

