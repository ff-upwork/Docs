{
  "date" : "2021-07-18",
  "keywords" :[ "LOC", "файл", "розширення", "формат файлу", "Розташування GPS", "Шляхова точка"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LOC - формат файлу розташування GPS",
  "description":"Дізнайтеся про формат файлу LOC та API, які можуть створювати та відкривати файли LOC.",
  "linktitle" : "LOC",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-18"
}

## Що таке файл LOC?

Файл із розширенням .loc — це файл розташування GPS, який містить геопросторові розташування як маршрутні точки. Маршрутна точка – це пара значень широти та довготи, які вказують на місце розташування, яке використовується програмами Географічної інформаційної системи (ГІС). Програми картографування GPS, такі як DeLorme Topo, використовують файли LOC для читання та відображення інформації, що міститься в цих файлах LOC, у вигляді шарів, які можна вибрати кінцевим користувачам. Крім того, вони використовуються для обміну даними GPS між програмами. Файли LOC можна відкрити за допомогою таких програм, як [TopoGrafix EasyGPS](https://www.easygps.com/), які відображають вміст таких файлів як шари та дані, нанесені на карту у відповідному геолокації.

## Формат файлу LOC - Додаткова інформація

Файли LOC схожі на файли [GPX](/uk/gis/gpx/), але зберігаються в іншому форматі. Вони зберігаються як [XML](/uk/web/xml/) файли, де вміст маршрутних точок і пов’язана інформація містяться в структурованих тегах. Оскільки XML є узагальненою мовою для обміну даними між різними програмами, це полегшує обмін даними LOC з іншими програмами.

## Формат файлу LOC – приклад

Нижче наведено заголовок і текст однієї маршрутної точки з файлу LOC. Як видно, інформація заголовка містить джерело розташування даних. Маршрутна точка містить таку інформацію, як «ID» і пов’язані з нею дані вмісту. Нарешті, маршрутна точка – це набір значень широти та довготи та текст, пов’язаний із цією конкретною маршрутною точкою.

```
<?xml version="1.0" encoding="UTF-8"?>

<loc version="1.0" src="Groundspeak">

<waypoint>

<name id="GCGFTA"><![CDATA[The Volunteer Cache or Find The Bridge by Eagle Son]]></name>

<coord lat="41.6965166666667" lon="-88.1080166666667"/>

<type>Geocache</type>
<link text="Cache Details">http://www.geocaching.com/seek/cache_details.aspx?wp=GCGFTA</link>

</waypoint>
```

## Список літератури

* [TopGraphic EasyGPS](https://www.easygps.com/)

