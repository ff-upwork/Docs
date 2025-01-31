{
  "date" : "2021-04-08",
  "keywords" :[ "файл mst", "формат файлу mst", "що таке файл mst", "файл", "приклад mst", "розширення файлу mst", "розширення", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
	

},
  "draft" : "false",
  "toc" : true,
  "title" :"LBR - LU Library Archive Format",
  "description":"Дізнайтеся про формат файлу LBR та API, які можуть створювати та відкривати файли LBR.",
  "linktitle" : "LBR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Що таке файл LBR?

Файл із розширенням .lbr — це архівний файл, створений за допомогою програми LU та використовувався в операційних системах CP/M і DOS протягом 1980-х років. Він більше не використовується і був замінений на сучасні формати архівних файлів. Формат не стискає файли-учасники та діє як архів контейнера для них. Функція архівування здебільшого використовувалася для передачі заархівованих файлів через Інтернет. Оскільки LBR не пропонував стиснення, інші утиліти, такі як SQ або CRUNCH, використовувалися для стиснення членських файлів перед архівуванням або отриманого архівного файлу після архівування, щоб зменшити його розмір.

## Формат файлу LBR

Формат файлу LBR розроблений Гері П. Новосільським і не містить загальнодоступних технічних деталей. Файли LBR починаються з байта 0x00, за яким йде 11 пробілів (0x20), потім два байти 0x00, потім два байти, які не є 0x00. Будучи контейнерним форматом файлу, його можна розпакувати за допомогою LU.COM і NULU.COM.

## Список літератури

* [LBR – Вікіпедія](https://en.wikipedia.org/wiki/LBR_(file_format))

