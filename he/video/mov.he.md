{
  "date" : "2019-10-11",
  "keywords" :[ "קובץ mov", "פורמט קובץ mov", "מהו קובץ mov", "קובץ", "דוגמה ל-mov", "סיומת קובץ mov","סיומת", "פורמט", "QuickTime", "MPEG- 4 אינץ'"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"קובץ MOV - פורמט קובץ סרטים של Apple QuickTime",
  "description":"למד על פורמט קובץ MOV וממשקי API שיכולים ליצור ולפתוח קובצי MOV.",
  "linktitle" : "MOV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-29"
}

## מהו קובץ MOV?

קובץ MOV הוא סוג קובץ וידאו, שפותח על ידי Apple Inc., המכיל רצועה אחת או יותר. כל רצועה מאחסנת סרט, אודיו, קטעי סרטים וכתוביות. זהו מיכל מולטימדיה שיכול לאחסן סוגים שונים של רכיבי מדיה. פורמט הווידאו MOV תואם הן למערכות Windows והן למערכות מקינטוש. הוא משתמש ב-MPEG-4 המקודד לדחיסה ומסלולים נשמרים באובייקטים הנקראים אטומים אשר ממוקמים במבנה נתונים היררכי.

## היסטוריה קצרה של פורמט קובץ MOV

פורמט הקובץ MPEG-4 התפתח ממפרט QuickTime File Format (**QTFF**) בשנת 2001. ארגון התקינה הבינלאומי אישר את הפורמט ומפרטי המערכות MPEG-4 Part 1 פורסמו בשנת 1999. בשנת 2001, קובץ עדכון פורמט [MP4](/he/video/mp4/) פורסם.

הגרסה הראשונה של MP4 עודכנה בשנת 2003 כ-MPEG-4 חלק 14 (ISO/IEC 14496-14:2003). בשנת 2004, MP4 הוכלל כדי להגדיר מבנה כללי לכל קבצי המדיה מבוססי הזמן. לכן, כעת הוא משמש כבסיס לפורמטים שונים של קבצי מולטימדיה.

## פורמט קובץ QuickTime (QTFF) - מידע נוסף

על מנת לעבוד עם מולטימדיה דיגיטלית, QTFF יכול להחזיק סוגים רבים של נתונים. זהו פורמט רעיון לחילופי מדיה דיגיטלית שכן הפורמט מגדיר את הסטנדרטים לתיאור כל סוג של מבני מדיה. פורמט הקובץ מורכב מאוסף גמיש של אובייקטים מונחה עצמים. לאחסון סרטים על דיסקים, QuickTime משתמש בשני מבנים, כלומר `אטומים` ו`אטומי QT`.

### אטומים

Atom היא היחידה הבסיסית של קובץ QuickTime. ישנם שני שדות עיקריים בכל אטום לפני כל שדה אחר: שדות גודל וסוג. שדה הגודל מציג את גודל האטום בעוד ששדה הסוג מציין את סוג הנתונים המאוחסנים באטום. מטבעם, אטומים הם היררכיים, מה שאומר שאטום אחד יכול להכיל אטומים אחרים שעדיין יכולים להכיל אחרים. הפריסה של אטום לדוגמה מוצגת בתמונה הבאה.

לכל אטום שני חלקים, 'כותרת' ו'נתונים'. הכותרת מכילה את שדות הגודל והסוג וחלק הנתונים מכיל את הנתונים בפועל. בהמשך, כל שדה מוסבר להלן:

### גודל אטום

הכותרת והתוכן של האטום מסומנים על ידי מספר שלם של 32 סיביות המכונה גודל האטום. שדה הגודל מכיל את גודל האטום בבתים, המבוטא במספר שלם של 32 סיביות ללא סימן.

### סוג אטום

סוג האטום מוצג גם על ידי מספר שלם של 32 סיביות, שלרוב מתייחסים אליו כשדה בן ארבעה תווים עם ערך קנמוני, כגון 'moov' (0x6D6F6F76) עבור אטום סרט, או 'trak' (0x7472616B) עבור אטום מסלול. ברגע שסוג האטום ידוע, הוא מאפשר לפרש את הנתונים שלו.

### QT Atoms ומיכלי Atom

אטומי QT מספקים פורמט אחסון לשימוש כללי ויש להם כותרת מורחבת המורכבת משדות גודל, סוג, מזהה אטום וספירת אטומי ילדים. אטומי QT עטופים במיכל אטום, מבנה נתונים ייחודי בעל כותרת עם ספירת נעילה. יש אטום שורש אחד בכל מיכל אטום שהוא אטום QT. הפריסה של אטום QT מוצגת באיור למטה.

לכותרת מיכל אטום QT יש את הנתונים הבאים:

שמור: אלמנט של 10 בתים עם ערך 0.

ספירת מנעולים: מספר שלם של 16 סיביות עם ערך של 0.

לכותרות אטום QT יש את הנתונים הבאים:

**גודל -** כותרת אטום QT והתוכן מסומנים בבתים על ידי מספר שלם של 32 סיביות. במקרה של אטום עלה, אז שדה זה מכיל גודל של אטום בודד.

**סוג -** סוג האטום מסומן במספר שלם של 32 סיביות. במקרה שזהו אטום השורש, אז הערך מוגדר ל'sean'.

**מזהה האטום -** זהו מספר שלם של 32 סיביות המציג את מזהה האטום וחייב להיות ייחודי לכל האחים. אטום השורש תמיד הערך של מזהה האטום כ-1.

**שמור -** מספר שלם של 16 סיביות שיש להגדיר ל-0.

**ספירת ילדים -** מספר שלם של 16 סיביות המציין את מספר אטומי הצאצא של אטום.

**שמור -** מספר שלם של 32 סיביות שיש להגדיר ל-0.

## מבנה קבצים של קבצי MOV

קבצי MOV מורכבים מנתחים רצופים. לכל נתח יש כותרת של 8 בתים: גודל נתח של 4 בתים (ביג-אנדיאן, בייט גבוה ראשון) וסוג נתח של 4 בתים - אחת מהחתימות המוגדרות מראש: "ftyp", "mdat", "moov", "pnot" ", "udta", "uuid", "moof", "free", "skip", "jP2", "wide", "load", "ctab", "imap", "matt", "kmat", "קליפ", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". הנתח הראשון הוא מסוג "ftype" ויש לו תת-סוג בהיסט 8. MOV מוגדר לפי תת-סוג שחייב להיות "qt". כדי להרכיב קובץ MOV, יש צורך באיטרציה של נתחים עד לזיהוי סוג לא ידוע.

הנה `דוגמה לדוגמה`: בדיקת הנתונים הבינאריים לדוגמה של קובץ MOV ברור שהוא מתחיל בחתימה **ftyp** (hex: 66 74 79 70) בהיסט 4, המגדיר את QuickTime Container File Type. תת-סוג הקובץ הוא **qt~_~_** (hex: 71 74 20 20) מה שמצביע על סוג קובץ MOV. גודל הבלוק הראשון הוא 32 (hex: 00 00 00 20, big-endian, בייט גבוה ראשון), הגודל ממוקם בהיסט 0. בהיסט 32 (hex: 20) ממוקם הנתח השני, שגודלו 8 ו סוג **mdat** (hex: 6D 64 61 74).

הנתח הבא ממוקם ב-offset 32+8#40 (hex: 28) ויש לו גודל 3,263,028 (hex: 00 31 CA 34) וסוג **mdat** (hex: 6D 64 61 74) ב-offset 44 (hex : 2C). הנתח הבא ממוקם ב-offset 40 + 3,263,028#3,263,068 (hex: 00 31 CA 5C) ויש לו גודל 21,189 (hex: 00 00 52 C5) וסוג **moov** (hex: 6D 6F 6F 76) 1,836,019,574 (משקס: 00 31 CA 60). זהו הנתח האחרון, כך שגודל הקובץ הכולל הוא 3,263,068+21,189#3,284,257 בתים.

## כיצד להמיר קובץ MOV?

ישנם שפע של נגני מדיה ועורכי וידאו תוכנה זמינים להמרת קבצי MOV פורמטים פופולריים אחרים של קבצי וידאו. חלק מנגני המדיה שיכולים להמיר קבצי MOV לפורמטים אחרים כוללים:

* נגן מדיה VideoLAN VLC
* נגן אלטימה אלמדיה

מספר נגני מדיה ועורכי וידאו, כולל VideoLAN VLC Media Player ו-Eltima Elmedia Player, יכולים להמיר קבצי MOV לפורמטים אחרים. תוכנות אלו יכולות להמיר קבצי MOV לפורמטי וידאו הבאים.

* וידאו MPEG-4 - [MP4](/he/video/mp4/)
* וידאו WebM - [WEBM](/he/video/webm/)
* זרם העברת וידאו - [TS](/he/video/ts/)
* פורמט מערכות מתקדמות - [ASF](/he/video/ts/)
* Ogg Vorbis Audio - [OGG](/he/audio/ogg/)
* אודיו MP3 - [MP3](/he/audio/mp3/)
* Codec אודיו ללא אובדן חינם - [FLAC](/he/audio/flac/)
* WAVE Audio - [WAV](/he/audio/wav/)

## API של קוד פתוח עבור קבצי MOV

* [React Native API להמרת MOV ל-MP4](https://github.com/taltultc/react-native-mov-to-mp4)
* [Python API לתיקון קבצי MOV](https://github.com/nrosenstein-stuff/movrepair)
* [Ruby API להמרת MOV ל-GIF](https://github.com/skygroundmedia/convert-mov-to-gif)

## הפניות

* [https://en.wikipedia.org/wiki/QuickTime_File_Format](https://en.wikipedia.org/wiki/QuickTime_File_Format)

