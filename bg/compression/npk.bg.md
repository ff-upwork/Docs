{
  "date" : "2022-06-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NPK файлов формат",
  "description":"Научете за файловия формат NPK и API, които могат да създават и отварят NPK файлове.",
  "linktitle" : "NPK",
  "menu" : {
    "docs" : {
      "identifier":"compression-npk",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-21"
}

## Какво е NPK файл?

NPK файлът е файл с пакет за надграждане на софтуер, използван от рутери **MikroTik** за надграждане на операционната система на рутера. Той идва като компресиран двоичен архив, който се зарежда в рутера за инсталиране на софтуерни актуализации. Информацията, съдържаща се в NPK файлове, включва мрежова информация като IP адрес и IP услуга, информация за конектори (ethernet интерфейси и сериен порт), настройка на имейл, конфигурация на мост и управление на локални потребители.

## NPK файлов формат

NPK файловете се съхраняват като компресиран двоичен архив. Това е затворен файлов формат, който се използва само от самите MikroTik. Не е предназначен за създаване на RouterOS добавки чрез трети страни. NPK файловете се поддържат от самия MikroTik и надстроени версии на същите могат да бъдат изтеглени от секциите за изтегляне на уебсайта [MikroTik](https://mikrotik.com/download).

Когато NPK файл се качи на рутер, операционната система на рутера не влиза в сила, освен ако не се рестартира. Следователно е необходимо рестартиране, за да може операционната система на рутера да бъде надстроена.

## Препратки

* [MikroTik - Надграждане на операционната система на рутера](https://mikrotik.com/download)
* [Как да създадете NPK файлове](https://forum.mikrotik.com/viewtopic.php?t=87126)

