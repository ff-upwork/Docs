{
  "date" : "2022-07-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"הרחבת קובץ INC - מה זה קובץ INC?",
  "description":"למד על INC Include פורמט קבצים וממשקי API שיכולים ליצור ולפתוח קובצי INC.",
  "linktitle" : "INC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-07-14"
}

## מהו קובץ INC?

קובץ INC הוא קובץ כולל המשמש את קוד המקור של התוכנה כדי להתייחס למידע על כותרות. הוא דומה לפורמט הקובץ [.h](/he/programming/h/) ומכיל הצהרות, פונקציות, כותרות או פקודות מאקרו שניתן לעשות בהן שימוש חוזר על ידי קובצי קוד מקור כגון C++. קבצי INC נמצאים בשימוש במגוון שפות תכנות כמו C, [C++](/he/programming/cpp/), Pascal, [PHP](/he/programming/php/) ו-[Java](/he/programming/java/). ניתן להשתמש בעורכי טקסט כגון Microsoft Notepad, Notepad++ ו- TextEdit לפתיחת קובצי INC.

## פורמט קובץ INC - מידע נוסף

קובץ INC נשמר כקובץ טקסט רגיל עם כל ההצהרות כלולות לפי תחביר ההכרזה. קובץ INC אחד יכול להפנות גם לקבצי INC אחרים. לאחר יצירתו, קובץ INC הופך לחלק מהפרויקט וניתן להפנות אליו מקובצי מקור כגון C++. ניתן להפנות אליו על ידי מספר קובצי מקור כדי למנוע כל כפילות.

## תוכן הקובץ של INC

קבצי INC יכולים לכלול את המידע הבא.

**`משתנים`** - במקרה של תכנות מונחה עצמים (OOP), קובץ כותרת מחלקה מכיל הגדרות של כל משתני רמת המחלקה הנגישים בכל קובצי קוד המקור של היישום

**`הצהרת שיטות`** - כל הצהרות השיטות נכללות בקבצי ה-.h header כדי להיות נגישים על פני מספר קובצי יישום.

**`הגדרות פונקציות שאינן מוטבעות`** - קובצי כותרת יכולים להכיל גם הגדרות של מתודות שאינן מוטבעות.

## חסרון בשימוש בקובץ INC ב-PHP

PHP הם סקריפטים בצד השרת הפועלים בשרת ומחזירים את התוצאות לדפי האינטרנט המתקשרים. אם קובץ PHP מפנה לקובץ INC והשרת אינו מוגדר לנתח קבצי .inc (וזה נפוץ מאוד), משתמש יכול להציג את קוד המקור של php בקובץ .inc על ידי ביקור בספריית ה-URL. לכן, יש להיזהר בעת שימוש בקבצי INC כקבצי כוללים ב-PHP.

## הפניות

* [שימוש ב-INC ב-PHP](https://stackoverflow.com/questions/7129842/what-is-an-inc-and-why-use-it)
