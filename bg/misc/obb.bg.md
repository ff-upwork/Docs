{
  "date" : "2022-02-16",
  "keywords" :[ "obb файл", "obb файлов формат", "какво е obb файл", "файл", "obb пример", "obb файлово разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OBB файлов формат – Android Opaque Binary Blob файл",
  "description":"Научете за OBB файловия формат и API, които могат да създават и отварят OBB файлове.",
  "linktitle" : "OBB",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-16"
}

## Какво е OBB файл?

OBB файлът е разширителен файл, който съдържа допълнителни данни, които са в допълнение към файла [APK](/bg/compression/apk/) за Android. Google Play Store не позволява да имате APK файл за Android с размер над 100 MB. Но някои приложения може да изискват графики с висока разделителна способност, медийни файлове или други големи активи, които да бъдат хоствани в допълнение към APK файловете. Това е мястото, където идват OBB файловите типове. Google Play позволява прикачването на тези разширителни файлове като допълнение към APK файла.

## OBB файлов формат

OBB файловете се записват като двоични файлове заедно с APK файловете. Когато APK придружава OBB файловете, Google Play хоства разширителните файлове на своя сървър и не се начисляват допълнителни разходи за разработчика. Тези допълнителни файлове се съхраняват в споделеното хранилище на устройството на SD карта или USB-монтируем дял, когато приложението се изтегли за инсталиране.

OBB файловете се изтеглят и инсталират при изтеглянето. Но в някои случаи те се изтеглят за инсталиране, когато приложението се стартира за първи път.

### OBB максимален размер на файла

Google Play Store ви позволява да качвате OBB разширителни файлове с размер до 2 GB. Препоръчва се файлове с голям размер да се качват като компресирани [ZIP](/bg/compression/zip/) файлове за ефективно качване през интернет.

Тези разширителни файлове могат да бъдат хоствани или като **основен** първичен разширителен файл за допълнителни ресурси, изисквани от приложението, или като допълнителен разширителен файл с корекция, предназначен за малки актуализации на основния разширителен файл.

## Препратки

* [Разработчици на Android - Разширителни файлове](https://developer.android.com/google/play/expansion-files)

