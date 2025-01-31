{
  "date" : "2019-10-11",
  "keywords" :[ "gbr файл", "gbr файлов формат", "какво е gbr файл", "файл", "gbr пример", "gbr файлово разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GBR файлов формат - Gerber файлов формат за PCB",
  "description":"Научете за GBR файловия формат и API, които могат да създават и отварят GBR файлове.",
  "linktitle" : "GBR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Какво е GBR файл?

Файл с разширение .gbr е файлов формат на Gerber за обмен на данни за дизайн на печатни платки (PCB). Разработен е от Ucamco. Данните за проектиране на печатни платки са основният компонент, изискван от производствената индустрия за работа. GRB файлът съдържа данни за PCB като медни слоеве, маска за запояване, легенда и данни за пробиване и маршрут. Може да се използва за прехвърляне на данни като производствени характеристики на печатни платки, включително дебелина или покритие в стандартизиран формат. Всички системи за проектиране на печатни платки извеждат Gerber файлове, които могат да се обработват от системи за производство на печатни платки. GBR файловете вече се превърнаха в де факто стандарт за трансфер на данни за проектиране на печатни платки (PCB). Ucamco предостави [безплатна онлайн програма за преглед](https://gerber-viewer.ucamco.com/) за отваряне и преглед на GBR файлови формати.

## GBR файлов формат

GBR е UTF-8 четим от човека формат, който се състои само от 27 команди. Благодарение на този кратък списък от команди и неговата компактност, GBR е лесен за отстраняване на грешки. В основата си Gerber е отворен векторен формат за 2D бинарни изображения. Метаинформацията се прехвърля с изображенията чрез атрибути. Един GRB файл определя едно изображение и не изисква никакви придружаващи файлове или външни параметри, за да бъдат интерпретирани. Едно изображение се нуждае само от един файл. Той използва 7-битови ASCII знаци за всички команди и имена, дефинирани в спецификацията, които могат да бъдат отпечатани. Това напълно покрива пълното генериране на изображения.

### Примерен GBR файл

Следва примерен Gerber файл, който създава кръг с диаметър 1,5 mm, центриран в началото. Има една команда на ред.

```
%FSLAX26Y26*%
%MOMM*%
%ADD   100C,1.5*%
D100* X0Y0D03*
M02*
```

## Препратки

* [формат Gerber](https://www.ucamco.com/en/gerber)

