{
  "date" : "2020-01-10",
  "keywords" :[ "קובץ dib", "פורמט קובץ dib", "מהו קובץ dib", "קובץ", "דוגמה dib", "סיומת קובץ dib","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DIB",
  "description":"למד על פורמט קבצי DIB וממשקי API שיכולים ליצור ולפתוח קובצי DIB.",
  "linktitle" : "DIB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## מהו קובץ DIB?

מפת סיביות בלתי תלויה בהתקן (DIB) היא קובץ תמונת רסטר הדומה במבנה לקובצי Bitmap הסטנדרטיים ([BMP]()/image/bmp/)). הוא מכיל טבלת צבעים המתארת את המיפוי של צבעי RGB לערכי הפיקסלים. זה מאפשר ל-DIB לייצג תמונה בכל מכשיר. ניתן לפתוח אותו כמעט עם כל היישומים שיכולים לפתוח קובץ BMP סטנדרטי ב-Windows כמו גם ב-macOS. DIB הם קבצים בינאריים ובעלי פורמט קובץ מורכב הדומה ל-BMP. תמונות DIB אינן תלויות ביכולות הפלט של מכשירי רינדור מבחינת עומק צבע ופיקסל לאינץ'.

## מפרטי פורמט קובץ DIB ##
DIB מכיל את מידע הצבע והממדים הבאים:

* פורמט הצבע של המכשיר עליו נוצרה התמונה המלבנית.
* הרזולוציה של המכשיר עליו נוצרה התמונה המלבנית.
* הפלטה של המכשיר בו נוצרה התמונה.
* מערך ביטים הממפה שלשות אדום, ירוק, כחול (RGB) לפיקסלים בתמונה המלבנית.
* מזהה דחיסת נתונים המציין את ערכת דחיסת הנתונים (אם קיימת) המשמשת להקטנת גודל מערך הביטים.

### פורמט DIB Block Data ###

DIB מגיע בהקשר של בלוק זיכרון בהשוואה לקבצי .DIB המאוחסנים בדיסק. בלוק הזיכרון מורכב ממבנה התואם למפרטי Windows API עבור DIBs. DIB בפועל מורכב מ:
* כותרת עליונה
* פלטת צבעים
* נתוני פיקסלים

מעשית, העבודה עם נתוני לוח, כותרת ותמונה נעשית כאילו היו שלושה בלוקים נפרדים של זיכרון. ידית אחיזה לבלוק זיכרון נפוץ זה מוקצית באמצעות GlobalAlloc ומכונה HDIB, המשמשת לחילוץ ולעבודה עם נתוני הכותרת, טבלת הצבעים ונתוני הפיקסלים.

### מבנים ###
מידע הכלול ב-DIB מיוצג על ידי מבנים שונים. אלו כוללים:

BITMAPInfo - מגדיר את מידע הממד והצבע עבור DIBs
```
typedef struct tagBITMAPINFO {
  BITMAPINFOHEADER bmiHeader;
  RGBQUAD          bmiColors[1];
} BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO;
```
הוא מורכב מ-BITMAPINFOHEADER:

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
ואחריו שניים או יותר מבני RGBQAD.

```
typedef struct tagRGBQUAD {
  BYTE rgbBlue;
  BYTE rgbGreen;
  BYTE rgbRed;
  BYTE rgbReserved;
} RGBQUAD;
```
### פיסות מידע ###
|Bits|תיאור|
---|---|
|פורמט 1 סיביות (מונוכרום)|מפות סיביות מונוכרומיות מורכבות משני צבעים (שחור ולבן). בשל מספר מצומצם זה של צבעים, מפות סיביות אלו תופסות פחות מקום בדיסק. ה-bitBitCount מחזיר אמת או שקר לייצוג של שני הצבעים. רוב היישומים מדלגים לחלוטין על הפלטה אם bitBitCount==1.
| פורמט 4 סיביות (VGA או 16 צבעים)|כל בייט של נתוני תמונה מייצג שני פיקסלים ו-bitBitCount==4. סיביות אלו מייצגות את צבע הפיקסל בסדר יורד.
|פורמט 8 סיביות (256 צבעים)|פורמט 8 סיביות זה יכול לייצג מקסימום 256 צבעים. כל בייט במערך נתוני מפת הסיביות של התמונה מייצג פיקסל בודד. הערך של אותו בייט הוא המספר של ערך לוח הצבעים שיש להשתמש בו מתוך 256 הערכים כפי שיוצגו על ידי ה-bmciColors.
|פורמט של 24 סיביות (TrueColor)|מפות סיביות אלה יכולות להכיל מקסימום 2^24 צבעים (biBitCount == 24). כל רצף של שלושה בתים במערך הנתונים של מפת סיביות מייצג את העוצמות היחסיות של שלושת הגוונים העיקריים של פיקסל. הגוונים מתוארים כערכים הנעים בין 0 ל-255 ומאוחסנים בשלושת הבתים בסדר כחול, ירוק ואדום. זוהי הבחנה חשובה, מכיוון שרוב ההפניות לצבעים ב-Windows משתמשות בסדר הפוך: אדום/ירוק/כחול, אז חשבו "BGR" כשעובדים עם תמונות TrueColor במקום "RGB". ניתן לציין פלטת צבעים כדי להאיץ את תהליך הציור עבור Windows, ובמקרה זה biClrUsed לא יהיה 0. אבל כפי שאתה יכול לראות, זה לא נחוץ, מכיוון שנתוני הפיקסלים עצמם מכילים את מידע הצבע.
|פורמט 32 סיביות|לתמונות 32 סיביות יש לכל היותר 2^24 צבעים (biBitCount == 24).

## הפניות ##
* [מפות סיביות בלתי תלויות בהתקן - מאת Microsoft](https://learn.microsoft.com/en-us/windows/win32/gdi/device-independent-bitmaps)

