{
  "date" : "2019-12-12",
  "keywords" :[ "FBX", "קובץ", "הרחבה", "פורמט", "פורמט קובץ תלת מימדי" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"מדריך פורמט הקבצים שלך כדי לדעת מהו קובץ FBX וממשקי API שיכולים ליצור ולפתוח אותם.",
  "title" :"FBX - FilmBox 3D File Format",
  "linktitle" : "FBX",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ FBX?

FBX, FilmBox, הוא פורמט קובץ תלת מימדי פופולרי שפותח במקור על ידי Kaydara עבור MotionBuilder. הוא נרכש על ידי Autodesk Inc בשנת 2006 וכעת הוא אחד מהפורמטים העיקריים של החלפת תלת-ממד בשימוש בכלי תלת-ממד רבים. FBX זמין בפורמט קובץ בינארי ו-ASCII. הפורמט הוקם כדי לספק יכולת פעולה הדדית בין יישומי יצירת תוכן דיגיטלי. ישנם כלים רבים זמינים להמרה מ/אל פורמט קובץ FBX.

## פורמט קובץ FBX - מידע נוסף

FBX הוא פורמט קנייני ומפרטים לגבי פורמט הקובץ הבינארי שלו אינם זמינים באופן רשמי. C++ FBX SDK מסופק על ידי Autodesk לקריאה, כתיבה והמרה אל/מקובץ FBX. סקריפט ייבוא וייצוא של Python עבור FBX זמין גם בתוכנת Blender שאינה משתמשת ב- FBX SDK.

### מבנה קובץ מבוסס טקסט

מבנה הקובץ המבוסס על טקסט הוא מבנה עץ מתועד עם מזהים בעלי שם ברור. הוא מורכב מרשימה מקוננת של צמתים המסודרים בהיררכיה כאשר לכל צומת יש:

* מזהה NodeType (שם מחלקה)
* טופלה של מאפיינים הקשורים אליו, רכיבי ה-tuple הם סוגי הנתונים הפרימיטיביים הרגילים: ##float, שלם, מחרוזת## וכו'.
* רשימה המכילה צמתים באותו פורמט (רקורסיבית).

אלה יכולים להיות מיוצגים באופן הגיוני כדלקמן:

```
NodeType: SomeProperty0a, SomeProperty0b, ... , {

 NestedNodeType1 : SomeProperty1a, ...
 NestedNodeType2 : SomeProperty2a, ... , {
 ... Sub-scope
 }

 ...
}
```

חלק מהצמתים הסטנדרטיים מוגדרים כרשימה מרומזת כאשר כל פריט מורכב מרשימה מקוננת. כל יישום שמתכוון לגשת לגיאומטריית FBX, צריך לנתח את התכנים הללו ולעשות להם משמעות שימושית. דוגמה לקובץ FBX מבוסס טקסט היא כמפורט להלן:

```
; FBX ...
; Copyright (C) 1997-2008 ...
; All rights reserved.
; ----------------------------------------------------
FBXHeaderExtension: {
    FBXHeaderVersion: 1003
    FBXVersion: 6000
    CurrentCameraResolution: {
        CameraName: "Model::Producer Perspective"
        CameraResolutionMode: "Window Size"
        CameraResolutionW: 1
        CameraResolutionH: 1
}
    CreationTimeStamp: {
    ...
}
}
;Object definitions
;------------------------------------------------------------------
Definitions: {
    Count: 2
    ObjectType: "Model" {
    Count: 2
}
}
...
```

## מבנה קבצים בינאריים של קבצי FBX

כפי שצוין קודם לכן, מפרטי פורמט קובץ FBX אינם זמינים באופן ציבורי עבור FBX. מכיוון ש-Blender Foundation מיישמת את פורמט הקובץ FBX מבלי להשתמש ב-SDK שסופק על ידי החברה, חלק מהפרטים על פורמט קובץ בינארי הם [זמינים](https://code.blender.org/2013/08/fbx-binary-file-format-specification/) כחלק מהטמעתו.

מבנה הקבצים הבינאריים פועל לפי הסדר הבא:

* כותרת ראשית
* שיא אובייקט
* כותרת תחתונה

### כותרת FBX

מידע כותרת הקובץ מורכב מ-27 בתים.

* בתים 0 - 20: Kaydara FBX Binary \x00 (קובץ-קסם, עם 2 רווחים בסוף, ולאחר מכן מסיים NULL).
* בתים 21 - 22: [0x1A, 0x00]## (לא ידוע אבל כל הקבצים שנצפו מציגים בתים אלה).
* בתים 23 - 26: int unsigned, מספר הגרסה. 7300 לגרסה 7.3 למשל.

### רשומת אובייקט ###

אחרי הכותרת מופיעה רשומת אובייקט שהיא רשומת צומת מלאה עם שם ריק ורשימת מאפיינים ריקה. הוא מכיל באופן רקורסיבי את כל צורת הקובץ.

### כותרת תחתונה ###

הקטע FBX Footer נמצא בסוף הקובץ שתוכנו אינו ידוע.

## פורמטים של שיא ##

רשומות בקובץ FBX מסווגות כ:

* רשומות צומת
* רישומי נכסים

### פורמט רשומת צומת ###

כל פורמט רשומה של צומת נקרא בשם ובעל פריסת הזיכרון הבאה.


|גודל (בייט)|סוג תאריך|שם
--- | ---|---|
|4|UInt32|EndOffset
|4|UInt32|NumProperties
|4|UInt32|PropertyListLen
|1|UInt8|שםLen
|NameLength|char|שם
|?|?|Property[n], כאשר n = 0:PropertyListLen
|אופציונלי| |
|?|?|NestedList
|13|uint8[]|Null-Record

איפה:

* `EndOffset` הוא המרחק מתחילת הקובץ לסוף רשומת הצומת (כלומר הבייט הראשון של מה שיבוא אחר כך). זה יכול לשמש כדי לדלג בקלות על רשומות לא ידועות או לא נדרשות.
* 'NumProperties' הוא מספר המאפיינים ב-tuple הערך המשויך לצומת. רשימה מקוננת כרכיב אחרון לא נספרת כנכס.
* `PropertyListLen` הוא האורך של רשימת הנכסים. זהו הגודל הנדרש לאחסון ##NumProperties## מאפיינים, אשר תלוי בסוג הנתונים של המאפיינים.
* `NameLen` הוא האורך של שם האובייקט, בתווים. נראה שהמקרה היחיד שבו זה 0 הוא הרשימות ברמה העליונה.
* `שם` הוא שם האובייקט. אין אפס סיום.
* `נכס[n]` הוא המאפיין ה-n. לפורמט, ראה סעיף מאפיין רשומה פורמט. מאפיינים נכתבים ברצף וללא ריפוד.
* `NestedList` היא הרשימה המקוננת, שנוכחותה מסומנת על ידי רשומת NULL ממש בסוף.

ניתן לקבוע את קיומו של ערך רשימה מקונן על ידי בדיקה אם נותרו בתים עד שמגיעים ל- EndOffset. אם כן, יש לקרוא את רשומת האובייקט הבאה ישירות אחרי המאפיין האחרון. לאחר מכן רשומת האובייקט עוקבת אחר 13 בתים אפס, אשר לאחר מכן משתלבים עם EndOffset. המטרה או הדרישה של הערך NULL אינן ידועות ועשויות להצביע על תכונת פורמט כלשהי.

### פורמט רשומת נכס ###

רשומת נכס מכילה פרטים על נכסים שהם חלק מ-Node. לרשומת מאפיין יש את פריסת הזיכרון הבאה:


|גודל (בייט)|סוג נתונים|שם
--- | --- | ---
|1|char|TypeCode
|?|?|נתונים

TypeCode מייצגים קודי תווים אשר מסודרים בקבוצות הדורשות טיפול דומה. ניתן לסווג TypeCodes בסוגים הבאים ו-TypeCode יכול להיות אחד מקודי התווים מבין הסוגים הללו.

#### סוגים פרימיטיביים ####

```
Y: 2 byte signed Integer
C: 1 bit boolean (1: true, 0: false) encoded as the LSB of a 1 Byte value.
I: 4 byte signed Integer
F: 4 byte single-precision IEEE 754 number
D: 8 byte double-precision IEEE 754 number
L: 8 byte signed Integer
```

הנתונים ברשומת הסוג הסקלרי הפרימיטיבי הם בדיוק הייצוג הבינארי של הערך, בסדר בתים קטן-אנדיאן.

#### סוגי מערכים ####

```
f: Array of 4 byte single-precision IEEE 754 number
d: Array of 8 byte double-precision IEEE 754 number
l: Array of 8 byte signed Integer
i: Array of 4 byte signed Integer
b: Array of 1 byte Booleans (always 0 or 1)
```

הנתונים עבור סוג מערך מורכבים יותר ונמצאים במבנה הבא.


|גודל (בייט)|סוג נתונים|שם
--- | --- | ---
|4|Uint32|ArrayLength
|4|Uint32|קידוד
|4|Uint32|אורך דחוס
|?|?|תוכן

### סוגים מיוחדים ###

להלן סוגים מיוחדים TypeCodes.

```
S: String
R: raw binary data
```

שני ה-TypeCodes הללו מיוצגים כדלקמן:


|גודל (בייט)|סוג נתונים|שם
--- | --- | ---
|4|Uin32|אורך
|אורך| |

המחרוזת אינה בעלת סיומת אפס, ועשויה להכיל תווים \0 (זה משמש למעשה בחלק ממאפייני FBX).

## הפניות ##

* [FBX - The Autodesk SDK](https://help.autodesk.com/view/FBX/2017/ENU/)
* [מפרטי פורמט קובץ בינארי של FBX](https://code.blender.org/2013/08/fbx-binary-file-format-specification/)
* [FBX - ויקיפדיה](https://en.wikipedia.org/wiki/FBX#File_format)

