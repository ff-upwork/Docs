{
  "date" : "2021-03-12",
  "keywords" :[ "VP9", "Файл", "Разширение", "Файлов формат", "Видео формат", "TrueMotion Video", "VPX", "On2 Technologies"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP9 – видео файл TrueMotion",
  "description":"Научете за VP9 файлов формат и API, които могат да създават и отварят VP9 файлове.",
  "linktitle" : "VP9",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-27"
}

## Какво е VP9 файл?

Google разработи кодека VP9 като безплатен стандарт за кодиране на видео с отворен код като наследник на VP8. Първоначално е проектиран да компресира ултра HD съдържание в YouTube, тъй като разширява и подобрява ефективността на кодиране на своя предшественик. Ако говорим за оригиналните VPX кодеци, те идват от On2 Technologies, които бяха асимилирани от Google през 2010 г. Google по-късно отвори кодека. VP8 и VP9 и двата формата се предлагат под безплатен BSD лиценз, който позволява на операторите да организират умения за кодиране или декодиране както в ексклузивен софтуер, така и в софтуер с отворен код, без да разкриват техния изходен код.

## Технически характеристики на VP9

* VP9 предоставя максимална разделителна способност от 8192x4352 при до 120 fps и множество цветови пространства, с Rec 601, Rec 709, Rec 2020, SMPTE-170, SMPTE-240 и sRGB
* Пълната гама от случаи на уеб и мобилна употреба от компресия с нисък битрейт до висококачествен ултра-HD, с допълнителна поддръжка за 10/12-битово кодиране и HDR, се поддържат напълно от този формат
* Може да намали битрейта на видео с до 50% в сравнение с други
* Подготвен е за адаптивен стрийминг и се използва от YouTube и други известни доставчици на уеб видео
* Устройствата Chrome, Opera, Edge, Firefox и Android, както и милиони смарт телевизори поддържат декодирането на този кодек
* Видео резолюциите, по-големи от 1080p, се модифицират чрез VP9 и позволяват компресия без загуби
* Различни цветови пространства като Rec. 601, Rec. 709, Rec. 2020, SMPTE-170, SMPTE-240 и sRGB се поддържат от VP9
* HDR видео, използващо Hybrid Log-Gamma и Perceptual Quantizer, също може да се поддържа от VP9


## Кратка история

* Разработката на видео кодек VP9 започна през 2011 г. и неговият декодер беше добавен към уеб браузъра Chromium през декември 2012 г.
* Първата му версия на уеб браузъра Google Chrome беше пусната през февруари 2013 г. и по това време пусна декодиране
* Google пусна Chrome 29.0.1547 с окончателна поддръжка на VP9 през август 2013 г.
* През октомври 2013 г. към FFmpeg беше добавен инстинктивен VP9 декодер
* Mozilla добави поддръжка на VP9 към Firefox през декември 2013 г. във версия 2, която беше пусната на 18 март 2014 г.
 

## Работа на VP9

Обикновено 4K видеото повишава качеството на картината, като прави конкретни пиксели по-малки, кодекът VP9 и HEVC ги правят по-големи, за да намалят битрейта и размера на файла. Въпреки че това може да изглежда противоречиво, механизмът за кодиране взема по-големите пиксели и ги променя в по-добра разделителна способност. Изходното видео, включващо видео кадри, се кодира или компресира, за да се получи компресиран битов видео поток. Всеки отделен кадър първо се разделя на блокове от пиксели. След това блоковете се изследват внимателно за триизмерни отхвърляния и последователните връзки между кадрите се оценяват, за да се възползват от области, които не могат да бъдат променени. Те са кодирани чрез вектори на движение, които гарантират качествата на дадения блок на следващия кадър. Остатъчната информация се кодира с помощта на ефективна двоична компресия.

## Препратки

* [VP9 Wikipedia](https://en.wikipedia.org/wiki/VP9)
* [Уеб документи на MDN](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Video_codecs#vp9)
* [Кокос](https://www.coconut.co/)

