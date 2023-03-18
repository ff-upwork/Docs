{
  "date" : "2021-04-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файлов формат SIFZ – Компресиран проектен файл на Synfig Studio",
  "description":"Научете за файловия формат SIFZ и API, които могат да създават и отварят SIFZ файлове.",
  "linktitle" : "SIFZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-30"
}

## Какво е SIFZ файл?

SIFZ файлът е gzip компресиран SIF файл, създаден от приложението за създаване на 2d анимации с отворен код **Synfig Studio**. Той съдържа множество графични елементи, които съставляват анимацията. Цялостното съдържание на анимацията е изградено с помощта на комбинация от платно, което е изпълнено с форми, щрихи с четка или молив и текст. Всички те са подредени на свои собствени позиции, манипулатори за радиус, допирателна, ъгъл, връх и ширина. SIFZ файловете могат да се отварят с [Synfig Studio](https://www.synfig.org/).

## SIFZ файлов формат

SIFZ файловете са компресирани [ZIP](/bg/компресия/zip/) файлове, които са пакетирани с помощта на метода за компресиране gzip. Synfig се използва за създаване на анимации с филмово качество, като се използват векторни и растерни изображения. За разлика от стария метод за създаване на анимация кадър по кадър, той ви позволява да създавате 2D анимации с по-високо качество с по-малко ресурси.

SIFZ файловете, когато са компресирани, са по-малки от некомпресираните SIF файлове. Това също улеснява прехвърлянето през интернет връзки с ниска честотна лента.

## Препратки

* [Synfig с отворен код - Github](https://github.com/synfig/synfig/)
* [Документация на Synfig](https://synfig.readthedocs.io/en/latest/index.html)
