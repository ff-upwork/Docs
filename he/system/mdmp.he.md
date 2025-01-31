{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"קובץ MDMP - פורמט קובץ מיניdump של Windows",
  "description":"למד על פורמט קובץ MDMP וממשקי API שיכולים ליצור ולפתוח קובצי MDMP.",
  "linktitle" : "MDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## מהו קובץ MDMP?

קובץ MDMP הוא קובץ זיכרון של יישום ב-Microsoft Windows שנוצר כאשר היישום נסגר בצורה חריגה או קורס. הוא מכיל מידע ונתונים שניתן להשתמש בהם כדי לנפות באגים בגורם להתרסקות. קבצי MDMP ישימים על יישומים שנוצרו על ידי כל פלטפורמה כגון Java, C++, .NET ואחרות. בנוסף ל-MDMP,

יישומים שיכולים לפתוח קבצי MDMP כוללים את Microsoft Visual Studio Debugger.

## פורמט קובץ MDMP

קבצי MDMP נשמרים כקבצים בינאריים בדיסק וניתן לפתוח אותם עם מאתר הבאגים של Microsoft Visual Studio. הוא מכיל את המידע הבא כדי לסייע בזיהוי הסיבה להתרסקות.

* פרטים על הודעת עצור, הפרמטרים שלה ונתונים נוספים
* רשימת מנהלי התקנים טעונים
* הקשר מעבד (PRCB) עבור המעבד שהפסיק לעבוד
* עיבוד מידע והקשר ליבה (EPROCESS) עבור התהליך שנפסק
* עיבוד מידע והקשר ליבה (ETHREAD) עבור השרשור שהופסק
* מחסנית קריאות במצב ליבה עבור השרשור שהפסיק

מידע זה עוזר לברר מה קרה, לתקן את הבעיה ולמנוע את הישנותה.

### ניתוח Minidump

Windows דורש קובץ החלפה באמצעי האחסון האתחול כדי ליצור קובץ dump של זיכרון. קובץ ההחלפה נוצר באמצעי האתחול וגודלו צריך להיות לפחות 2 מגה-בייט (MB). קובץ ה-dump נוצר כאשר יישום קורס. במקרה של בעיה שנייה, נוצר קובץ dump זיכרון קטן שני בעוד שהקודם נשמר. השם של קובץ ה-dump שונה כדי למנוע החלפה.

Windows שומרת רשימה של כל קבצי dump הזיכרון בתיקיית %SystemRoot%\Minidump. אתה יכול לנתח קבצי MDMP על ידי הפעלתם ב-Visual Studio Debugger כפי שמופיע בשלבים שלהלן.

## כיצד אוכל לפתוח קובץ MDMP ב-Visual Studio?

ניתן להשתמש בשלבים הבאים כדי לפתוח קובץ MDMP ב-Visual Studio.

* ב-Visual Studio, מתפריט קובץ, בחר פתח | Crash Dump .
* נווט לקובץ ה-dump שברצונך לפתוח.
* בחר פתח.

## התייחסות

* [כיצד לקרוא את קובץ dump הזיכרון הקטן שנוצר על ידי Windows אם מתרחשת קריסה](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

