{
  "date" : "2021-04-08",
  "keywords" :[ "קובץ dar", "פורמט קובץ dar", "מהו קובץ dar", "קובץ", "דוגמה ל-dar", "סיומת קובץ dar","סיומת", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DAR - פורמט קובץ ארכיון דיסק",
  "description":"למד על פורמט קובץ DAR וממשקי API שיכולים ליצור ולפתוח קובצי DAR.",
  "linktitle" : "DAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## מהו קובץ DAR?

קובץ עם סיומת .dar הוא ארכיון דחוס שנוצר באמצעות ארכיון DAR Disk. זה יכול ליצור גיבוי/ארכיון לדיסק מלא או לקבוצת קבצים. הוא נוצר כדי להחליף את פורמט הקובץ [TAR](/he/compression/tar/) במערכת ההפעלה UNIX וניתן ליצור אותו כקובצי ארכיון מפוצלים עבור מספר רב של קבצים. ארכיון DAR תומך באפשרות של מחיקת קבצים מהמערכת המקושרים לקבצים הראשיים בארכיון. היכולות שלו לספק גיבוי דיפרנציאלי, אינקרמנטלי ודקרמנטלי הופכות אותו לטוב יותר מקבצי TAR.

## פורמט קובץ DAR

קבצי DAR הם ארכיונים דחוסים שיכולים להשתמש בכל דחיסה לכל קובץ כגון [gzip](/he/compression/gz/), [bzip2](/he/compression/bz2/), lzo, xz או lzma. פורמט הקובץ המדויק של קובץ DAR תלוי באיזה סוג עיצוב משמש לדחיסת תוכן הארכיון. זה גם מאפשר הצפנת Blowfish, Twofish, AES, Serpent, Camellia והצפנת מפתח ציבורי וחתימה (OpenPGP).

### תכונות DAR

חלק מהתכונות של פורמט קובץ DAR הן כדלקמן.

* דואג לכל סוג של אינוד (ספרייה, קבצים רגילים, סימלינקים, מכשירים מיוחדים, צינורות עם שם, שקעים, דלתות, ...)
* דואג לאינודים מקושרים קשיחים (קבצים רגילים עם קישורים קשיחים, התקני char, התקני בלוק, סימלינקים עם קישורים קשיחים)
* דואג לקבצים דלילים
* דואג לתכונות מורחבות של קבצי לינוקס,
* דואג לקובץ ACL של לינוקס
* דואג למזלגות קבצים של Mac OS X
* דואג לכמה תכונות ספציפיות למערכת קבצים כמו תאריך לידה של מערכת הקבצים HFS+ ותכונות בלתי ניתנות לשינוי, רישום נתונים, מחיקה מאובטחת, ללא מיזוג זנב, בלתי ניתנים למחיקה, noatime של מערכת הקבצים ext2/3/4.
* דחיסה לכל קובץ עם gzip, bzip2, lzo, xz או lzma (בניגוד לדחיסת כל הארכיון). אדם יכול לבחור שלא לדחוס קבצים שכבר דחוסים על סמך סיומת שם הקובץ שלו.
* חילוץ מהיר של קבצים מכל מקום בארכיון
* רישום מהיר של תוכן הארכיון באמצעות שמירת קטלוג הקבצים בארכיון
* גיבוי חי של מערכת קבצים: מזהה מתי קובץ שונה בזמן שהוא נקרא לגיבוי ויכול לנסות שוב לשמור אותו עד למספר מרבי נתון של ניסיונות חוזרים
* קובץ Hash (MD5, SHA1 או SHA-512) שנוצר תוך כדי תנועה עבור כל פרוסה, הקובץ המתקבל תואם ל-md5sum או sha1sum, כדי להיות מסוגל לבדוק במהירות את שלמות כל פרוסה
* מערכת קבצים עצמאית: ניתן להשתמש בה כדי לשחזר מערכת למחיצה בגודל שונה ו/או למחיצה עם מערכת קבצים אחרת[5]

## הפניות

* [DAR](http://dar.linux.free.fr/)
* [DAR Disk Archiver](https://en.wikipedia.org/wiki/Dar_(disk_archiver))

