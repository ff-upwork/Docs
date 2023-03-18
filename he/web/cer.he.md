{
  "date" : "2021-07-13",
  "keywords" :[ "CER", "הרחבה", "קובץ", "פורמט", "אינטרנט", "תעודה", "שפה" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CER - פורמט קובץ אישור",
  "description":"למד על פורמט קובץ CER וממשקי API שיכולים ליצור ולפתוח קובצי CER.",
  "linktitle" : "CER",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## מהו קובץ CER? ##

קובץ עם סיומת cer אחראי לאחסון מידע מסוים על תעודת הבעלים והמפתח הציבורי הספציפי. פורמט זה של קבצים אינו יכול לאחסן את המפתחות הפרטיים ויש לו את היכולת לאחסן רק תעודה אחת שהיא x509. רשויות האישורים המאובטחות במיוחד הן אלה השייכות ל-HTTPS, פרוטוקול מהימן ומאובטח לגלישה
ה-CER הוא אישור של השרת שלך. זה בדרך כלל מתקבל על ידי רשות האישורים עבור הדומיין. CER נחשב לרוב זהה ל-[CRT](/he/web/crt/), למרות ששניהם הם באותו פורמט של אישור SSL אך הם סיומות שמות קובץ שונות.
ניתן להשתמש בהם במערכות הפעלה פשוט על ידי פתיחת דפדפן ובדיקת אבטחת הדפדפן או האתר בשימוש.

## היסטוריה קצרה ##

בשנת 1995, Thawte הפכה לסמכות ההסמכה הראשונה לפתרון סוגיית אישורי SSL ציבוריים (Secured Socket Link) מחוץ לארה"ב. לאחר מכן, יש שורה של רשויות כאלה שנוסדה בין 1995 ל-2020.

## פורמט קובץ CER ##

קבצים אלה יכולים להיות פשוטים
* PKC S#7 כולל קידוד Base64 ASCII
* סיומות הקובץ שלה הן p7b או p7cZ
* עבור תוכן בינארי, האישור יהיה DER או pkcs12/pfx.
ישנם סוגים רבים של קבצי אישורים עם כמה מפרטים ייחודיים:
* .pem, כאשר ארגון usThawteificate משרשר פורמט זה ידוע כיוצר אישורים
* .arm, כאשר נדרשת השיטה לחילוץ הסמכה מסייעת בחתימה עצמית, הפורמט שצוין למטרה זו הוא .arm. הוא מיוצג בקידוד ASCII בסיס 64.
* .der, זה מורכב מנתונים בינאריים. המשמעות היא שניתן להשתמש בו עבור תעודה בודדת בלבד
* .pfx (PKC512), זה מורכב ממפתח פרטי התואם לאישור שהונפק על ידי CA או אישור בחתימה עצמית. פורמט זה ידוע בהמרה של מימוש SSL אחד לאחר.

