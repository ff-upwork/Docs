{
  "date" : "2019-10-11",
  "keywords" :[ "chm", "קובץ chm", "פורמט קובץ chm", "סוג קובץ chm", "קובץ", "סוג", "מהו קובץ chm" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CHM - HTML Help File Format",
  "description" :"למד על מהו קובץ CHM וממשקי API שיכולים ליצור ולפתוח אותם.",
  "linktitle" : "CHM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ CHM?

פורמט הקובץ CHM מייצג את קובץ העזרה של Microsoft **[HTML](/he/web/html/)** המורכב מאוסף של דפי HTML. הוא מספק אינדקס לגישה מהירה לנושאים וניווט לחלקים שונים של מסמך העזרה. ניתן לחפש תוכן בקובץ CHM באמצעות אפשרות החיפוש הניתנת. CHM הוא פורמט קובץ עזרה מקוון קנייני של מיקרוסופט המשמש לעתים קרובות לתיעוד תוכנה. בנוסף, הוא משמש במספר יישומים אחרים כמו מדריכי הדרכה, ספרים אינטראקטיביים ועלונים אלקטרוניים. רוב סביבות הפיתוח המודרניות של Microsoft תומכות בהפקת תיעוד CHM ממידע זמין באפליקציה.

היכולת הייחודית של פורמט קובץ CHM ליישם תוכן עניינים ואינדקס משולב הופכת אותו להבדל על פני דפי HTML סטנדרטיים אחרים. קובץ ה-CHM שנוצר הוא קטן יחסית בגודלו, ולכן ניתן להפיץ אותו בקלות עם חבילות תוכנה. כלי עריכת העזרה, HTML Help Workshop, מספק מערכת קלה לשימוש ליצירה וניהול של פרויקטי עזרה והקבצים הקשורים אליהם. קובצי CHM עשויים לכלול טקסט, תמונות והיפר-קישורים; ניתן לצפייה בדפדפן אינטרנט; בשימוש על ידי Windows ותוכניות אחרות כפתרון עזרה מקוון.

## פורמט קובץ CHM

הצורה הסופית של קובץ CHM שנוצר תלויה באופן שבו מערכת העזרה מעוצבת והאם היא מיועדת לאפליקציה או לאתר אינטרנט. קובץ CHM תומך בדחיסת נתונים עם דחיסת LZX ליצירת קבצי HTML דחוסים. יש לו את מנוע החיפוש המובנה לחיפוש מהיר של תוכן יחד עם היכולת למזג קבצי CHM מרובים. קובץ CHM מורכב מקבוצה של קובצי HTML, תוכן עניינים מקושר וקובץ אינדקס.

### קבצי HTML

בין אם אתה יוצר נושאי עזרה להפצה עם תוכנית, או באינטרנט, המסמכים שאתה כותב נוצרים באמצעות שפת עיצוב מיוחדת המכונה Hypertext Markup Language (HTML). לקובצי HTML יש סיומת שם קובץ .htm או .html.

למרות שכל נושא עזרה או דף אינטרנט שאתה כותב נראה כמסמך עם טקסט, גרפיקה או תמונות מונפשות, קובצי .htm הם למעשה מסמכי טקסט שיש להם קודי עיצוב מיוחדים של HTML. קודים אלה, הנקראים תגים, אומרים לדפדפן כיצד להציג כל עמוד. רק הטקסט המופיע בנושא או בדף אינטרנט נמצא בפועל בקובץ ה-.htm. כל גרפיקה, צלילים, תמונות מונפשות או רכיבים אחרים המופיעים הם קבצים נפרדים שקובץ ה-HTML שלך מצביע עליהם. הדפדפן מעתיק או מוריד את הגרפיקה, הצלילים או אלמנטים אחרים כאשר הוא רואה את התגים שאומרים לו לעשות זאת.

### תוכן העניינים (TOC)
קובץ תוכן העניינים של העזרה (.hhc) הוא קובץ HTML המכיל את כותרות הנושאים של תוכן העניינים שלך. כאשר משתמש פותח את תוכן העניינים בקובץ עזרה מורכב (או בדף אינטרנט) ולוחץ על כותרת נושא, קובץ ה-HTML המשויך לכותרת זו ייפתח.

### קובץ אינדקס
קובץ האינדקס (.hhk) הוא קובץ HTML המכיל את ערכי האינדקס (מילות המפתח) עבור האינדקס שלך. כאשר משתמש פותח את האינדקס בקובץ עזרה מורכב, או בדף אינטרנט, ולוחץ על מילת מפתח, קובץ ה-HTML המשויך למילת המפתח ייפתח.

## רכיבי עזרה של HTML

HTML עזרה מורכבת ממספר רכיבים. אלה כוללים את הדברים הבאים:

* `סדנת עזרה ב-HTML`: כלי עריכת עזרה עם ממשק גרפי קל לשימוש ליצירת קובצי פרויקט, קובצי HTML, קבצי תוכן, קבצי אינדקס, וכל מה שאתה צריך כדי להרכיב מערכת עזרה מקוונת או אתר אינטרנט .
* `HTML Help ActiveX control`: תוכנה קטנה ומודולרית המשמשת להכנסת עזרה ניווט ופונקציונליות של חלונות משניים לתוך קובץ HTML.
* `מציג העזרה של HTML`: חלון בעל שלושה חלוניות פונקציונלי לחלוטין, בו יכולים להופיע נושאי עזרה מקוונים.
* `עורך תמונות עזרה של מיקרוסופט HTML`: כלי גרפי מקוון ליצירת צילומי מסך; ולהמרה, עריכה וצפייה בקבצי תמונה.
* `The HTML Help Java Applet`: תוכנית קטנה מבוססת Java שניתן להשתמש בה במקום פקד ActiveX כדי להכניס עזרה לניווט לתוך קובץ HTML.
* `תוכנת ההפעלה של HTML Help`: התוכנית שמציגה ומפעילה עזרה כאשר אתה לוחץ על קובץ עזרה מהידור.
* `מהדר העזרה של HTML`: תוכנית הקומפילציה של פרויקט, תוכן, אינדקס, נושא וקבצים אחרים לקובץ עזרה מהידור.
* `The HTML Help Authoring Guide`: מדריך מקוון שנועד לסייע למחברים בשימוש ב-HTML Help לעיצוב מערכת עזרה. המדריך מכיל גם הפניה מלאה לעזרה של HTML למפתחים והפניה לתג HTML למחברים.

## הפניות

* [עזרה של Microsoft HTML](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/htmlhelp/microsoft-html-help-1-4-sdk)
* [עזרה של Microsoft Compiled HTML](https://en.wikipedia.org/wiki/Microsoft_Compiled_HTML_Help)

