{
  "date" : "2021-04-16",
  "keywords" :[ "XML", "P6XML", "קובץ", "הרחבה", "פורמט קובץ", "פרויקט", "ניהול", "Primavera", "P6"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P6XML - Primavera P6 Project",
  "description":"למד על פורמט קובץ P6XML וממשקי API שיכולים ליצור ולפתוח קובצי P6XML.",
  "linktitle" : "P6XML",
  "menu" : {
    "docs" : {
      "parent" : "project-management"
}
},
  "lastmod" : "2021-05-07"
}

## מהו קובץ P6XML? ##

לסיומת הקובץ P6XML יש קריאה מצוינת, יכולת הסתגלות ושימוש רחב שהופכים אותה לפורמט האידיאלי. ל- Primavera P6 Professional יש את הפונקציונליות לייצא ולייבא גם קבצי [XER](/he/project-management/xer/) וגם קובצי XML. XML מייצג **Extensible Markup Language**. פורמט כללי זה מאפשר למשתמשים לשתף מידע על פרויקט בין מסדי נתונים של Primavera P6. ניתן לאחסן בקלות את נתוני הפרויקט בקובץ טקסט באמצעות קובץ ה-XML; זה הופך את הדברים לפשוטים יותר עבור תוכנות רבות להחליף את הנתונים. ניתן לשתף ולנהל נתונים כאלה בקלות על ידי משתמש Primavera P6.

## היתרונות של פורמט קובץ P6XML ##

* למשתמשי Primavera קל להגדיר אילו קווי בסיס ייצאו ויובאו באמצעות קובץ ה-XML
* ייצוא XML יכול להכיל את כל תוכניות הפעולה המפורטות של הפרויקט
* כל משתמש המשתמש ב-Primavera 6 שאינו יכול לערוך, להוסיף או למחוק פריטי נתונים גלובליים מסוימים, כמו קודי פעילות, יומנים ומשאבים, לא יוכל לייבא אותם
* בנוסף להגדרות General and Project Security Profile המשמשות את Primavera, פריטי נתונים שישפיעו או ישנו את הנתונים במסד הנתונים לא ייובאו

## ייצוא קובץ ה-XML מ-Primavera P6 ##

לייצוא פרויקטים של P6 Professional ונתוני פרויקטים לקובץ P6XML, השתמש ב-Oracle Primavera Cloud. אתה יכול להוריד את הקובץ כאשר הוא נוצר מאפליקציית שולחן העבודה P6 Professional ולייבא אותו אל Primavera Cloud. לפני שתפעיל ללא הפרעה את תהליך הייצוא, עליך לקבוע אם אתה מקושר למסד נתונים של P6 Professional או ל-P6 EPPM. חלק מהתכונות של תהליך הייצוא עשויות להיות שונות בהתאם למסד הנתונים שלך. לאחר הגדרות P6 Specialized עם מסד נתונים P6 Proficient, תהליך הייצוא פועל באופן מקומי במערכת שלך. עם מסד נתונים P6 Professional, אתה יכול לייצא ולפתוח בקלות את קובץ ה-XML של P6 מהגדרה במערכת שלך.

להלן כמה שלבים המתארים את תהליך הייצוא:

* פרויקט פתוח רצונות Primavera P6
* לאחר מכן, בחר ייצוא בלשונית קובץ
* בחר "Primavera P6 – (XML)". לאחר מכן, לחץ על הבא
* לחץ פעמיים על הפרויקט שתייצא
* בחר את החתכים עבור הנתיב שבו אתה רוצה לשים את הקובץ המיוצא ובחר "סיום".
* בחר את האפשרות איך אתה רוצה לשמור את הקובץ
* אם אין צורך בפריסות ברמת הפרויקט עם קובץ הייצוא, חיוני לנקות את הבחירה ל"ייצא את כל הפריסות ברמת הפרויקט".
* בחר סיום ואז תקבל אישור על ייצוא ה-XML

### טיפים חשובים ###

* בכל פעם שמתחברים למסד נתונים של P6 EPPM, על המנהל להעביר את כתובת ה-URL של מקור התוכן לשדה P6 URL בדף הכללי של הגדרות יישומים ב-P6
* זה נוח לייצא פרויקטים רבים לקובץ XML אחד
* נתונים גלובליים המוקצים לפרויקט מיוצאים
* זה נוח לייצא קבצי XML מבלי לקבל כניסה לכל המשאבים



## בעיות בפתיחת קובץ P6XML? ##

כמה בעיות נפוצות שעלולות להתעורר ולגרום לתפקוד שגוי של פורמט P6XML הן כדלקמן:

* היעדר תוכנה תומכת
* קובץ פגום
* קובץ נגוע עקב וירוס
* תיאור P6XML נמחק בטעות מהרישום של Windows
* אין זכות גישה במערכת לפתיחת הקבצים
* כונן מיושן במערכת שלך
* שם ההרחבה של הקובץ שונה


## הפניות ##

* [Oracle - P6 XML](https://docs.oracle.com/cd/E80480_01/English/admin/p6_import_guide/index.html)