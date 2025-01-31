{
  "date" : "2021-28-05",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAR - Microsoft Access Reports File",
  "keywords" :[ "mar", "mar file", "mar file format", "what is access report", "access report", "microsoft access report"],
  "description":"למד על פורמט קובץ Acess Report (MAR) המשמש את תוכנת Microsoft Access ליצירת קיצור דרך או קישור ל-Microsoft Access Report.",
  "linktitle" : "MAR",
  "menu" : {
    "docs" : {
    "identifier": "reporting-mar",
      "parent" : "reporting"
}
},
  "lastmod" : "2021-28-05"
}

## מהו Access Report (קובץ MAR)? ##
קובץ שנוצר על ידי Microsoft Access כקיצור דרך לדוח שלו נשמר עם סיומת הקובץ .mar. **דוח Microsoft Access** מציע דרך לעצב, להציג ולסכם את המידע במסד הנתונים של Microsoft Access. דוחות אלו מאפשרים לך לעצב את הנתונים שלך בפריסה מדויקת ואינפורמטיבית לצפייה על מסך או הדפסה. הדוח רק מציג את הנתונים הסטטיים, מה שאומר שלא נוכל לשנות את הנתונים בטבלאות בעת צפייה בדוח Access. הדוח מציג את הנתונים העדכניים ביותר כאשר הוא נפתח.

## פורמט קובץ Microsoft Access Report (MAR).

פורמט הקובץ MAR משמש את תוכנת Microsoft Access ליצירת קיצור דרך או קישור ל-Microsoft Access Report שהוא אובייקט מסד נתונים שהופך שימושי כאשר אתה צריך להציג את המידע במסד הנתונים שלך עבור כל אחד מהשימושים הבאים:

- הצג סיכום נתונים.
- ארכיון תמונות מצב של הנתונים.
- הצג פרטים על רשומות בודדות.
- צור תוויות.

## חלקים מדוח גישה
העיצוב של דוח Access מחולק למקטעים שונים שניתן לצפות בהם בתצוגת העיצוב. הטבלה הבאה מסבירה כיצד כל חלק עובד ויכולה לעזור לך ליצור דוחות.
| מדור | כיצד מוצג הקטע בעת הדפסה | היכן ניתן להשתמש בקטע |
---------|----|------|
| כותרת דוח | בתחילת הדו"ח. | השתמש בכותרת הדוח למידע שעלול להופיע בדרך כלל בדף שער, כגון לוגו, כותרת או תאריך. כאשר אתה מציב פקד מחושב המשתמש בפונקציה Sum aggregate בכותרת הדוח, הסכום המחושב הוא עבור הדוח כולו. כותרת הדוח מודפסת לפני כותרת העמוד. |
| כותרת עמוד | בראש כל עמוד. | השתמש בכותרת דף כדי לחזור על כותרת הדוח בכל עמוד. |
| כותרת קבוצה | בתחילת כל קבוצת שיאים חדשה. | השתמש בכותרת הקבוצה כדי להדפיס את שם הקבוצה. לדוגמה, בדוח המקובץ לפי מוצר, השתמש בכותרת הקבוצה כדי להדפיס את שם המוצר. כאשר אתה מציב פקד מחושב המשתמש בפונקציה Sum aggregate בכותרת הקבוצה, הסכום הוא עבור הקבוצה הנוכחית. אתה יכול לכלול מספר מקטעי כותרות קבוצתיות בדוח, בהתאם למספר רמות הקיבוץ שהוספת. למידע נוסף על יצירת כותרות עליונות ותחתונות של קבוצה, עיין בסעיף הוספת קיבוץ, מיון או סיכומים. |
| פירוט | מופיע פעם אחת עבור כל שורה במקור הרשומה. | זה המקום שבו אתה מציב את הפקדים המרכיבים את הגוף הראשי של הדוח. |
| כותרת תחתונה של קבוצה | בסוף כל קבוצת רשומות. | השתמש בכותרת תחתונה של קבוצה כדי להדפיס מידע סיכום עבור קבוצה. תוכל לכלול מספר קטעי כותרת תחתונה קבוצתית בדוח, בהתאם למספר רמות הקיבוץ שהוספת. |
| כותרת תחתונה של עמוד | בסוף כל עמוד. | השתמש בכותרת תחתונה של עמודים כדי להדפיס מספרי עמודים או מידע לכל עמוד. |
| כותרת תחתונה לדיווח | בסוף הדו"ח. הערה: בתצוגת עיצוב, כותרת התחתונה של הדוח מופיעה מתחת לכותרת התחתונה של העמוד. עם זאת, בכל שאר התצוגות (תצוגת פריסה, למשל, או כאשר הדוח מודפס או מוצג בתצוגה מקדימה), כותרת התחתונה של הדוח מופיעה מעל לכותרת התחתונה של העמוד, מיד אחרי הכותרת התחתונה של הקבוצה או שורת הפרטים האחרונה בעמוד האחרון. | השתמש בכותרת התחתונה של הדוח כדי להדפיס סיכומי דוחות או מידע סיכום אחר עבור הדוח כולו. |






## הפניות ##

- [מבוא לדוחות ב-Access](https://support.microsoft.com/en-us/office/introduction-to-reports-in-access-e0869f59-7536-4d19-8e05-7158dcd3681c)
- [עיצוב דוחות ב-Access](https://github.com/prijuly2000/DBMS/blob/master/DesigningReportsinAccess2010.pdf)

