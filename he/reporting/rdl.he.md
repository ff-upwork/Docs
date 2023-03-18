{
  "date" : "2021-03-01",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDL - קובץ שפה של הגדרת דוח",
  "keywords" :[ "rdl", "שפת הגדרת דוח", "XmlTextWriter", "XSD", "רכיב RDL"],
  "description":"למד על פורמט קובץ RDL שהוא ייצוג XML של הגדרת דוח SQL Server Reporting Services.",
  "linktitle" : "RDL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-01"
}

## מהו קובץ RDL? ##

ה-RDL (שפת הגדרת דוחות) היא רף שנקבע על ידי מיקרוסופט להגדרת דוחות. קובץ RDL מורכב מרכיב RDL אחד או רבים. ואילו אלמנט RDL מורכב מסוג הנתונים והקרדינליות שלו. אלמנט יכול להיות פשוט או מורכב. לאלמנט הפשוט אין אלמנט או תכונות צאצא, ואילו לרכיב מורכב יש ילדים ותכונות אופציונליות.

## הגדרת סכימת RDL XML
קובץ XML Schema Definition (XSD) מאמת את קובץ ה-RDL. הסכימה מגדירה את הכללים היכן יכולים להופיע רכיבי RDL בקובץ .rdl. אלמנט RDL יכול להיות פשוט או מורכב. לאלמנט פשוט אין אלמנטים או תכונות צאצאים ולרכיב מורכב יש ילדים ובאופן אופציונלי, תכונות.

## יצירת RDL
מכיוון ש-RDL פתוח וניתן להרחבה באופיו, ניתן לבנות רבים מיישומים וכלים המייצרים קבצי RDL על סמך סכימת ה-XML שלו. אחת הדרכים הפשוטות ביותר ליצור RDL מאפליקציה היא להשתמש במחלקות Microsoft .NET Framework של מרחב השמות **System.Xml** ומרחב השמות System.Linq. במיוחד, ניתן להשתמש במחלקה **XmlTextWriter** לכתיבת RDL. ניתן ליצור הגדרת דוח מלאה מתחילתו ועד סופו בכל יישום .NET Framework באמצעות **XmlTextWriter**. מפתחים יכולים גם להוסיף פריטי דוח מותאמים אישית עם מאפיינים מותאמים אישית כדי להרחיב את ה-RDL.

## סוגי RDL
הטבלה הבאה מפרטת את הסוגים והתכונות המשמשים ברכיבי RDL.

|סוג|תיאור|
---|---|
|בינארי | מאפיין עם ערך בינארי מקודד בסיס-64.|
|בוליאנית| מאפיין עם true או false כערך האובייקט. אלא אם צוין אחרת, הערך של אובייקט בוליאני אופציונלי שהושמט הוא False.|
|תאריך |מאפיין עם תאריך או ערך תאריך-שעה שצוין במלואו בפורמט התאריך ISO8601: YYYY-MM-DD[THH:MM[:SS[.S]]].|
|Enum |מאפיין עם ערך טקסט מחרוזת שחייב להיות אחד מתוך רשימה של ערכים ייעודיים.|
|צף |נכס בעל ערך צף. נקודה (.) משמשת כמפריד עשרוני אופציונלי.|
|Integer |מאפיין בעל ערך שלם (int32).|
|שפה | מאפיין עם ערך טקסט המכיל קוד שפה ותרבות, כגון "en-us" לאנגלית אמריקאית. הערך חייב להיות שפה ספציפית או שפה ניטרלית שעבורה מוגדרת שפת ברירת מחדל ב-Microsoft .NET Framework.|
|שם | מאפיין עם ערך טקסט מחרוזת. השמות חייבים להיות ייחודיים במרחב השמות של הפריט. אם לא צוין, מרחב השמות של פריט הוא האובייקט המכיל הפנימי ביותר שיש לו שם.|
|NormalizedString |מאפיין עם ערך טקסט מחרוזת שעבר מנורמל.|
|גודל |רכיב גודל חייב להכיל מספר (עם תו נקודה המשמש כמפריד עשרוני אופציונלי). אחרי המספר יש לציין מציין עבור יחידת אורך CSS כגון cm, mm, in, pt או pc. רווח בין המספר למציין הוא אופציונלי. למידע נוסף על מגדירי גודל, ראה CSS Values and Units Reference.ב-RDL, הערך המקסימלי עבור Size הוא 160 אינץ'. הגודל המינימלי הוא 0 אינץ'|
|String |מאפיין עם ערך טקסט מחרוזת.|
|UnsignedInt |מאפיין עם ערך שלם לא חתום (uint32).|
| משתנה | מאפיין עם כל סוג XML פשוט.|

## סוגי נתונים RDL
ב-RDL, DataType Enumeration מגדיר את סוג הנתונים של תכונה, ביטוי או פרמטר. הטבלה הבאה מראה כיצד סוגי נתוני CLR תואמים לסוגי נתונים RDL.

|סוג(ים) CLR |סוג נתונים תואם|
---|---|
|בוליאנית| בוליאנית|
|DateTime, DateTimeOffset |DateTime|
|Int16, Int32, UInt16, Byte, SByte |מספר שלם|
|סינגל, זוגי |צף|
|מחרוזת, Char, GUID, טווח זמן |מחרוזת|


## הפניות ##

- [שפת הגדרת דוח (ויקיפדיה)](https://en.wikipedia.org/wiki/Report_Definition_Language)
- [שפת הגדרת דוח (SSRS)](https://docs.microsoft.com/en-us/sql/reporting-services/reports/report-definition-language-ssrs)
