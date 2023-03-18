{
  "date" : "2021-08-04",
  "keywords" :[ "מוד", "mp3", "קובץ", "הרחבה", "פורמט", "מהו פורמט קובץ mod", "מוזיקה", "פורמט קובץ mod", "מוד לעומת MP3", "מפרט פורמט קובץ mod "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"למד על פורמט קובץ MOD וממשקי API שיכולים ליצור, להמיר ולפתוח קובצי MOD.",
  "title" :"MOD - קובץ מודול מוזיקה",
  "linktitle" : "MOD",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-04"
}

## מהו קובץ MOD?
קובץ עם סיומת .mod הוא קובץ מודול מוזיקה שנוצר באמצעות פורמט מודול המוזיקה הסטנדרטי, המבוסס על **פורמט מודול Amiga** שפותח על ידי Karsten Obarski והופץ עם תוכנת **Ultimate Soundtracker** עבור ה-Commodore מערכת אמיגה. בדומה לקובץ [MIDI](/he/audio/mid/), הוא מורכב מתבניות תווים ודגימות צליל, המייצגים כלים שונים המושמעים בהתאם לתווים. קבצי MOD משמשים במיוחד במשחקי וידאו כמוזיקת רקע ובתת-תרבות אמנות המחשב **דמוסצנה**.

## פורמט קובץ MOD

ה-MOD הוא פורמט קובץ מחשב המשמש את תפקידו הבסיסי הוא לייצג מוזיקה, וזה היה פורמט קובץ המודול הראשון. קבצי MOD משתמשים בסיומת הקובץ .mod, למעט ב-**Amiga** שקוראת כותרת של קובץ כדי לקבוע את סוג הקובץ, כך שהיא לא מסתמכת על סיומות שמות קובץ. קובץ MOD מורכב מסט של כלים שונים בצורה של דגימות, מספר תבניות המפרטות כיצד ומתי יש לנגן את הדגימות, ורשימה של אילו תבניות לנגן באיזה סדר.

### מפרטי פורמט קובץ MOD

תבנית קובץ MOD מעוצבת למעשה בממשק משתמש של סיקוונסר כטבלה עם עמודה אחת לכל ערוץ, כך לטבלה זו יש ארבע עמודות (אחת לכל ערוץ חומרה של Amiga. בכל עמודה יש 64 שורות).

תא בטבלה יכול לגרום לאחת מהפעולות הבאות להתרחש בערוץ העמודה שלו כשמגיעים לזמן השורה שלו:

- התחל כלי המנגן תו חדש בערוץ זה בווליום נתון, אולי עם אפקט מיוחד שהופעל עליו
- שנה את עוצמת הקול או האפקט המיוחד המוחל על ההערה הנוכחית
- שינוי זרימת דפוס; קפוץ למיקום ספציפי של שיר או תבנית או לולאה בתוך תבנית
- לעשות כלום; כל תו קיים שמתנגן בערוץ זה ימשיך להתנגן

מכשיר הוא דגימה בודדת יחד עם מפרט אופציונלי של איזה חלק מהדגימה ניתן לחזור כדי להחזיק תו מוצק.

### תזמון
מסגרת הזמן המינימלית הייתה 0.02 שניות בקובץ ה-MOD המקורי, או מרווח "הריקה אנכית" (VSync), מכיוון שהתוכנה המקורית השתמשה בתזמון VSync של הצג הפועל ב-50 הרץ (עבור PAL) או 60 הרץ (עבור NTSC) לתזמון.

## הפניות

* [MOD (פורמט קובץ) - מאת ויקיפדיה](https://en.wikipedia.org/wiki/MOD_(file_format))
