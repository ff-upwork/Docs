{
  "date" : "2020-01-10",
  "keywords" :[ "dib файл", "dib файлов формат", "какво е dib файл", "файл", "dib пример", "dib файлово разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DIB",
  "description":"Научете за файловия формат DIB и API, които могат да създават и отварят DIB файлове.",
  "linktitle" : "DIB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## Какво е DIB файл?

Независимото от устройството растерно изображение (DIB) е файл с растерно изображение, който е подобен по структура на стандартните файлове с растерно изображение ([BMP]()/image/bmp/)). Той съдържа цветова таблица, която описва картографирането на RGB цветове към стойностите на пикселите. Това позволява на DIB да представя изображение на всяко устройство. Може да се отваря с почти всички приложения, които могат да отварят стандартен BMP файл в Windows, както и в macOS. DIB са двоични файлове и имат сложен файлов формат, подобен на BMP. DIB изображенията са независими от изходните възможности на устройствата за изобразяване по отношение на дълбочината на цвета и пиксел на инч.

## Спецификации на DIB файлов формат ##
DIB съдържа следната информация за цвят и размери:

* Цветовият формат на устройството, на което е създадено правоъгълното изображение.
* Разделителната способност на устройството, на което е създадено правоъгълното изображение.
* Палитрата за устройството, на което е създадено изображението.
* Масив от битове, който картографира червени, зелени, сини (RGB) триплети към пиксели в правоъгълното изображение.
* Идентификатор за компресиране на данни, който показва схемата за компресиране на данни (ако има такава), използвана за намаляване на размера на масива от битове.

### Формат на DIB блок данни ###

DIB идва в контекста на блок памет в сравнение с .DIB файлове, съхранени на диск. Блокът памет се състои от структура, която е в съответствие със спецификациите на Windows API за DIB. Действителният DIB се състои от:
* Заглавка
* Цветова палитра
* Пикселни данни

Практически работата с данни за палета, заглавие и изображение се извършва като три отделни блока памет. Манипулаторът на този общ блок памет се присвоява с помощта на GlobalAlloc и е известен като HDIB, който се използва за извличане и работа със заглавката, цветната таблица и пикселните данни.

### Структури ###
Информацията, съдържаща се в DIB, е представена от различни структури. Те включват:

BITMAPInfo - Дефинира информацията за размера и цвета за DIB
```
typedef struct tagBITMAPINFO {
  BITMAPINFOHEADER bmiHeader;
  RGBQUAD          bmiColors[1];
} BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO;
```
Състои се от BITMAPINFOHEADER:

```
typedef struct tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} BITMAPINFOHEADER, *PBITMAPINFOHEADER;
```
последвано от две или повече RGBQAD структури.

```
typedef struct tagRGBQUAD {
  BYTE rgbBlue;
  BYTE rgbGreen;
  BYTE rgbRed;
  BYTE rgbReserved;
} RGBQUAD;
```
### Битове данни ###
|Битове|Описание|
---|---|
|1-битов формат (монохромен)|Монохромните растерни изображения се състоят от два цвята (черен и бял). Поради този ограничен брой цветове, тези растерни изображения заемат по-малко място на диска. BitBitCount връща true или false за представяне и на двата цвята. Повечето от приложенията пропускат напълно палитрата, ако bitBitCount==1.
|4 битов формат (VGA или 16 цвята)|Всеки байт данни за изображението представлява два пиксела и bitBitCount==4. Тези битове представляват цвета на пиксела в низходящ ред.
|8-битов формат (256 цвята)|Този 8-битов формат може да представи максимум 256 цвята. Всеки байт в масива от растерни данни на изображението представлява един пиксел. Стойността на този байт е номерът на записа в цветовата палитра, който трябва да се използва от 256 записа, представени от bmciColors.
|24-битов формат (TrueColor)|Тези растерни изображения могат да имат максимум 2^24 цвята (biBitCount == 24). Всяка трибайтова последователност в масива от данни за растерни изображения представлява относителните интензитети на трите основни нюанса на пиксел. Нюансите се описват като стойности в диапазона от 0 до 255 и се съхраняват в трите байта в реда Синьо, Зелено и Червено. Това е важно разграничение, тъй като повечето препратки към цветовете в Windows използват обратния ред: червено/зелено/синьо, така че мислете за „BGR“, когато работите с изображения TrueColor, вместо за „RGB“. Може да бъде зададена цветова палитра, за да се ускори процеса на рисуване за Windows, в който случай biClrUsed няма да бъде 0. Но както можете да видите, това не е необходимо, тъй като самите пикселни данни съдържат информация за цвета.
|32-битов формат|32-битовите изображения имат максимум 2^24 цвята (biBitCount == 24).

## Препратки ##
* [Независими от устройство растерни изображения - от Microsoft](https://learn.microsoft.com/en-us/windows/win32/gdi/device-independent-bitmaps)

