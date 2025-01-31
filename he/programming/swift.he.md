{
  "date" : "2019-10-11",
  "keywords" :[ ".swf", "SWF", "Apple swift", "קובץ", "סיומת", "פורמט קובץ", "מדריך אפל סוויפט", "מדריך תכנות" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SWIFT - קובץ קוד מקור של אפל",
  "description":"למד על פורמט קובץ SWIFT וממשקי API שיכולים ליצור ולפתוח קובצי SWIFT.",
  "linktitle" : "SWIFT",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## מהו קובץ Swift?

קובץ עם סיומת .swift מתייחס לשפת התכנות SWIFT שהציגה אפל לכתיבת יישומי תוכנה ואפליקציות עבור macOS, iOS, tvOS ועוד. לפני SWIFT, Objective-C הייתה שפת התכנות העיקרית לכתיבת יישומים. ניתן להשתמש בו עם Xcode שהוא ערכת כלים שלמה למפתחים ליצירת אפליקציות עבור Mac, iPhone, iPad, Apple Watch ו- Apple TV. SWIFT הוא חזק יותר, אינטראקטיבי, אקספרסיבי, ומציע יותר בטיחות בעיצוב מבלי להתפשר על הביצועים. ניתן לפתוח קבצי Swift לעריכה בכל עורך טקסט בנוסף ל-Apple Xcode. הוא תומך במערכות ההפעלה של אפל, לינוקס, חלונות ואנדרואיד.

## היסטוריה קצרה

* הפיתוח החל באמצע 2010 על ידי Chris Lattner עם תרומה של מתכנתים אחרים מאפל
* האפליקציה הרשמית הראשונה שנכתבה ב-SWIFT שוחררה ב-2 ביוני 2014 בכנס המפתחים העולמי של Apple (WWDC) וגרסת בטא של השפה שוחררה למפתחי אפל רשומים
* Swift 1.0 שוחרר ב-9 בספטמבר 2014 עם Xcode של iOS
* Swift 1.1 שוחרר ב-22 באוקטובר 2014, עם השקת Xcode 6.1
* Swift 1.2 שוחרר ב-8 באפריל, 2015, יחד עם Xcode 6.3
* Swift 2.0 הוכרז ב-WWDC 2015, והפך זמין לפרסום אפליקציות ב-App Store ב-21 בספטמבר 2015.
* Swift 3.0 שוחרר ב-13 בספטמבר 2016.
* Swift 4.0 שוחרר ב-19 בספטמבר 2017.
* Swift 4.1 שוחרר ב-29 במרץ 2018.
* שפת Swift הופיעה בקוד פתוח ב-3 בדצמבר 2015 יחד עם הספריות התומכות, מאפר הבאגים ומנהל החבילות שלה תחת רישיון Apache 2.0. הפרויקט התארח ב-[Swift.org](https://swift.org/) וקוד המקור שלו מתארח ב-[GitHub](https://github.com/apple/swift).
* במהלך WWDC 2019, אפל הכריזה על מסגרת SwiftUI לעיצוב מבנה ממשק משתמש בכל הפלטפורמות של אפל

## פורמט קובץ Swift - מידע נוסף

קבצי Swift הם קבצי טקסט רגיל שניתן לפתוח עם כל עורך טקסט. עורך הטקסט העיקרי המשמש לפתיחה ועריכה של קבצים מהירים הוא Xcode של אפל. חלקים רבים של Swift מכירים את פיתוח האפליקציות באמצעות C ו-Objective-C. התיעוד של Swift מספק [מדריך לפיתוח יישומים](https://docs.swift.org/swift-book/documentation/the-swift-programming-language/thebasics/) מפורט לכתיבת קוד באמצעות Swift.

## תכונות שפה של Swift

Swift נבדלת משפות תוכנית אחרות על סמך התכונות הבאות.

`מודרני` - פרמטרים בעלי שם באים לידי ביטוי בתחביר נקי שהופך ממשקי API ב-Swift לקלים יותר לקריאה ולתחזוקה. אפילו יותר טוב, אתה אפילו לא צריך להקליד נקודה-פסיק.

`בטיחות` - משתנים תמיד מאותחלים לפני השימוש, מערכים ומספרים שלמים נבדקים עבור גלישה, הזיכרון מנוהל אוטומטית ואכיפת גישה בלעדית לשומרי זיכרון מפני שגיאות תכנות רבות.

'מהיר ועוצמתי' - באמצעות טכנולוגיית המהדר LLVM בעלת הביצועים הגבוהים להפליא, קוד Swift הופך לקוד מקורי אופטימלי שמפיק את המרב מהחומרה המודרנית.

`תאימות מקור ובינארית` - אפליקציות שפותחו עם הגרסה הקודמת של Swift תואמות מהדורות חדשות ואין צורך להדר מחדש את קוד המקור. עם השקת Swift 5, ספריות Swift נכללות בכל מהדורת מערכת ההפעלה לעתיד. זה ימנע הכללה של ספריות Swift באפליקציות המכוונות למהדורות מערכת הפעלה נוכחית ועתידית.

`קוד פתוח` - Swift הוא קוד פתוח עם מאות תרומות מחברי Swift Community. הוא מגובה במעקב אחר באגים חזק, פורומים ובניית פיתוחים רגילים הזמינים לכולם.

## הפניות
* [Swift - GitHub](https://github.com/apple/swift)
* [Swift - ויקיפדיה](https://en.wikipedia.org/wiki/Swift_(programming_language))

