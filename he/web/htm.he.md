{
  "date" : "2019-10-11",
  "keywords" :[ "htm", "קובץ htm", "פורמט קובץ htm", "סוג קובץ htm", "קובץ", "סוג", "מהו קובץ htm" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ HTM",
  "description" :"מדריך פורמט הקבצים שלך כדי ללמוד מהו קובץ HTM וממשקי API שיכולים ליצור ולפתוח אותם.",
  "linktitle" : "HTM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ HTM?

קבצים עם סיומת **.htm** מייצגים Hypertext Markup Language ליצירת דפי אינטרנט לתצוגה בדפדפני אינטרנט כגון Google Chrome, Internet Explorer, Firefox ועוד מספר אחרים. הוא מגדיר את הסימון ליצירת דפים סטטיים לפרסום ברשת האינטרנט העולמית (WWW) לגישה לאחרים. סימון זה אומר לדפדפנים כיצד להציג את התוכן של דף אינטרנט. דפים כאלה יכולים להכיל טקסט רגיל, תמונות, היפר-קישורים לדפים אחרים, סרטונים ומידע מדיה אחר. כאשר דף אינטרנט מתפרסם, תוכל לעיין בקוד הסימון שמאחוריו על ידי הצגת מקור הדף שלו. דפדפנים מודרניים מאפשרים לבדוק כל חלק של דף אינטרנט שבו כל תת-חלוקה או רכיב סימון במקור HTM משוכלל.

## היסטוריה קצרה של HTM

מאז הקמתו ותפקידו הראשון, מפרטי ה-HTML נשמרים על ידי World Wide Web Consortium (W3C) מאז 1996. בשנת 2000, הוא גם הפך לתקן בינלאומי (ISO/IEC 15445:2000). בשנת 1999 פורסם HTML 4.01. בשנת 2004, קבוצת העבודה של Web Hypertext Application Technology (WHATWG) החלה לעבוד על גרסת HTML5 שהפכה למסירה משותפת עם ה-W3C בשנת 2008. היא הושלמה ותוקנה ב-28 באוקטובר 2014.

## פורמט קובץ HTML

מסמך HTML 4 מורכב משלושה חלקים:

1. שורה המכילה מידע על גרסת HTML
1. סעיף כותרת הצהרתית
1. גוף, המכיל את תוכנו בפועל של המסמך. הגוף עשוי להיות מיושם על ידי רכיב BODY או אלמנט FRAMESET כדי להכיל את הגוף במסגרות

כל קטע יכול להיות מוביל או אחריו רווחים לבנים, שורות חדשות, טאבים והערות. דוגמה למסמך HTML פשוט היא כפי שמוצג להלן:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
   <HEAD>
      <TITLE>Understanding HTML File Format</TITLE>
   </HEAD>
   <BODY>
      <P>Hello World!
   </BODY>
</HTML>
```

### מידע על הגרסה

שורת הקוד הראשונה,<!DOCTYPE html> , נקראת הצהרת doctype והיא אומרת לדפדפן באיזו גרסה של HTML הדף כתוב. בהתאם לגרסת ה-HTML, ישנן מספר הצהרות doctype שונות הנותנות שמות להגדרת סוג המסמך (DTD) הנמצאת בשימוש עבור המסמך. כל DTD שונה מהאחר באלמנטים שבהם הוא תומך ונבדלים כדלקמן:

* HTML 4.01 Strict - כולל את כל הרכיבים והמאפיינים שלא [הוצא משימוש](https://www.w3.org/TR/html401/conform.html#deprecated) או שאינם מופיעים במסמכים של ערכת מסגרות
* HTML 4.01 Transitional - כולל הכל ב-DTD המחמיר בתוספת אלמנטים ותכונות שהוצאו משימוש (רובם נוגעים להצגה חזותית
* HTML 4.01 Frameset - כולל גם הכל במסגרות המעבר DTD פלוס

עבור **HTML5**, מידע הגרסה הוא פשוט כפי שהוזכר להלן.

```
<!DOCTYPE html>
```

### מידע על כותרת

כותרת של מסמך HTML יכולה לכלול מספר רכיבי HTML שאינם מעובדים על ידי הדפדפן. אלמנטים כאלה הם מטא נתונים המתארים מידע על הדף או כוללים קטעים המשמשים לאחזר מידע ממשאבים חיצוניים כמו גיליונות סגנונות CSS או קובצי JavaScript. כותרת עליונה של עמוד מיוצגת על ידי \<head> תג ומסתיים ב-\</head> תָג.

<html>להגדרת כותרת העמוד, ה-\<title> אלמנט הוא היחיד שנדרש בתוך התגים \<head>. אותו הדבר משמש על ידי מנועי חיפוש כדי לזהות את הכותרת של דף. </html>

### מידע גוף

זהו החלק הראשי בקובץ המכיל את כל תוכן הקובץ שמעובד על ידי דפדפנים. גוף HTML יכול להכיל סימונים שיכולים להתייחס לאבני בניין שונות בצורת תגים. זה יכול להכיל כמה סוגים שונים של מידע כמו טקסט, תמונות, צבעים, גרפיקה וכו'. בנוסף, ניתן להטמיע רכיבי אודיו ווידאו בגוף ה-html לעיבוד על ידי דפדפנים. בנוכחות יישום גיליונות סגנון מודרניים לייצוג חזותי, תכונות המצגת של BODY כגון צבע רקע, צבע קישור, צבע טקסט וכו' הוצאו משימוש. לפיכך, ניתן להשיג את אותם אפקטים באמצעות גיליונות סגנונות כפי שמוצג להלן:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Inline Style Sheets referencing</TITLE>
 <STYLE type#"text/css">
  BODY { background: white; color: black}
  A:link { color: red }
  A:visited { color: maroon }
  A:active { color: fuchsia }
 </STYLE>
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>
```

גיליונות סגנונות מוטבעים קלים להטמעה ועבור יישומים מהירים לאפקטים החזותיים, גיליונות סגנונות חיצוניים הופכים את זה לנוח יותר לפריסה פעם אחת ולגישה במקומות רבים.

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Linking to External style sheets</TITLE>
 <LINK rel#"stylesheet" type#"text/css" href#"smartstyle.css">
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>

```

### רכיבי HTML

כפי שהוזכר קודם לכן, תוכן בתוך HTML Body מיוצג על ידי תגים, הידועים גם כ-Html Elements. לכל תג יכול להיות מידע נוסף בצורה של תכונות שנכתבות בשם
```
<tag attribute1#"value1" attribute2#"value2">
```
אם כי אין צורך לכלול תכונות עם כל תג. אם תכונות אינן מוזכרות, ערכי ברירת מחדל משמשים בכל מקרה. להלן כמה דוגמאות מהאלמנטים:

#### כותרת

```
<head>
  <title>The Title</title>
</head>
```

#### כותרות

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### פסקאות

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```

## הפניות

* [המבנה הגלובלי של מסמך HTML](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)
