---
date: 2019-10-11
keywords: WEBM, מהו קובץ WEBM, פורמט קובץ WEBM
מְחַבֵּר:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "למד על פורמט קבצי WEBM וממשקי API שיכולים ליצור ולפתוח קובצי WEBM."
title: WEBM - WebM Video File Format
linktitle: WEBM
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## מהו קובץ WEBM?

קובץ עם סיומת .webm הוא קובץ וידאו המבוסס על פורמט קובץ WebM הפתוח ללא תמלוגים. הוא תוכנן לשיתוף וידאו באינטרנט ומגדיר את מבנה מיכל הקבצים כולל פורמטים של וידאו ואודיו. WebM הוא 100% חינמי, מיישם איכות גבוהה המבוססת על טכנולוגיות פתוחות כגון HTML, HTTP ו-TCP/IP הפתוחות לכל אחד להטמעה. WebM תוכנן במיוחד להגשת וידאו באינטרנט, מה שהופך אותו למוטב לסטרימינג עם טביעת רגל חישובית נמוכה. זה הופך אותו למתאים להשמעת סרטונים בכל מכשיר, במיוחד נטבוקים, מחשבי כף יד וטאבלטים בעלי הספק נמוך.

## פורמט קובץ WEBM

מבנה הקבצים של WebM מבוסס על תת-קבוצה של פורמט קובץ המכיל Matroska [MKV](/he/video/mkv/). זרמי הווידאו הזמינים בקובץ WebM נדחסים באמצעות טכנולוגיות הדחיסה VP8 או VP9 שהן יעילות מאוד בדחיסה. באופן דומה, זרמי האודיו בקובץ WebM נדחסים באמצעות קודקים Vorbis או Opus שפותחו על ידי [קרן Xiph](https://www.xiph.org/). כל הסרטונים והקודקים האודיו הללו הם ללא תמלוגים וניתן להשתמש בהם ללא כל חיוב.

להלן המפרטים המסוכמים עבור פורמט הקובץ WebM.

|שדה|תיאור|
---|---|
|סוג MIME |video/webm|
|אודיו בלבד מסוג MIME |audio/webm|
|מזהה סוג אחיד| org.webmproject.webm|
|שם Codec וידאו| VP8 או VP9|
|שם Codec אודיו| Vorbis או Opus|

### WebM Elements

WebM, בהיותה תת-קבוצה של מפרטי Matroska, מספקת תמיכה בחלק מהפונקציונליות של Matroska. להלן תיאור של האלמנטים הנתמכים.

#### EBML

|שם |תיאור|
---|---|
|EBML|הגדר את מאפייני ה-EBML של הנתונים הבאים. כל מסמך EBML צריך להתחיל בזה.|
|EBMLVersion |הגרסה של מנתח EBML המשמשת ליצירת הקובץ.|
|EBMLReadVersion|גרסת ה-EBML המינימלית שמנתח צריך לתמוך כדי לקרוא את הקובץ הזה.|
|EBMLMaxIDLength |האורך המרבי של המזהים שתמצא בקובץ זה (4 או פחות ב-Matroska).|
|EBMLMaxSizeLength|האורך המרבי של הגדלים שתמצא בקובץ זה (8 או פחות ב-Matroska). זה לא מחליף את גודל האלמנט המצוין בתחילת אלמנט. אלמנטים בעלי גודל מצויין גדול מהמותר על ידי EBMLMaxSizeLength ייחשבו כבלתי חוקיים.|
|DocType|מחרוזת המתארת את סוג המסמך העוקב אחרי כותרת EBML זו ("webm" במקרה שלנו).|
|DocTypeVersion|הגרסה של מתורגמן DocType המשמשת ליצירת הקובץ.|
|DocTypeReadVersion|גרסת DocType המינימלית שמתורגמן צריך לתמוך כדי לקרוא קובץ זה.|

#### אלמנטים גלובליים

נכון לעכשיו, רק הרכיב 'Void' נתמך המשמש לביטול נתונים פגומים, כדי למנוע התנהגויות בלתי צפויות בעת שימוש בנתונים פגומים. התוכן מושלך. משמש גם לשמירת מקום בתת-אלמנט לשימוש מאוחר יותר.

#### פלח
אלמנט זה מכיל את כל שאר האלמנטים ברמה העליונה (רמה 1). בדרך כלל קובץ Matroska מורכב מקטע אחד.

#### מטא חיפוש מידע

המידע הבא לחיפוש נתמך.

|שם הרכיב |תיאור|
---|---|
|SeekHead |מכיל את המיקום של אלמנט נוסף ברמה 1.|
|Seek |מכיל ערך חיפוש בודד לרכיב EBML.|
|SeekID |המזהה הבינארי המתאים לשם האלמנט.|
|SeekPosition |מיקום האלמנט בקטע באוקטטים (0 = אלמנט ברמה ראשונה).|

## הפניות

* [WebM](https://www.webmproject.org/)
* [מאגרי קוד WebM](https://www.webmproject.org/code/#webp-repositories)

