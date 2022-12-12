{
  "date" : "2019-12-03",
  "keywords" :[ "doc", "קובץ", "סיומת", "פורמט קובץ", "Word", "מסמך" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOC - Microsoft Word Document File",
  "description":"למד על פורמט קובץ DOC וממשקי API שיכולים ליצור ולפתוח קובצי DOC.",
  "linktitle" : "DOC",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## מהו קובץ DOC?

קבצים עם סיומת doc מייצגים מסמכים שנוצרו על ידי Microsoft Word או מסמכי עיבוד תמלילים אחרים בפורמט קובץ בינארי. התוסף שימש בתחילה לתיעוד טקסט רגיל במספר מערכות הפעלה שונות. זה יכול להכיל כמה סוגים שונים של נתונים כגון תמונות, מעוצבות כמו גם טקסט רגיל, גרפים, תרשימים, אובייקטים מוטבעים, קישורים, דפים, עיצוב עמודים, הגדרות הדפסה ועוד הרבה אחרים. הפורמט היה פופולרי לכל סוגי התיעוד בשל מגוון האפשרויות שהוא מציע למשתמשים לכתיבת מדריכים, הצעות, מפרטים, קורות חיים, מאמרים או כל מסמך דומה. הגרסה המעודכנת של DOC היא [DOCX](/he/Word%20Processing/DOCX/) המבוססת על Office OpenXML שהמפרט שלו זמין בגלוי.

## היסטוריה קצרה ##

WordPerfect, מוצר של [Corel](https://www.corel.com/en/), השתמש ב-DOC כהרחבה של הפורמט הקנייני שלהם. בשנות השמונים, WordPerfect נותרה בחירת השימוש ברוב המחשבים בשל זמינותו הקלה, התאמתו לרוב מכונות המחשב ומערכות ההפעלה. עם זאת, WordPerfect ראתה את נפילתו במערכת ההפעלה Windows כאשר מיקרוסופט הציגה את Microsoft Word כמוצר שלה לפורמט קובץ מסמכים ובחרה בסיומת DOC עבור הפורמט הקנייני שלהם. ככל ש-Microsoft Word הפכה יותר ויותר פופולרית, פורמט הקובץ DOC עבר מספר תיקונים מ-Microsoft Word 97 - 2003. זה היה 2007 כאשר פורמט קובץ ה-DOC המוגדר כברירת מחדל הוחלף בפורמט Office Open XML (המכונה DOCX) ובגירסאות החדשות של Microsoft Word משתמש כעת בתוסף החדש הזה כפורמט קובץ ברירת מחדל.

## מפרטי פורמט קובץ DOC - מידע נוסף

מיקרוסופט לא פרסמה את מפרטי פורמט הקובץ DOC במשך זמן רב עד 2008. בפברואר 2008, פורמטים של פורמטים פורמטים של קובץ doc תחת הבטחת המפרט הפתוח של Microsoft. למרות שהמפרט אינו מתאר את כל התכונות המשמשות את פורמט DOC, הוא מספק מידע רב על הידע הנדרש לעבודה עם פורמט קובץ זה. ובכל זאת, נדרשת הנדסה לאחור כדי לעשות שימוש במידע הזמין. המפרט עודכן מספר פעמים וה[גרסה] העדכנית ביותר (https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx) היא 8.0 שעודכנה נכון לאוגוסט 2018 .

### כמה מושגי יסוד ###

לפני שנכנס לפרטים כלשהם על מפרטי פורמט הקובץ עבור DOC, יש צורך להבין כמה מושגים בסיסיים כדי לעבוד עם פורמט קובץ זה.

**בסיס מידע קבצים (Fib):** מבנה ה-Fib מכיל מידע על המסמך ומציין את מצביעי הקובץ לחלקים שונים המרכיבים את המסמך.
ה-Fib הוא מבנה באורך משתנה. פרט לחלק הבסיס הקבוע בגודלו, לפני כל קטע יש שדה ספירה המציין את גודל הקטע הבא.

**מיקום התווים:** CP או Character Position מייצגים מספר שלם של 32 סיביות ללא סימן המשמש כאינדקס מבוסס אפס של תו בטקסט המסמך. לא ניתן לאחזר ישירות את המיקום והגודל של כל תו בקובץ ויש לחשב אותם באמצעות אלגוריתם שצוין מראש. הדמויות כוללות:

* טקסט המסמך
* עוגנים של אובייקטים כגון הערות שוליים או תיבות טקסט
* תווי שליטה כגון סימני פסקה וסימני תאי טבלה

**PLC:** מבנה ה-PLC הוא מערך של CPs ואחריו מערך של רכיבי נתונים. רכיבי הנתונים עבור כל PLC חייבים להיות באותו גודל של אפס או יותר בתים, ומסיבה זו, מספר ה-CPs חייב להיות אחד יותר ממספר רכיבי הנתונים. מבני PLC הם מסוגים שונים כאשר כל סוג מציין אם מותרים CPs כפולים עבור סוג זה או לא. מבנה PLC מורכב מ:

* **aCP (אורך משתנה):** מערך של רכיבי CP. כל סוג של מבנה **PLC** מציין את המשמעות של רכיבי ה-CP ואת הטווח המותר.
* **aData (אורך משתנה):** כל סוג של מבנה **PLC** מציין את המבנה והמשמעות של רכיבי הנתונים, כל הגבלה על מספר רכיבי הנתונים וכל הגבלה על הנתונים הכלולים בהם. זה גם מפרט את הקשר בין רכיבי הנתונים וה-CPs התואמים.

**בחירה חוקית:** מבני קובץ ה-DOC מתוארים בעיקר על ידי מגוון של CPs. ישנם מספר [כללים](https://msdn.microsoft.com/en-us/library/dd908861(v#office.12).aspx) שצוינו על ידי Microsoft שיש לפעול לפיהם במקרה כזה.

**STTB:** ה-STTB היא טבלת מחרוזות המורכבת מכותרת שאחריה מגיע מערך של אלמנטים. הערך **cData** מציין את מספר האלמנטים הכלולים במערך.

**אחסון נכסים:** קובץ word עשוי לכלול אלמנטים שונים כגון טקסט, פסקאות, טבלאות, תמונות וקטעים כאשר לכל אחד מהם יכולים להיות מאפיינים משלו. מאפיינים של אלה מאוחסנים בקובץ Word כהבדלים מברירת המחדל. הבדלים כאלה מוגדרים על ידי PRl המורכב מ-Single Property Modifier (Sprm) והאופרנד שלו. יישום יכול לקבוע את קבוצת המאפיינים הסופית על ידי יישום של רשימות של **Prl**s.

**הגנה על סיסמה:** ניתן להגן על קובצי Word גם באמצעות סיסמה, עבורם ניתן להשתמש באחד מהמנגנונים הבאים.

* ערפול XOR
* הצפנת RC4 של מסמך בינארי של משרד
* הצפנת מסמך בינארי של משרד RC4 CryptoAPI

אם FibBase.fEncrypted ו-FibBase.fObfuscation הם שניהם 1, הקובץ מעורפל באמצעות ערפול XOR.

אם FibBase.fEncrypted הוא 1 ו-FibBase.fObfuscation הוא 0, הקובץ מוצפן באמצעות הצפנת Office Binary Document RC4 או Office Binary Document RC4 CryptoAPI Encryption, כאשר EncryptionHeader מאוחסן בבייטים הראשונים של FibBase.lKey של זרם הטבלה. ה-EncryptionHeader.EncryptionVersionInfo מציין באיזה מנגנון הצפנה נעשה שימוש להצפנת הקובץ.

### מבנה הקובץ ###

קובץ Word בינארי במקוריותו הוא קובץ מורכב של OLE המורכב ממספר אחסון וזרמים. לאחסון ולזרמים הללו יש מבנה וגדלים משלהם, המציינים את הפרמטרים לכתיבה וקריאה. אלו הם:

#### WordDocument Stream ####

זרם זה מכיל את טקסט המסמך ומידע אחר שאליו מתייחסים מחלקים אחרים של הקובץ. לזרם אין מבנה מוגדר מראש מלבד ה-FIB בהתחלה שהוא חובה ואמור להיות ב-offset 0. זרם זה לא יכול להיות גדול מ-2147 MB.

#### 1TableStream או 0TableStream ####

קובץ Word בינארי יכול להכיל זרם טבלה הידוע כ-1Table stream או 0Table stream. לפחות אחד מאלה צריך להיות קיים במסמך. עם זאת, אם מסמך מכיל זרמי 1Table ו-0Table גם יחד, נעשה שימוש רק בזרם שאליו מתייחס base.fWhichTblStm. יש להתעלם מהזרם ללא הפניות.
ה-Table Stream לא יכול להיות גדול מ-2147 MB.

#### זרם נתונים ####

לזרם הנתונים אין מבנה מוגדר מראש. הוא מכיל נתונים שהפניה אליהם מ-FIB או מחלקים אחרים של הקובץ. זרם זה אינו חייב להיות נוכח אם אין אזכורים אליו. זרם הנתונים לא יכול להיות גדול מ-2147 MB.

#### אחסון מאגר חפצים ####

האחסון של מאגר האובייקטים מכיל אחסון עבור אובייקטי OLE משובצים. אחסון זה אינו חייב להיות קיים אם אין אובייקטי OLE מוטבעים במסמך.

#### אחסון נתוני XML מותאם אישית ####

אחסון נתוני XML מותאם אישית הוא אחסון אופציונלי ששמו חייב להיות "MsoDataStore".

#### זרם מידע סיכום ####

זרם מידע הסיכום הוא זרם אופציונלי ששמו חייב להיות "\005SummaryInformation", כאשר \005 הוא התו עם הערך 0x0005, ולא המחרוזת המילולית "\005".

#### זרם מידע סיכום מסמך ####

זרם המידע של סיכום המסמך הוא זרם אופציונלי ששמו חייב להיות "\005DocumentSummaryInformation", כאשר \005 הוא התו עם הערך 0x0005, ולא המחרוזת המילולית "\005".

#### זרם הצפנה ####

זרם ההצפנה הוא זרם אופציונלי ששמו חייב להיות "הצפנה". זרם זה לא חייב להיות נוכח אלא אם מתקיימים שני התנאים הבאים:

* המסמך מוצפן עם Office Binary Document RC4 CryptoAPI Encryption.
* הערך fDocProps מוגדר ב-EncryptionHeader.Flags.

#### אחסון מאקרו ####

אחסון המאקרו הוא אחסון אופציונלי המכיל את פקודות המאקרו של הקובץ. אם קיים, זה חייב להיות אחסון שורש לפרויקט.

#### אחסון חתימות XML ####

אחסון חתימות ה-XML הוא אחסון אופציונלי ששמו חייב להיות "_xmlsignatures".

#### זרם חתימות ####

זרם החתימות הוא זרם אופציונלי ששמו חייב להיות "_signatures". זרם זה מכיל חתימות דיגיטליות.

#### ניהול זכויות מידע אחסון נתונים שטח ####

אחסון הנתונים של ניהול זכויות המידע הוא אחסון אופציונלי ששמו חייב להיות "\006DataSpaces", כאשר \006 הוא התו עם הערך 0x0006, ולא המחרוזת המילולית "\006". אם האחסון הזה קיים, זרם התוכן המוגן חייב להיות נוכח גם הוא.
אם אחסון זה קיים, יש לקרוא את כל הזרמים והאחסון שצוינו מלבד האחסון הזה וזרם התוכן המוגן מזרם התוכן המוגן כמפורט ב-[MS-OFFCRYPTO] ואם אחד מהזרמים והאחסון הללו קיים מחוץ לתוכן המוגן זרם, יש להתעלם מהם.

#### זרם תוכן מוגן ####

זרם התוכן המוגן הוא זרם אופציונלי ששמו חייב להיות "\009DRMContent", כאשר \009 הוא התו עם הערך 0x0009, ולא המחרוזת המילולית "\009".
אם זרם זה קיים, אחסון שטח הנתונים לניהול זכויות מידע חייב להיות קיים.

## הפניות ##

* [מפרטי גיבוש קובץ MS-DOC](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx)
* [Doc Computing](https://en.wikipedia.org/wiki/Doc_(computing))
