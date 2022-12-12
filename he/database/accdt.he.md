{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDT", "הרחבה", "קובץ", "פורמט קובץ", "סוג קובץ מסד נתונים", "פורמט קובץ מסד נתונים", "קבצי מסד נתונים" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"למד על פורמט קובץ ACCDT וממשקי API שיכולים ליצור ולפתוח קבצי ACCDT.",
  "title" :"ACCDT - Microsoft Access 2007 Template Database Format",
  "linktitle" : "ACCDT",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## מהו קובץ ACCDT?

קובץ עם סיומת .accdt הוא קובץ תבנית מסד נתונים של Microsoft Access המכיל רכיבי מסד נתונים מוגדרים מראש. אלמנטים אלה הם אוסף של מבנים המגדירים יישומי מסד נתונים כגון סכימות מסד נתונים לאחסון נתונים, תיאור פריסה לתצוגות של הנתונים ומטא נתונים המתארים את מסד הנתונים. בהיותם קבצי תבנית, ניתן להשתמש בקבצי ACCDT ליצירת מסדי נתונים על סמך הגדרות התבנית הזמינות בהן. קבצי מסד נתונים שהתקבלו נשמרים כקבצי [ACCDB](/he/database/accdb/) ומאוכלסים בנתונים בטבלאות. Microsoft Access 2007 ואילך יכול לפתוח קבצי ACCDT.

## פורמט קובץ ACCDT

קובצי תבניות ACCDT מבוססים על מפרטי Office Open XML וכל הנתונים כלולים בחבילת ZIP. מידע על המבנה והתוכן של מסד הנתונים כלול בקבצי [XML](/he/web/xml/) ובקבצי הטקסט ומקושרים זה לזה באמצעות מערכות יחסים. אתה יכול לשנות את השם של קובץ ACCDT לסיומת [.zip](/he/compression/zip/) ולהשתמש בכל תוכנת דחיסה כדי לחלץ את התוכן של ארכיון ה-ZIP.

### מבנה הקובץ

קבצי ACCDT הם חבילות המכילות אוסף של חלקים קשורים. כל **חלק** מאחסן מידע על התוכן של יישום מסד נתונים באמצעות XML, טקסט ופורמטים בינאריים, הכולל:

* אובייקטים של מסד נתונים
* מטא נתונים נלווים
* מבנה החבילה

#### חבילה

חבילה היא ארכיון [ZIP](/he/compression/zip/) המכיל חלקים מרובים ותואם את אמנות האריזה הפתוחות המפורטות ב-[ISO/IEC-29500-2](https://go.microsoft.com/fwlink/ ?LinkId=150883). קבצי ACCDT חייבים להכיל לפחות חלק אחד של Template metadaa שאמור להיות היעד של מערכת יחסים. מטא נתונים של תבנית זה הם החלק ההתחלתי של קובץ ACCDT.

#### חלק

חלק הוא זרם של בתים שיש לו סוג משויך לציון אופי וסוג התוכן המאוחסן בו. ספירת חלקים מציינת חלקים חוקיים, סוגי תוכן חוקיים וקשרים נדרשים בין כל החלקים בחבילה.

#### מערכת יחסים

`Package Relationship` - כאשר המטרה היא חלק והמקור הוא החבילה כולה.

`Part-to-Part Relationship` - כאשר המטרה היא חלק והמקור הוא חלק בחבילה.

`קשר מפורש` - כאשר משאב מופנה מהתוכן של חלק מקור על ידי הפניה לרכיב קשר לפי הערך של תכונת ה-ID שלו.

`קשר מרומז` - קשר שאינו מפורש.

`קשר פנימי` - כאשר המטרה היא חלק בחבילה.

`קשר חיצוני` - כאשר היעד הוא משאב חיצוני שאינו בחבילה.

## הפניות ##

* [פורמט קובץ תבנית גישה](https://docs.microsoft.com/en-us/openspecs/sharepoint_protocols/ms-accdt/0a4a68d7-7a85-4a27-ad74-730db57862d7)
