{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл ATOM – Формат за синдикиране на Atom",
  "description" :"Научете какво е ATOM файл и API, които могат да създават и отварят ATOM файлове.",
  "linktitle" : "ATOM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## Какво е ATOM файл?

ATOM файлът е формат за синдикиране за структурата на Atom канали и документи за въвеждане. Подобно на .RSS файловете, файловият формат ATOM е базиран на XML формат за синдикиране, който е стандарт за публикуване на съдържание. ATOM файл се използва за уеб емисии, които позволяват на софтуерните програми да проверяват за актуализации, публикувани на уебсайта. Той съдържа записи, които могат да бъдат от различни типове, като заглавия, статии с пълен текст, извадки или връзки към съдържание на уебсайт

Приложенията, които могат да **отварят ATOM файлове** включват **Apple Safari**.

## ATOM файлов формат - повече информация

ATOM файловете се съхраняват и публикуват в популярния XML файлов формат, който е универсален формат за обмен на информация. Той е разработен като алтернатива на RSS, като се имат предвид ограниченията и недостатъците на RSS файловия формат.

### Типове Atom документи

1. `Atom Entry Documents` - Това е XML документ, който се състои от един елемент информация, известен като вход, за Atom емисията. Разполага с atom-entry елемент, който съдържа редица дъщерни елементи. Съдържанието на запис в Atom може да бъде обикновен текст, HTML, XHTML или друг тип медия IANA (Internet Assigned Numbers Authority).
1. `Atom Feed Documents` - Това е XML документ, който предоставя метаданни за Atom емисия и един или повече записи за емисия. Когато клиент направи заявка за информация от емисията, документът за емисията се генерира от сървъра, който включва редица Atom записи за изпълнение на заявката.
1. `Колекция Atom` - Това е специален вид документ за подаване на Atom, който съдържа URL адресите на Atom записи, които са достъпни за редактиране.

## Препратки

* [Формат за синдикиране на Atom - RFC](https://www.rfc-editor.org/rfc/rfc4287.html)
* [Общ преглед на Atom Feeds - IBM](https://www.ibm.com/docs/en/cics-ts/5.4?topic=support-overview-atom-feeds)
* [Atom - уеб стандарт](https://en.wikipedia.org/wiki/Atom_(web_standard))

