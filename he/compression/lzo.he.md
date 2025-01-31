{
  "date" : "2021-06-16",
  "keywords" :[ "LZO", "דחוס", "קובץ", "הרחבה", "פורמט קובץ", "למפל-זיו-אוברהום" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ LZO",
  "description":"למד על פורמט קובץ LZO וממשקי API שיכולים ליצור ולפתוח קובצי LZO.",
  "linktitle" : "LZO",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## מהו קובץ LZO? ##

קובץ עם סיומת .lzo משולב עם תכונות אחסון קבצים שיכולות להקטין את כל הקבצים בקובץ הדחוס. כל הקבצים הדחוסים עשויים להכיל קובץ אחד או יותר או אפילו קבוצות של קלסרים עם מספר קבצים מסוגים וממדים שונים. הגודל של קובץ דחוס קטן יותר בהשוואה לגודל המשותף של כל הקבצים והתיקיות המאוחסנים בקובץ דחוס LZO. כל הקבצים הדחוסים של LZO מאוחסנים בפורמט LZO ומופעלים במפורש עם תכונות דחיסה המשמשות את תוכנת הדחיסה והדחיסה של קבצי LZOP. כל מפרטי הדחיסה משולבים בתוכנית דחיסת ופירוק קבצים זו שמקורה בספריית דחיסת הקבצים של Lempel-Ziv-Oberhume. מהירות דחיסה מהירה יותר ויחסי דחיסה מפותחים משולבים גם בקבצי LZO אלה.

## מפרט LZO ##

מרקוס פרנץ קסבר יוהנס אוברהומר פיתח את האלגוריתם המקורי "lzop", המבוסס על אלגוריתמים קודמים של אברהם למפל ויעקב זיו, בשנת 1996. ספרייה זו מיישמת מגוון אלגוריתמים עם המאפיינים הבאים:

* דחיסה מהירה יותר מאשר DEFLATE
* דקומפרסיה מהירה
* מאגרים נוספים הדרושים במהלך הדחיסה (בגודל 8KB או 64KB, תלוי ברמת הדחיסה)
* מאגרי המקור והיעד הם כל הזיכרון הנדרש לפירוק
* מספק שליטה הן על יחס הדחיסה והן על מהירות הדחיסה

בתור אלגוריתם דחיסה של בלוק, LZO מבצע דחיסה חופפת כמו גם ביטול דחיסה במקום. כדי להשיג דחיסה חופפת, גודל הבלוק של הדחיסה והדחיסה חייב להתאים. אלגוריתם הדחיסה של LZO מפצל את נתוני הקלט להתאמות (מילון הזזה) וליטרונים שאינם תואמים, נותן תוצאות טובות עם נתונים מיותרים ביותר ותוצאות מקובלות עם נתונים שאינם ניתנים לדחיסה, רק מגדיל את הנתונים הבלתי ניתנים לדחיסה ב-1/64 מהמקור. גודל.

## בעיות בפתיחת קובץ LZO ##

להלן מספר הבעיות שעלולות לגרום לעבודה לקויה של פורמט קובץ LZO:
  


* ייתכן שהקובץ פגום. כדי לפתור בעיה זו, הורד את הקובץ שוב או בקש מהשולח לשלוח שוב את הקובץ
* הסיבה השנייה היא קובץ נגוע במקרה זה סרוק את הקובץ כראוי
* קישורים לא תקינים לקובץ LZO
* הסרת תיאור ה-LZO
* אין מספיק משאבי חומרה
* דרייברים מיושנים של הציוד
  


## הפניות ##

* [LZO - מאת ויקיפדיה](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Oberhumer)

