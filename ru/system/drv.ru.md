{
  "date" : "2021-07-08",
  "keywords" :[ "DRV", "расширение", "файл", "формат", "система", "драйвер", "драйвер устройства Windows", "программы", "компьютер", "приложение" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRV — драйвер устройства Windows",
  "description":"Узнайте о формате файла DRV и API-интерфейсах, которые могут создавать и открывать файлы DRV.",
  "linktitle" : "DRV",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## .DRV вариант № ##

Файлы с расширением .drv относятся к драйверу устройств Windows. Операционная система Windows использует эти файлы для подключения внутренних и внешних жестких устройств. Файлы DRV состоят из инструкций и параметров того, как устройство и операционная система связываются друг с другом. Эти файлы помогают установить драйверы устройств для правильной работы с Windows. Кроме того, для устройств, подключенных к материнской плате ПК через шину или кабель, требуются файлы DRV.


## Формат файла DRV ##

Файлы DRV обычно упаковываются в виде файлов динамических библиотек (файлы [DDL](/ru/system/dll/)) или [EXE](/ru/executable/exe/). Эти файлы могут поддерживаться на всех системных платформах, таких как смартфоны, и нет гарантии, что каждая платформа будет правильно поддерживать эти файлы. Однако некоторые наиболее распространенные устройства, использующие расширение файла .drv:

* Звуковые карты
* Графические карты
* Принтеры
* Устройства хранения данных
* Сетевые адаптеры
* Аксессуары для компьютерной техники

Не рекомендуется открывать файлы DRV, отправленные по электронной почте, поскольку этот формат файла содержит вирусы и другие вредоносные программы. Обязательно выполните всестороннее сканирование перед открытием любого неизвестного файла DRV.


## Пример ДРВ ##

```
// Include necessary files...
#include <font.defs>
#include <media.defs>
#include <hp.h>
#include <epson.h>
#include <label.h>

// Localizations are provided for all of the base languages supported by
// CUPS...
#po ar ""
#po ca ""
#po de ""
#po el ""
#po es ""
#po fr ""
#po no ""
#po ru ""
#po sk ""
#po sv ""
#po th ""
#po tr ""
#po uk ""

// MediaSize sizes used by label drivers...
#media "w90h18/1.25x0.25\"" 90 18
#media "w90h162/1.25x2.25\"" 90 162
#media "w108h18/1.50x0.25\"" 108 18
#media "w108h36/1.50x0.50\"" 108 36
#media "w108h72/1.50x1.00\"" 108 72
#media "w108h144/1.50x2.00\"" 108 144
#media "w144h26/2.00x0.37\"" 144 26
#media "w576h360/8.00x5.00\"" 576 360
#media "w576h432/8.00x6.00\"" 576 432
#media "w576h468/8.00x6.50\"" 576 468

// Common stuff for all drivers...
Attribute "cupsVersion" "" "2.2"
Attribute "FileSystem" "" "False"
Attribute "LandscapeOrientation" "" "Plus90"
Attribute "TTRasterizer" "" "Type42"

Font *

Version "2.1"

// Dymo Label Printer
{
  Manufacturer "Dymo"
  ModelName "Label Printer"
  Attribute NickName "" "Dymo Label Printer"
  PCFileName "dymo.ppd"
  DriverType label
  ModelNumber $DYMO_3x0
  Throughput 8
  ManualCopies Yes
  ColorDevice No

  HWMargins 2 14.9 2 14.9

  *MediaSize w81h252
  MediaSize w101h252
  MediaSize w54h144
  MediaSize w167h288
  MediaSize w162h540
  MediaSize w162h504
  MediaSize w41h248
  MediaSize w41h144
  MediaSize w153h198

  Resolution k 1 0 0 0 136dpi
  Resolution k 1 0 0 0 203dpi
  *Resolution k 1 0 0 0 300dpi

  Darkness 0 Light
  Darkness 1 Medium
  *Darkness 2 Normal
  Darkness 3 Dark
}

```

