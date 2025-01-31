---
date: 2019-10-11
keywords: kt, .kt, פורמט קובץ kotlin, כיצד לפתוח קבצי kotlin, כיצד להפעיל קבצי kotlin, פורמט קובץ .kt, קובץ kt , סיומת קובץ kotlin, .kt extension, kotlin vs java
מְחַבֵּר:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: פורמט קובץ KT
linktitle: KT
description: "למד על פורמט קובץ KT וממשקי API שיכולים ליצור ולפתוח קבצי KT."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-20
---

## מהו קובץ KT? ##

קוד מקור שנכתב ב-Kotlin נשמר עם סיומת .kt הידועה בכינויה **סיומת קובץ Kotlin**. ה-Kotlin היא שפת תכנות חוצת פלטפורמות למטרות כלליות שפותחה על ידי JetBrains כדי להיות ניתנת להפעלה הדדית מלאה עם [Java](/he/programming/java/). הסימן המסחרי של קוטלין מוגן על ידי קרן קוטלין.

Kotlin הוכרזה כשפת התכנות המועדפת לפיתוח אפליקציות אנדרואיד על ידי גוגל ב-7 במאי 2019. Android Studio 3.0 החל לתמוך ב-Kotlin כחלופה לפיתוח אפליקציות אנדרואיד באוקטובר 2017.

## היסטוריה קצרה של פורמט קובץ Kotlin KT##

קוטלין נחשפה על ידי JetBrains ביולי 2011 כשפת תכנות חדשה עבור JVM. המנהיג של JetBrains דמיטרי ג'מרוב אמר שברוב השפות חסרו תכונות שהם חיפשו מלבד סקאלה, אבל הקומפילציה האיטית של סקאלה הייתה חיסרון. אחת המטרות העיקריות של קוטלין הייתה קומפילציה במהירות כמו ג'אווה. פרויקט Kotlin היה בקוד פתוח תחת רישיון Apache 2 בפברואר 2012.

גרסה 1.0 של Kotlin שוחררה ב-15 בפברואר 2015. אנדרואיד הכריזה על תמיכה מהשורה הראשונה ב-Kotlin באנדרואיד ב-Google I/O 2017. Kotlin 1.2 שוחררה ב-28 בנובמבר 2017 עם היכולת לשתף קוד בין פלטפורמות JVM ו-JavaScript. Kotlin 1.3 שוחרר ב-29 באוקטובר 2018 עם תמיכה בתכנות אסינכרוני. גוגל הכריזה על Kotlin להיות שפת התכנות המועדפת לפיתוח אפליקציית אנדרואיד ב-7 במאי 2019. Kotlin 1.4 שוחרר באוגוסט 2020 עם כמה שינויים קלים כדי לתמוך בפעולה הדדית עם Swift/Objective-C.

## תחביר קוטלין ##

Kotlin תוכנן להיות טוב יותר מג'אווה אבל עדיין להיות פעיל עם קוד Java כדי לאפשר העברה הדרגתית מג'אווה לקוטלין.

* נקודה-פסיק הם אופציונליים בקוטלין. די בשורה חדשה כדי לציין את סוף ההצהרה.
* קוטלין תומך בשני סוגים של משתנים, לקריאה בלבד, המוגדרים על ידי מילת המפתח *val*, וניתנים לשינוי, המוגדרים על ידי מילת המפתח *var*.
* השיעורים הם פרטיים וסופיים כברירת מחדל. כדי לנבוע ממחלקה, יש להצהיר על מחלקת הבסיס עם מילת המפתח *פתוח*.
* קוטלין תומך גם בתכנות פרוצדורלי.
* נקודת הכניסה לתוכנית Kotlin היא הפונקציה ה"ראשית" בדומה ל-Java, C# וכו'.

### דוגמה תחביר ###

להלן דוגמה לתחביר קוטלין.

```kotlin
// The example code prints Hello World from Kotlin to the console.
    fun main() {
      val audience = "World"
      println("Hello, $audience!")
}
```

בקוד לעיל, מילת המפתח **כיף** מגדירה את הפונקציה בשם main. בתוך הפונקציה, משתנה לקריאה בלבד 'קהל' מוצהר עם מילת המפתח **val**. על ידי שימוש בשיטת **println**, "Hello World from Kotlin" מודפס על הקונסולה. הערך של הקהל המשתנה מוזרק למחרוזת עם הסימן **$**.

## קוטלין נגד ג'אווה
ה-Kotlin היא שפה רשמית לכתיבת אפליקציות אנדרואיד עם תכונות מתקדמות רבות, אך מפתחי Java מומחים רבים עדיין לא מראים את העניין שלהם לעבור ל-Kotlin. הם חושבים שהם יכולים לעשות הכל רק עם Java. אז להלן ההשוואה בין שתי טכנולוגיות שעשויות לשכנע את מפתחי Java לעבור:

| פרמטר | Java | קוטלין |
|--------------------|--------|---------------- -|
| אובייקטים יחידים | √ | √ |
| סוגי תווים כלליים | √ | Χ |
| קומפילציה | Bytecodes | מכונה וירטואלית |
| ביטוי למדה | Χ | √ |
| מערך בלתי משתנה | Χ | √ |
| שדות לא פרטיים | √ | Χ |
| שחקנים חכמים | Χ | √ |
| בטיחות אפס | Χ | √ |
| חברים סטטיים | √ | Χ |

## הפניות ##

- [Kotlin (שפת תכנות) - ויקיפדיה](https://en.wikipedia.org/wiki/Kotlin_(programming_language))

