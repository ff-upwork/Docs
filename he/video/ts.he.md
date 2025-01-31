{
  "date" : "2021-12-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ TS - קובץ זרם העברת וידאו",
  "keywords" :[ "ts", "זבוב", "הרחבה", "הרחבה", ".ts", "פורמט" ],
  "description":"למד על מהו קובץ TS וממשקי API שיכולים ליצור ולפתוח קבצי TS.",
  "linktitle" : "TS",
  "menu" : {
    "docs" : {
      "identifier":"video-ts",
      "parent" : "video"
}
},
  "lastmod" : "2021-12-16"
}

## מהו קובץ TS?

קובץ עם סיומת .ts הוא זרם וידאו המאחסן את הנתונים ב-DVD. הוא משתמש באלגוריתם דחיסה MPEG-2 ([.mpeg](/he/video/mpg/)) כדי להשיג יעילות ותאימות מקסימלית בין סוגי מדיה שונים כגון הזרמת אינטרנט ושידור. פורמט קובץ TS נוצר כך שניתן להפעיל אותו במכשירים עם חיבורי אינטרנט לקויים, כגון טלוויזיה חכמה.

## פורמט קובץ TS - מידע נוסף

הנתונים בקובץ TS דומים לקובץ [MP4](/he/video/mp4/), אך הם מחולקים לגושים זעירים. כל נתח מורכב מחתיכת וידאו זעירה, ואחריה מעט אודיו וכיתוב אופציונלי. קובץ TS בודד מורכב מהרבה נתחים כאלה. בנוסף לווידאו, אודיו וכיתוב, כל נתח מורכב גם מכמה נתונים נוספים לזיהוי שגיאות בנתח. בשל כך, קבצי TS גדולים במידת מה.

### מדוע להשתמש בפורמט קובץ TS?

אז אם קבצי TS הם קצת גדולים בגודלם, איזה יתרון זה מציע להשתמש בהם במקום פורמטים אחרים של קבצים? ובכן, בשידור, ניתן לשלוח את הנתחים הזעירים של וידאו ואודיו דרך אמצעי התקשורת (קווית או רדיו) בזמן אמת. הנתונים הנוספים בנתחים משמשים את המקלט כדי לדלג על הנתחים המועדים לשגיאות.

בנוסף, נעשה שימוש בקבצי TS מכיוון שמערכת השידור לא צריכה את כל הזרם כדי להפעיל אותו. ניתן לקלוט את השידור וניתן להשתמש בו בזמן אמת על ידי הרכבת אודיו ווידאו.

## איך לשחק קבצי TS?

ובכן, ניתן לפתוח ולהפעיל קבצי TS ב-[VideoLAN VLC media player](https://www.videolan.org/vlc/features.html) הזמין להורדה באופן חופשי.

## הפניות ##

* [MPEG Transport Stream - ויקיפדיה](https://en.wikipedia.org/wiki/MPEG_transport_stream)

