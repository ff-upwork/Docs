{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ FIT- קובץ פעילות של Garmin",
  "description":"למד על פורמט קובץ FIT וממשקי API שיכולים ליצור ולפתוח קובצי FIT.",
  "linktitle" : "FIT",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## מהו קובץ FIT?

קובץ FIT הוא קובץ GIS שנוצר על ידי מכשירי ספורט לבישים של Garmin. הוא משמש כדי לתעד את הפעילויות של האדם כאשר הוא/היא זז כשהוא לובש מכשירים אלה. נתוני הפעילות כוללים מיקום וזמן כפי שתועדו במכשיר ה-GPS. קבצי FIT משמשים גם להעברת נתוני הפעילות המוקלטים באמצעות ממשקי API באינטרנט. זו הסיבה שקובצי FIT הם פורמט הקובץ הנפוץ ביותר לשיתוף נתוני כושר עם פלטפורמות כושר אחרות. פורמטים נפוצים אחרים של קבצים כוללים [GPX](/he/gis/gpx/), TCX ו-[KML](/he/gis/kml/).

## פורמט קובץ FIT - מידע נוסף

קובצי FIT נשמרים בתקליטור כקבצים בינאריים עם המידע שנרשם על ידי מכשירי Garmin עבור הפעילות. מידע המאוחסן בתוך קובץ FIT כולל:

* תאריך שעה
* סוגי ספורט
* נתוני הקפה ופיצול
* מסלול GPS
* נתוני חיישן
* אירועים להפעלה פעילה

ניתן לתעד את נתוני הפעילות בקובץ בזמן אמת או לייצא לאחר השלמת רישום הפעילות.

### הודעות פעילות FIT

קובץ פעילות FIT עשוי לכלול כמה סוגי הודעות נדרשים. להלן ההודעות הנדרשות עבור קובץ פעילות.

|הודעה|מטרה|
---|---|
|זיהוי קובץ| הודעת מזהה הקובץ נדרשת על ידי כל סוגי הקבצים FIT וצפויה להיות ההודעה הראשונה בקובץ. עבור קובצי Activity, המאפיין Type צריך להיות מוגדר ל-4.|
|פעילות| נדרשת הודעת פעילות יחידה בקובץ FIT Activity. כלולים בהודעת הפעילות המאפיינים חותמת זמן מקומית וספירת פעילויות באתר. חותמת הזמן המקומית משמשת לקביעת היסט אזור הזמן שניתן להחיל על כל חותמות הזמן בקובץ. רוב המכשירים מקליטים קבצי FIT בזמן אמת וספירת הפגישות לא תהיה ידועה עד סוף ההקלטה. בגלל זה, הודעת הפעילות תהיה לרוב ההודעה האחרונה בקובץ.|
|פגישה| קובצי פעילות יכילו הודעת הפעלה אחת או יותר. הודעת הפעלה היא סוג הודעת סיכום. זמן התחלה, זמן שחלף כולל, זמן טיימר כולל וחותמת זמן הם שדות חובה עבור כל הודעות הסיכום.|
|בק| הודעות הקפה מייצגות הקפות או מרווחים בתוך הפגישה. הודעת Lap היא סוג הודעת סיכום. זמן התחלה, זמן שחלף כולל, זמן טיימר כולל וחותמת זמן הם שדות חובה עבור כל הודעות הסיכום.|
|הקלט| הודעות שיא כוללות קואורדינטת GPS, מהירות, מרחק, דופק, כוח וכו'|

## משאבים שימושיים לקובץ FIT

* [פענוח קובצי פעילות FIT](https://developer.garmin.com/fit/cookbook/decoding-activity-files/)
* [קידוד קובצי פעילות FIT](https://developer.garmin.com/fit/cookbook/encoding-activity-files/)
 

## הפניות ##

* [קובץ פעילות FIT](https://developer.garmin.com/fit/file-types/activity/)

