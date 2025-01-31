{
  "date" : "2021-08-24",
  "keywords" :[ "קובץ wdb", "פורמט קובץ wdb", "מהו קובץ wdb", "קובץ", "דוגמה ל-wdb", "סיומת קובץ wdb","סיומת", "פורמט" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"למד על פורמט קובץ WDB וממשקי API שיכולים ליצור ולפתוח קבצי WDB.",
  "title" :"WDB - SQL Server Trace File",
  "linktitle" : "WDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-24"
}

## מהו קובץ WDB?
קובץ עם סיומת .wdb הוא למעשה קובץ מסד נתונים שנוצר על ידי Microsoft Works אשר שימש לביצוע פונקציות כמו מערכת ניהול מסד נתונים. קובץ WDB דומה לקובץ Access Database ([MDB](/he/database/mdb/)), אך פחות יעיל ומגבלות גדולות יותר. לא ניתן לפתוח את קבצי WDB באמצעות Microsoft Access. עם זאת, אתה יכול לפתוח את קובץ WDB ב-Microsoft Works ולאחר מכן לייצא אותו לקובץ MDB, על מנת לפתוח קובץ WDB ב-MS Access.

## פורמט קובץ WDB
Microsoft Works Database הוא פורמט מסד הנתונים המקורי של חבילת המשרד של Microsoft Works. בגלל האופי הקנייני של הפורמט וכמה מגבלות. לא ניתן לפתוח את קבצי WDB בשום תוכנה אחרת מלבד Microsoft Works. בתבנית הקובץ ניתן למצוא כותרת חוזרת של 10 בתים לפני כל אחת ממחרוזות הטקסט של ASCII המייצגות את ערכי השדות שנסתיימו על ידי ערך NULL. הכותרת מתחילה בדרך כלל עם **\x0f** בתים ו-NULL, ואחריו 4 בתים של נתונים לסירוגין עם NULLs.

### מבנה הקובץ

המבנה של קובץ WDB ניתן להלן:
- **כותרת ראשונה**: מתחילת הקובץ, מסתיימת ב-\x25\x00\xf2 ו-244 בתים NULL
- **כותרת שניה**: מתחיל ב-\xffT - כלומר \xff\x54 ומתרחב ל-4096 בתים, שמכיל שמות עמודות/שדות ודברים אחרים, ונראה שהוא מתחיל במיקום בתים 6144.
- **שדה**: לערך יש כותרת של 10 בתים, בפורמט הבא: {type byte} {type byte, part 2} {data byte 1} \x00 {db 2} \x00 {db 3} {db 3 , חלק 2} {db 4} \x00. נתונים בייט 2 הוא מספר השדה, בייט נתונים 3 הוא מספר הרשומה (הוספת בייט נתונים 3, חלק 2 כאשר הוא עובר מעל 256 רשומות).


## הפניות ##

* [User:JesseW/wdb format](https://en.wikipedia.org/wiki/User:JesseW/wdb_format)

