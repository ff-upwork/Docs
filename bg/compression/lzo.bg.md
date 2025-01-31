{
  "date" : "2021-06-16",
  "keywords" :[ "LZO", "Компресиран", "Файл", "Разширение", "Файлов формат", "Lempel-Ziv-Oberhume" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZO файлов формат",
  "description":"Научете за файловия формат LZO и API, които могат да създават и отварят LZO файлове.",
  "linktitle" : "LZO",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## Какво е LZO файл? ##

Файл с разширение .lzo се комбинира с функции за архивиране на файлове, които могат да намалят размера на всички файлове в компресирания файл. Всички компресирани файлове могат да включват един или повече файлове или дори групи от класьори с няколко файла от различни видове и размери. Размерът на компресиран файл е по-малък в сравнение с общия размер на всички файлове и папки, съхранени в LZO компресиран файл. Всички LZO компресирани файлове се съхраняват във формат LZO и изрично се изпълняват с функции за компресиране, използвани от софтуера за компресиране и декомпресиране на файлове LZOP. Всички спецификации за компресиране са комбинирани в тази програма за компресиране и декомпресиране на файлове, която произхожда от библиотеката за компресиране на файлове Lempel-Ziv-Oberhume. По-бързата скорост на декомпресия и развитите съотношения на компресия също са комбинирани в тези LZO файлове.

## Спецификация на LZO ##

Markus Franz Xaver Johannes Oberhumer разработи оригиналния алгоритъм "lzop", базиран на по-ранни алгоритми от Abraham Lempel и Jacob Ziv, през 1996 г. Тази библиотека прилага различни алгоритми със следните характеристики:

* По-бързо компресиране от DEFLATE
* Бърза декомпресия
* Допълнителни буфери, които са необходими по време на компресия (с размер 8KB или 64KB, в зависимост от нивото на компресия)
* Изходният и дестинационният буфер са цялата памет, необходима за декомпресия
* Осигурява контрол върху степента на компресия и скоростта на компресия

Като алгоритъм за блокова компресия, LZO извършва припокриваща се компресия, както и декомпресия на място. За да се постигне припокриваща се компресия, размерът на блока за компресиране и декомпресия трябва да съвпада. Алгоритъмът за компресиране на LZO разделя входните данни на съвпадения (плъзгащ се речник) и литерали, които не съвпадат, като дава добри резултати със силно излишни данни и приемливи резултати с некомпресируеми данни, като само увеличава некомпресираните данни с 1/64 от оригинала размер.

## Проблеми при отваряне на LZO файл ##

Следват няколко проблема, които могат да причинят лоша работа на файловия формат LZO:
  


* Файлът може да е повреден. За да разрешите този проблем, изтеглете файла отново или помолете подателя да изпрати отново файла
* Втората причина е заразен файл, в този случай сканирайте правилно файла
* Неправилни връзки към файла LZO
* Премахване на описанието на LZO
* Няма достатъчно хардуерни ресурси
* Остарели драйвери на оборудването
  


## Препратки ##

* [LZO - От Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Oberhumer)

