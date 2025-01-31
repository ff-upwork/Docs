{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MDMP файл – Windows Minidump файлов формат",
  "description":"Научете за MDMP файловия формат и API, които могат да създават и отварят MDMP файлове.",
  "linktitle" : "MDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## Какво е MDMP файл?

MDMP файлът е дъмп на паметта на приложение в Microsoft Windows, който се създава, когато приложението се затвори необичайно или се срине. Той съдържа информация и изхвърляния на данни, които могат да се използват за отстраняване на грешки на причината за срива. MDMP файловете са приложими за приложения, създадени от всяка платформа като Java, C++, .NET и други. В допълнение към MDMP,

Приложенията, които могат да отварят MDMP файлове, включват Microsoft Visual Studio Debugger.

## MDMP файлов формат

MDMP файловете се записват като двоични файлове на диск и могат да се отварят с програмата за отстраняване на грешки на Microsoft Visual Studio. Той съдържа следната информация, за да ви помогне да идентифицирате причината за срива.

* Подробности за съобщението Stop, неговите параметри и други данни
* Списък на заредените драйвери
* Контекст на процесора (PRCB) за процесора, който е спрял да работи
* Информация за процеса и контекст на ядрото (EPROCESS) за процеса, който е спрял
* Информация за процеса и контекст на ядрото (ETHREAD) за нишката, която е спряла
* Стек за извикване в режим на ядрото за нишката, която е спряла

Тази информация помага да разберете какво се е случило, да коригирате проблема и да предотвратите повторната му поява.

### Анализирайте Minidump

Windows изисква файл за пейджинг на тома за зареждане, за да създаде файл за дъмп на паметта. Файлът за виртуална памет се създава на зареждащия том и трябва да е с размер поне 2 мегабайта (MB). Dump файлът се създава, когато дадено приложение се срине. В случай на втори проблем се създава втори малък дъмп файл на паметта, докато предишният се запазва. Името на дъмп файла е различно, за да се избегне презаписване.

Windows поддържа списък с всички дъмп файлове на паметта в папката %SystemRoot%\Minidump. Можете да анализирате MDMP файлове, като ги стартирате в Visual Studio Debugger, както е посочено в стъпките по-долу.

## Как да отворя MDMP файл във Visual Studio?

Следните стъпки могат да се използват за отваряне на MDMP файл във Visual Studio.

* Във Visual Studio от менюто File изберете Open | Изхвърляне при срив.
* Придвижете се до дъмп файла, който искате да отворите.
* Изберете Отваряне.

## справка

* [Как да прочетем малкия дъмп файл на паметта, който е създаден от Windows, ако възникне срив](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

