{
  "date" : "2019-12-09",
  "keywords" :[ "קובץ zip", "פורמט קובץ zip", "מהו קובץ zip", "קובץ", "דוגמה ל-zip", "סיומת קובץ zip","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"רוכסן",
  "description":"מהו קובץ ZIP וממשקי API שיכולים ליצור ולפתוח קובצי ZIP.",
  "linktitle" : "ZIP",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## מהו קובץ ZIP? ##

קובץ עם סיומת .zip הוא ארכיון שיכול להכיל קבצים או ספריות אחד או יותר. ניתן להחיל דחיסה בארכיון על הקבצים הכלולים על מנת להקטין את גודל קובץ ה-ZIP. פורמט קובץ ZIP פורסם כבר בפברואר 1989 על ידי פיל כץ לצורך השגת ארכיון של קבצים ותיקיות. הפורמט נעשה חלק מתוכנית השירות [PKZIP](https://www.pkware.com/pkzip), שנוצרה על ידי PKWARE, Inc. מיד לאחר הזמינות של [מפרטים זמינים](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT), חברות רבות הפכו את פורמט קובץ ה-ZIP לחלק מכלי התוכנה שלהם, כולל Microsoft (מאז Windows 7), Apple (Mac OS X) ועוד רבים אחרים.

## היסטוריה קצרה של פורמט קובץ ZIP

ההיסטוריה של פורמט קובץ ה-ZIP מתוארכת למקרה של חבילת חוק שהונחה על ידי System Enhancement Associates (SEA) נגד PKWARE על השימוש בכלי השירות שלו ב-ARC ללא הרשאות לסימן המסחרי שלו ולזכויות היוצרים של מראה המוצר וממשק המשתמש. לפני כן, פיל כץ, שכתב את קוד המקור של SEA ושחרר את PKXARC, מחלץ ARC, ו-PKARC, מדחס קבצים, בתור תוכנה חינמית עבור מערכות מבוססות MS-DOS. כשהפסידה בתביעה, PKWARE לא יכלה להשתמש בכל מה שקשור ל-ARC יותר. כאן נוצרה יצירת דחיסת קבצים חדשה, בשם ZIP שנעשתה חלק משירותי PKZIP ב-PKWARE, Inc.

כץ פרסם את מפרטי פורמט קובץ ה-ZIP לרשות הציבור, תוך שמירה על הזכויות הקנייניות על כלי הדחיסה והחילוץ שלו, כלומר PKZIP. מערכת הדחיסה של ZIP הצליחה (ויכולה) לאחסן קבצים בתיקייה באמצעות אלגוריתם של בדיקת יתירות מחזורית של 32 סיביות ([CRC](http://en.wikipedia.org/wiki/Cyclic_redundancy_check)) לדחיסת קובץ גדלים. שלא כמו ARC, תיקיות .ZIP כללו קובץ ספרייה שמילא את התפקיד של ספר קודים של קריפטוגרף, שמכיל את המידע הדרוש לעיבוד הקבצים הדחוסים.

## שיטות דחיסה נתמכות ב-ZIP

לפי מפרטי תבנית קובץ ZIP, שיטות הדחיסה הבאות נתמכות.

* חנות - לא מרמזת על דחיסה
* לצמק
* הפחתה (זה מרמז על גורמי דחיסה הנעים בין רמה 1 לרמה 4)
* להתפוצץ
* לרוקן את האוויר
* Deflat64
* BZIP2
* LZMA (EFS)
* WavPack
* PPMd גרסה I, Rev 1

DEFLATE היא שיטת הדחיסה הנפוצה שהיא אלגוריתם דחיסת תאריכים ללא אובדן המשתמש בשילוב של קידוד LZ77 ו-Huffman והוא מפורט ב-[RFC 1951](https://tools.ietf.org/html/rfc1951).

## מפרט פורמט קובץ ZIP

לקבצי ZIP יש יכולת לאחסן קבצים מרובים באמצעות טכניקות דחיסה שונות ובו זמנית תומכים באחסון קובץ ללא כל דחיסה. כל קובץ מאוחסן/דחוס בנפרד מה שעוזר לחלץ אותם, או להוסיף חדשים, מבלי להחיל דחיסה או דחיסה על הארכיון כולו.

### פורמט קובץ ZIP הכולל

כל קובץ Zip בנוי בצורה הבאה:


|פורמט קובץ ZIP
---|
|כותרת קובץ מקומית 1
|נתוני קובץ 1
|מתאר נתונים 1
|כותרת קובץ מקומית 2
|נתוני קובץ 2
|מתאר נתונים 2
| ....
| ....
|כותרת קובץ מקומית N
|קובץ נתוני N
|מתאר נתונים N
|כותרת פענוח ארכיון
|ארכיון רשומת נתונים נוספת
|מדריך מרכזי

פורמט קובץ ZIP משתמש באלגוריתם CRC של 32 סיביות למטרת אחסון בארכיון. על מנת לרנדר את הקבצים הדחוסים, ארכיון ZIP מחזיק בקצהו ספרייה השומרת את כניסת הקבצים הכלולים ומיקומם בקובץ הארכיון. הוא, לפיכך, ממלא את התפקיד של קידוד לקפסול מידע הדרוש לעיבוד הקבצים הדחוסים. קוראי ZIP משתמשים בספרייה כדי לטעון את רשימת הקבצים מבלי לקרוא את כל ארכיון ה-ZIP. הפורמט שומר עותקים כפולים של מבנה הספריות כדי לספק הגנה טובה יותר מפני אובדן נתונים.

כל קובץ בארכיון ZIP מיוצג כערך בודד כאשר כל ערך מורכב מכותרת קובץ מקומית ואחריה נתוני הקובץ הדחוסים. המדריך שבסוף הארכיון מכיל את ההפניות לכל ערכי הקבצים הללו. קוראי קבצי ZIP צריכים להימנע מקריאת כותרות הקבצים המקומיות ויש לקרוא כל מיני רישום קבצים מהמדריך. ספרייה זו היא המקור היחיד לכניסות קבצים חוקיים בארכיון שכן ניתן לצרף קבצים גם לקראת סוף הארכיון. זו הסיבה שאם קורא קורא כותרות מקומיות של ארכיון ZIP מההתחלה, הוא עשוי לקרוא ערכים לא חוקיים (נמחקו), כמו גם אלה שאינם חלק מהמדריך שנמחק מהארכיון.

סדר כניסות הקבצים בספרייה המרכזית אינו חייב להיות תואם לסדר כניסות הקבצים בארכיון.

### ערכי קובץ ZIP

ערכים בקובץ ZIP מסודרים בזה אחר זה כאשר כל ערך מורכב מ:

* כותרת קובץ מקומית
* שדות נתונים נוספים אופציונליים
* נתוני משתמש (אופציונלי דחוס/אופציונלי מוצפן)

כותרת הקובץ המקומית של כל ערך מייצגת מידע על הקובץ כגון הערה, גודל הקובץ ושם הקובץ. שדות הנתונים הנוספים (אופציונלי) יכולים להכיל מידע עבור אפשרויות הרחבה של פורמט ZIP.

#### כותרת קובץ מקומית

לכותרת הקובץ המקומית יש מבנה שדה ספציפי המורכב מערכי ריבוי בתים. כל הערכים מאוחסנים בסדר בתים קטן-אנדיאן כאשר אורך השדה סופר את האורך בבייטים. כל המבנים בקובץ ZIP משתמשים בחתימות של 4 בתים עבור כל ערך קובץ. הקצה של חתימת הספרייה המרכזית הוא 0x06054b50 וניתן להבחין בה באמצעות חתימה ייחודית משלה. להלן סדר המידע המאוחסן בכותרת הקובץ המקומית.


|היסט|בייטים|תיאור
---|---|---|
|0|4|חתימת כותרת קובץ מקומית # 0x04034b50 (קריאה כמספר אנדיאן קטן)
|4|2|דרושה גרסה לחילוץ (מינימום)
|6|2|דגל סיביות למטרה כללית
|8|2|שיטת דחיסה
|10|2|זמן השינוי האחרון של הקובץ
|12|2|תאריך השינוי האחרון של הקובץ
|14|4|CRC-32
|18|4|גודל דחוס
|22|4|גודל לא דחוס
|26|2|אורך שם הקובץ (n)
|28|2|אורך שדה נוסף (מ')
|30|n|שם הקובץ
|30+n|m|שדה נוסף

#### כותרת קובץ מדריך מרכזי


|היסט|בייטים|תיאור
---|---|---|
|0|4|חתימת כותרת קובץ ספרייה מרכזית # 0x02014b50
|4|2|גרסה שנעשתה על ידי
|6|2|דרושה גרסה לחילוץ (מינימום)
|8|2|דגל סיביות למטרה כללית
|10|2|שיטת דחיסה
|12|2|זמן השינוי האחרון של הקובץ
|14|2|תאריך השינוי האחרון של הקובץ
|16|4|CRC-32
|20|4|גודל דחוס
|24|4|גודל לא דחוס
|28|2|אורך שם הקובץ (n)
|30|2|אורך שדה נוסף (מ')
|32|2|אורך הערת הקובץ (k)
|34|2|מספר דיסק שבו הקובץ מתחיל
|36|2|תכונות קובץ פנימיות
|38|4|תכונות קובץ חיצוניות
|42|4|היסט יחסי של כותרת הקובץ המקומית. זהו מספר הבתים בין תחילת הדיסק הראשון שבו הקובץ מתרחש, לבין תחילת כותרת הקובץ המקומי. זה מאפשר לתוכנה שקוראת את הספרייה המרכזית לאתר את מיקום הקובץ בתוך קובץ ה-ZIP.
|46|n|שם הקובץ
|46+n|m|שדה נוסף
|46+n+m|k|תגובה לקובץ

#### סוף רשומת המדריך המרכזי


|היסט|בייטים|תיאור
---|---|---|
|0|4|חתימת סוף הספרייה המרכזית # 0x06054b50
|4|2|מספר של דיסק זה
|6|2|דיסק שבו מתחילה ספרייה מרכזית
|8|2|מספר רשומות ספריות מרכזיות בדיסק זה
|10|2|מספר כולל של רשומות ספריות מרכזיות
|12|4|גודל הספרייה המרכזית (בתים)
|16|4|קיזוז של תחילת הספרייה המרכזית, ביחס לתחילת הארכיון
|20|2|אורך התגובה (n)
|22|n|תגובה

## הפניות

* [מפרט פורמט קובץ ZIP של PKWARE](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT)
* [מבנה של קובץ PKZip](https://users.cs.jmu.edu/buchhofp/forensics/formats/pkzip-printable.html)