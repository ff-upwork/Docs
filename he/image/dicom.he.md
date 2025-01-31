{
  "date" : "2019-10-11",
  "keywords" :[ "קובץ dicom", "פורמט קובץ dicom", "מהו קובץ dicom", "קובץ", "דוגמה לדיקום", "סיומת קובץ dicom","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DICOM - פורמט קובץ הדמיה ותקשורת דיגיטלית",
  "description":"למד על פורמט קבצי DICOM וממשקי API שיכולים ליצור ולפתוח קובצי DICOM.",
  "linktitle" : "DICOM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ DICOM?

DICOM הוא ראשי התיבות של Digital Imaging and Communications in Medicine ונוגע לתחום האינפורמטיקה הרפואית. DICOM משמש לשילוב של מכשירי הדמיה רפואיים כמו מדפסות, שרתים, סורקים וכו' של ספקים שונים ומכיל גם נתוני זיהוי של כל מטופל לייחודיות. ניתן לשתף קובצי DICOM בין שני צדדים אם הם מסוגלים לקבל נתוני תמונה בפורמט DICOM. חלק התקשורת של DICOM הוא פרוטוקול שכבת יישומים ומשתמש ב-TCP/IP כדי לתקשר בין ישויות. גרסאות הנתמכות על ידי שירותי אינטרנט הן 1.0, 1.1, 2 ואילך.

## היסטוריה ##

DICOM פותחה במשותף על ידי המכללה האמריקאית לרדיולוגיה (ACR) ואיגוד יצרני החשמל הלאומי (NEMA) לצורך החלפה וצפייה בתמונות רפואיות כמו MRI, סריקות CT ותמונות אולטרסאונד. בתחילה, היה קשה לפענח את התמונות שהמכונות ייצרו. לכן, ACR ו-NEMA יצרו יחד צוות בשנת 1983 אשר הוציא את התקן הראשון שלו, ACR/NEMA 300 בשנת 1985. הגרסה השנייה יצאה בשנת 1988 שהייתה פופולרית יותר בקרב הספקים, אך עד מהרה התברר שגם הגרסה השנייה זקוקה לשיפור. הגרסה השלישית של התקן שוחררה בשנת 1993 בשם "DICOM". 3.0 היא עדיין הגרסה העדכנית ביותר, אך היא עודכנה ברציפות מאז 1993.

## פורמט קובץ DICOM ##

DICOM הוא השילוב של הגדרת פורמט קובץ ופרוטוקול תקשורת רשת. DICOM משתמש בסיומת .DCM. .DCM קיים בשני פורמטים שונים, כלומר פורמט 1.x ופורמט 2.x. DCM Format 1.x זמין עוד בשתי גרסאות רגילות ומורחבות. פרוטוקולי HTTP ו-HTTPS משמשים עבור שירותי האינטרנט של DICOM.

### כותרת הקובץ ###

כותרת הקובץ מכילה 128 בתים הקדמת קובץ וקידומת DICOM של 4 בתים.

**הקדמה מס' 128 בתים**|**קידומת מס' 4 בתים "D, I, C, M**

**הקדמה** משמשת לגישה לתמונות ולנתונים אחרים בקובץ DICOM המספק תאימות לפורמטים נפוצים של קבצי תמונה.

**קידומת** מכילה את המחרוזת "DICM" כתווים רישיות.

### מערך נתונים ###

כל קובץ חייב להכיל מערך נתונים יחיד המייצג מופע SOP ו-SOP Class עם IOD קשור. מערך נתונים הוא ייצוג של מידע מהעולם האמיתי. ערכת נתונים מכילה רכיבי נתונים ורכיבי נתונים מכילים ערכים של התכונות של אותו אובייקט. מבנה התכונות מצוין ב-IOD. אובייקט נתוני DICOM מורכב ממספר תכונות, כולל פריטים כגון שם, מזהה וכו', וגם תכונה מיוחדת אחת המכילה את נתוני פיקסל התמונה.

### רכיבי נתונים ###

רכיב הנתונים מורכב תג של רכיב נתונים, אורך ערך וערך עבור רכיב הנתונים. ישנם 5 סוגים של רכיבי נתונים, כלומר רכיבי נתונים נדרשים מסוג 1, רכיבי נתונים מותנים מסוג 1C, רכיבי נתונים נדרשים מסוג 2, רכיבי נתונים מותנים מסוג 2C ורכיבי נתונים אופציונליים מסוג 3. בסיסי שלושה סוגים של מבני רכיבי נתונים הם כדלקמן.

**רכיב נתונים עם VR מפורש**

|מספר קבוצה|מספר אלמנט|ייצוג ערך|שמור|אורך ערך|שדה ערך
---|---|---|---|---|---|
|2 Bytes|2 Bytes|2 Bytes|2 Bytes # 0x00, 0x00|4 Bytes|"Value Length Bytes"

**רכיב נתונים עם VR מפורש**

|מספר קבוצה|מספר אלמנט|ייצוג ערך|אורך ערך|שדה ערך
---|---|---|---|---|
|2 Bytes|2 Bytes|2 Bytes|2 Bytes|"Value Length Bytes"

**רכיב נתונים עם VR מרומז**


|מספר קבוצה|מספר אלמנט|אורך ערך|שדה ערך
---|---|---|---|
|2 Bytes|2 Bytes|4 Bytes|"Value Length Bytes"

1. **תג אלמנט נתונים**: מספר שלם מסודר המייצג את מספר הקבוצה ומספר האלמנט
1. **ייצוג ערך VR**: VR הוא מחרוזת תווים המייצגת את ה-VR של אלמנט הנתונים.
1. **אורך ערך**: האם המספר השלם ללא סימן מייצג את האורך המפורש של שדה הערך.
1. **שדה ערך**: מתאר את הערכים של רכיבי הנתונים.

## תחביר העברה ##

תחביר העברה הוא קבוצה של כללים לקידוד כדי לייצג באופן חד משמעי תחבירים מופשטים יותר. בעזרת תחביר העברה ישויות מתקשרות לנהל משא ומתן על טכניקות קידוד נפוצות שבהן הם תומכים.

## SOPs ##

האיחוד של IOD ו-DIMSE מגדיר מחלקת SOP. הגדרת SOP Class מכילה את הכללים והסמנטיקה שעשויים להגביל את השימוש בשירותים בקבוצת השירות של DIMSE או בתכונות של IOD. דוגמאות לרכיבי שירות הם Store, Get, Find, Move וכו'. דוגמאות לאובייקטים הן תמונות CT, תמונות MR, אך כוללות גם רשימות לוח זמנים, תורי הדפסה וכו'.

## שירותים ##

DICOM מספקת שירותים שונים, בעיקר הקשורים לתקשורת נתונים. כל אחד מהם מתואר בקצרה להלן:


**חנות:** שירות DICOM Store שולח תמונות או אובייקטים אחרים למערכת ארכיון ותקשורת של תמונות (PACS) או לשרת.


**התחייבות לאחסון:** שירות התחייבות לאחסון משמש לאישור שתמונה נשמרה באופן קבוע במכשיר בכל סוג של מדיה.


**שאילתה/שליפה:** שירות זה מאפשר לתחנת עבודה למצוא את רשימות התמונות או אובייקטים אחרים ולאחר מכן לאחזר אותם מ-PACS.


**רשימת עבודה של מודאליות:** שירות רשימת מודאליות מספקת רשימה של הליכי הדמיה שתוזמנו לביצועים על ידי מכשיר רכישת תמונה.


**הדפסה:** שירות זה שולח תמונות למדפסת.

## מספרי יציאה מעל IP ##

DICOM משתמש ביציאות TCP ו-UDP הבאות:

1. 104
1. 2761
1. 2762
1. 11112

## הפניות ##

* [https://en.wikipedia.org/wiki/DICOM](https://en.wikipedia.org/wiki/DICOM)
* [https://www.leadtools.com/sdk/medical/dicom-spec](https://www.leadtools.com/sdk/medical/dicom-spec)
* [https://www.dicomstandard.org/concepts/](https://www.dicomstandard.org/concepts/)
* [https://www.dicomlibrary.com/dicom/](https://www.dicomlibrary.com/dicom/)

