{
  "date" : "2019-10-11",
  "keywords" :[ "M4V", "קובץ", "הרחבה", "פורמט", "MPEG-4", "ניהול זכויות דיגיטליות", "DRM", "Apple", "וידאו"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M4V",
  "description":"למד על פורמט קובץ M4V וממשקי API שיכולים ליצור ולפתוח קבצי M4V.",
  "linktitle" : "M4V",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-14"
}

## מהו קובץ M4V?

פורמט קובץ **M4V**, שפותח על ידי Apple, הוא מיכל וידאו המוגן אופציונלי עם הגנת העתקה Digital Rights Management (DRM) כדי להגן על פרטיות או העתקה. קטעי וידאו ורצועות אודיו עטופים על ידי קבצי מיכל לאינדקס וארגון זרמי השמעה. בנוסף, קונטיינרים מספקים גם תכונה של פרקים דומים לאלו שבדי.וי.די. אפל משתמשת ב-M4V כדי לקודד סרטונים ב-iTunes Store שלה. זה מגן על שכפול לא מורשה באמצעות הגנת ההעתקה FairPlay של אפל על ידי מתן אפשרות להפעיל קובצי M4V רק במחשבים מורשים שיש להם את החשבונות ששימשו לרכישת הסרטון. עם זאת, אם הגנת DRM מוסרת מקבצי M4V, ניתן להפעיל קבצים אלה בנגני וידאו אחרים על ידי שינוי הסיומת מ-.m4v ל-.mp4, וזו הסיבה שקובצי M4V משויכים ל-MPEG-4. M4V משתמש ב-H.264 עבור וידאו ו-**[AAC](/he/audio/aac/)** וב-Dolby Digital עבור קידוד ופענוח אודיו.

## מבנה קובץ M4V ##

לקבצי M4V יש נתחים רציפים עם כותרת של 8 בתים, גודל נתח של 4 בתים וסוג נתח של 4 בתים בכל נתח. הנתח הראשון הוא "ftype" ויש לו תת-סוג בהיסט 8. M4V מוגדר לפי תת-סוג שחייב להיות "M4V_". סוגי נתחים נוספים הם חתימות מוגדרות מראש: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2", "wide" , "טען", "ctab", "imap", "מאט", "kmat", "קליפ", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", " PICT". חוזרים על נתחים, עד שיזהה סוג לא ידוע, אנו יוצרים קובץ M4V.

הנה בדיקה של דוגמה: הנתונים הבינאריים של קובץ m4v לדוגמה נבדקים באמצעות Hex Viewer וניתן לראות שהוא מתחיל בחתימה **ftyp** (hex: 66 74 79 70) בהיסט 4, המגדיר את QuickTime סוג קובץ מיכל. תת-סוג הקובץ הוא **M4V_** (hex: 4D 34 56 20) המצביע על סוג קובץ M4V (MPEG-4). גודל הבלוק הראשון הוא 32 (hex: 00 00 00 20, big-endian, בייט גבוה ראשון), הגודל ממוקם בהיסט 0. בהיסט 32 (hex: 20) ממוקם הנתח השני, שגודלו 30,322 (hex : 00 00 76 72, big-endian, תחילה בייט נמוך יותר) והקלד **moov** (hex: 6D 6F 6F 76). הנתח הבא נמצא ב-offset 32+30,322#30,354 (hex: 00 00 76 92) ויש לו גודל 8 (hex: 00 00 00 08) וסוג **free** (hex: 66 72 65 65).
### קודקים בשימוש ב-M4V ###

#### וידאו Codec H.264 ####

H.264 הוא תקן דחיסת וידאו הממיר וידאו דיגיטלי לפורמט הדורש פחות מקום כאשר נדרש שידור או אחסון. M4V משתמש ב-H.264 לדחיסת וידאו. היישום שלו נע בין DVD, טלוויזיה, ועידות וידאו והזרמת וידאו דרך האינטרנט. H.264 מורכב משני חלקים עיקריים: Encoder - אשר דוחס את הווידאו, Decoder - אשר מבטל את הדחיסה של הווידאו הדחוס בחזרה. באיור למטה, תהליכי קידוד ופענוח מודגשים, ותהליכים אחרים מכוסים בתקן H.264.

##### תהליך קידוד ופענוח וידאו ב-H.264 #####

עבור זרם הסיביות הדחוס H.264, מקודד הווידאו עורך את תהליך החיזוי, הטרנספורמציה והקידוד. במקביל, המפענח מבצע תהליך הפוך של פענוח, טרנספורמציה הפוכה ושחזור כדי להפיק בחזרה את קובץ הווידאו. H.264 לוקח חצי מהגודל של MPEG.

#### Codec אודיו ####

קידוד אודיו מתקדם (AAC) הוא קודק שמע לדחיסת אודיו דיגיטלית מאבדת ומשמש במיכל M4V. AAC הוא היורש של פורמט [MP3](/he/audio/mp3/) ומשיג איכות טובה יותר מ-MP3 עם אותו קצב סיביות. פורמט AAC זורק קצת מידע במהלך תהליך הדחיסה, שהוא פחות חשוב. AAC הוא Codec מבוסס בלוק משתנה (VBR) שבו כל בלוק מפענח ל-1024 דוגמאות של תחום זמן.

### הפניות ###

* [ויקיפדיה - M4V](https://en.wikipedia.org/wiki/M4V)
* [ויקיפדיה - MPEG-4_AVC](https://en.wikipedia.org/wiki/H.264/MPEG-4_AVC)
