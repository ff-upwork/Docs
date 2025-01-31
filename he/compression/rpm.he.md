{
  "date" : "2021-04-08",
  "keywords" :[ "קובץ rpm", "פורמט קובץ rpm", "מהו קובץ rpm", "קובץ", "דוגמה לrpm", "rpm file file","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPM - Red Hat Package Manager File",
  "description":"למד על פורמט קובץ RPM וממשקי API שיכולים ליצור ולפתוח קבצי RPM.",
  "linktitle" : "RPM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## מהו קובץ RPM?

קובץ עם סיומת rpm הוא חבילת מערכת הפעלה Red Hat Linux להתקנות של תוכניות במערכות לינוקס. מנהל החבילות של Red Hat משתמש בפורמט הקובץ RPM והוא מערכת ניהול חבילות בקוד פתוח בחינם. למרות שניתן להשתמש בקבצי RPM כפי שהם עבור התקנת תוכניות, ניתן להמיר אותם לפורמטים אחרים של חבילות כגון [DEB](/he/compression/deb/) באמצעות תוכנת Debian בשם Alien.

## פורמט קובץ RPM

קובץ RPM הוא קובץ בינארי שיכול להכיל קבוצה של קבצים. רוב הפעמים, קבצי RPM הם " RPMs בינאריים " שהם קובצי ההפעלה של התוכנה. קובץ RPM יכול להכיל RPMs מקור (SRPMs) שניתן להשתמש בהם כדי לבנות את החבילה מקוד המקור. פורמט הקובץ RPM מורכב מארבעה חלקים.

* Lead - מזהה את הקובץ כקובץ RPM
* חתימה - ניתן להשתמש בה כדי להבטיח שלמות ו/או אותנטיות
* כותרת - מכיל מטא נתונים כולל שם חבילה, גרסה, ארכיטקטורה, רשימת קבצים וכו'.
* ארכיון קבצים - ידוע גם בשם מטען, שבדרך כלל הוא בפורמט cpio, דחוס עם [GZIP](/he/compression/gz/)

## הפניות

* [RPM - ויקיפדיה](https://rpm.org)
* [תיעוד RPM](https://rpm.org/documentation.html)

