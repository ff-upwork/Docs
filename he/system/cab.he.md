{
  "date" : "2021-06-29",
  "keywords" :[ "CAB", "הרחבה", "קובץ", "פורמט", "מערכת", "קובץ Windows Cabinet", "Microsoft", "Installer", "SetUp", "AdvPak" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CAB - קובץ ארון Windows",
  "description":"למד על פורמט קבצי CAB וממשקי API שיכולים ליצור ולפתוח קובצי CAB.",
  "linktitle" : "CAB",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## מהו קובץ CAB? ##

קובץ עם סיומת .cab שייך לקובץ windows cabinet השייך לקטגוריית קבצי מערכת. זהו קובץ שנשמר בפורמט קובץ הארכיון בגרסאות של Microsoft Windows התומכות באלגוריתמים של נתונים דחוסים, כגון [LZX](/he/compression/lzx/), Quantum ו-[ZIP](/he/compression/zip/ ). הקובץ מגיע בשימוש חיוני כאשר משתמש או מפתח רוצים להכיל ולשתף נתוני התקנת תוכנה וקבצים. התכונות של דחיסת נתונים ללא אובדן וההסמכה הדיגיטלית הכלולה בקבצים אלה הופכות את הקובץ הזה למושלם לאחסון ושיתוף של קבצים כאלה. הוא תומך במתקינים שונים של מיקרוסופט כגון Device Installer, SetUp API ו-AdvPak.

## היסטוריה קצרה ##

קובץ CAB הוא סוג קובץ דחיסת נתונים שפותח על ידי מיקרוסופט. זה נקרא בתחילה "יהלום", אבל אז הוא נודע בפופולרי כקובץ CAB, קיצור של המילה "ארון"

## מפרט טכני ##

קובץ CAB יכול להכיל בדרך כלל עד 65535 תיקיות לכל היותר, שיכולות, בתורן, להכיל מקסימום 65536 קבצים כל אחת. מנגנון אחסון קבצי CAB חסכוני בזמן ובמקום שכן הוא שומר כל תיקיה כבלוק דחוס במקום לדחוס ולאחסן כל קובץ בנפרד. לא ניתן לאחסן תיקיות ריקות בתיקיות ארכיון CAB. קובץ CAB פותח לראשונה על ידי מיקרוסופט ומשמש במתקינים שונים, כגון InstallShield בפורמט שונה במקצת. קבצי CAB מחוברים בדרך כלל לתוכניות לחילוץ עצמי. קבצי CAB של Microsoft ניתנים לזיהוי בקלות הודות לסמן הייחודי שלהם שעוזר בזיהוי הפורמט. הסמן הייחודי לכל קבצי CAB של Microsoft הוא קידומת של ארבע מילים, MSCF. כשהוא רואה קוד זה, משתמש יכול להבחין בקלות בין קובץ CAB של Microsoft מקבצים אחרים ולהשתמש בו בהתאם במדחסים או בגרסאות. ניתן לדחוס את הקבצים עם יותר נתוני התקנות תוכנה, או לשחרר את הנתונים הנוכחיים באמצעות התוכנה הנכונה.


## דוגמה של מונית ##

הדוגמה הבאה ממחישה את הקשר בין קבצים ותיקיות במבנה קבצי CAB:

{{< figure src="../cab.png" alt="פורמט קובץ CAB" >}}

## התייחסות ##

* [CAB - WIKIPEDIA](https://en.wikipedia.org/wiki/Cabinet_(file_format))
