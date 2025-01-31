{
  "date" : "2019-12-10",
  "keywords" :["XLTX", "plik", "rozszerzenie", "format pliku", "Excel Open XML", "Arkusz kalkulacyjny" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Twój przewodnik po formatach plików, aby dowiedzieć się, co to jest plik XLTX i interfejsy API, które mogą je tworzyć i otwierać.",
  "title" :"Co to jest plik XLTX?",
  "linktitle" : "XLTX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Czym jest plik XLTX?

Pliki z rozszerzeniem .xltx reprezentują pliki szablonów programu Microsoft Excel oparte na specyfikacjach formatu plików Office OpenXML. Służy do tworzenia standardowego pliku szablonu, który można wykorzystać do generowania plików [XLSX](/pl/spreadsheet/xlsx/), które mają te same ustawienia, co określone w pliku XLTX.

## Krótka historia

To było na początku 2000 roku, kiedy Microsoft zdecydował się na zmianę, aby dostosować się do standardu **Office Open XML**. Dokumenty różnych typów w ramach tego nowego standardu zostały zidentyfikowane przez dodanie „X” w ich rozszerzeniach, gdzie „X” oznacza XML. Do 2007 roku ten nowy format plików stał się częścią pakietu Office 2007 i jest również stosowany w nowych wersjach pakietu Microsoft Office. Nowy typ pliku ma dodatkowe zalety w postaci małych rozmiarów plików, mniejszej liczby zmian spowodowanych uszkodzeniem i dobrze sformatowanej reprezentacji obrazów.

## Specyfikacje formatu plików XLTX

Pliki XLTX są oparte na formacie plików Office OpenXML i używają XML i [ZIP](/pl/compression/zip/) w celu zmniejszenia rozmiaru pliku. Został stworzony wraz z wydaniem pakietu Microsoft Office 2007 w celu zastąpienia binarnego formatu pliku XLT. Podobnie jak XLTX, formatu XLT można używać do tworzenia plików [XLS](/pl/spreadsheet/xls/) przy użyciu programów Microsoft Excel 2003 i 2007. Można je otwierać w programie Microsoft Excel, klikając dwukrotnie plik. Organizację plików w formacie pliku XLTX można zaobserwować, zmieniając nazwę pliku na ZIP, a następnie wyodrębniając jego zawartość na dysk.

### [Typy_zawartości].xml ###

Jest to jedyny plik znaleziony na poziomie podstawowym podczas rozpakowywania pliku ZIP. Zawiera listę typów zawartości dla części w pakiecie. Wszystkie odniesienia do plików XML zawartych w pakiecie znajdują się w tym pliku XML.

### \_rels (folder) ###

Jest to folder Relationships zawierający pojedynczy plik XML przechowujący relacje na poziomie pakietu. Linki do kluczowych części plików Xltx są zawarte w tym pliku jako identyfikatory URI. Te identyfikatory URI identyfikują typ relacji każdej kluczowej części z pakietem. Obejmuje to związek z głównym dokumentem biurowym znajdującym się jako xl/workbook.xml oraz innymi częściami w docProps jako podstawowe i rozszerzone właściwości.

### docProps ###

Ten folder zawiera ogólne właściwości dokumentu. Obejmują one zestaw podstawowych właściwości, zestaw rozszerzonych lub specyficznych dla aplikacji właściwości oraz miniaturowy podgląd dokumentu. Pusty skoroszyt zawiera dwa pliki w tym folderze, a mianowicie app.xml i core.xml. Plik core.xml zawiera informacje takie jak autor, data utworzenia i zapisania oraz modyfikacji. Plik App.xml zawiera informacje o zawartości pliku.

### xl (folder) ###

Jest to główny folder zawierający wszystkie szczegóły dotyczące zawartości skoroszytu. Domyślnie ma następujące foldery:

* \_rels
* motyw
* karty pracy

oraz następujące pliki xml:

* style.xml
* skoroszyt.xml

## Bibliografia ##

* [[MS-XLSX] — format pliku .Xlsx](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

