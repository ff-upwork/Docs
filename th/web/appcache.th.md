{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ APPCACHE - รูปแบบไฟล์รายการแคช HTML5",
  "description" :"เรียนรู้เกี่ยวกับไฟล์ APPCACHE และ API ที่สามารถสร้างและเปิดไฟล์ APPCACHE ได้",
  "linktitle" : "APPCACHE",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## ไฟล์ APPCACHE คืออะไร??

ไฟล์ APPCACHE เป็นไฟล์ข้อความที่มีรายการทรัพยากรที่เบราว์เซอร์จะแคชไว้สำหรับการเข้าถึงเว็บแอปพลิเคชันแบบออฟไลน์ สิ่งนี้มีประโยชน์เมื่อไม่มีการเชื่อมต่ออินเทอร์เน็ต ในสถานการณ์ดังกล่าว เบราว์เซอร์จะใช้ทรัพยากรแคชแบบออฟไลน์เพื่อให้สามารถเข้าถึงเนื้อหาเว็บได้ ไฟล์ APPCACHE มีทรัพยากรบนเว็บ เช่น รูปภาพ (เช่น **[PNG](/th/image/png/)**, **[WEBP](/th/image/webp/)** ฯลฯ), สไตล์ชีต **([ CSS])(/th/web/css/)** และไฟล์สคริปต์ (เช่น ไฟล์ Javascript **[JS](/th/web/js/)**)

แอปพลิเคชันที่สามารถ **เปิดไฟล์ APPCACHE** ได้แก่ เว็บเบราว์เซอร์ เช่น Google Chrome, Safari และ Firefox

## รูปแบบไฟล์ APPCACHE - ข้อมูลเพิ่มเติม

ไฟล์ APPCACHE เป็นไฟล์ข้อความธรรมดาที่ให้การเข้าถึงหน้าเว็บแบบออฟไลน์สำหรับการเรียกใช้งานโดยไม่ต้องเชื่อมต่ออินเทอร์เน็ต การปรากฏตัวของ APPCACHE กำหนดเพจว่าพร้อมใช้งานแบบออฟไลน์

### วิธีการอ้างอิงไฟล์ APPCACHE?

ในหน้า HTML ของคุณ มีการอ้างอิงไฟล์ APPCACHE ดังนี้

```
<html manifest="example.appcache">
  ...
</html>
```

## โครงสร้างไฟล์ Manifest ของ APPCACHE

ไฟล์รายการ APPCACHE อย่างง่ายมีลักษณะดังต่อไปนี้

```
CACHE MANIFEST
index.html
stylesheet.css
images/logo.png
scripts/main.js
http://cdn.example.com/scripts/main.js
```

นี่เป็นตัวอย่างที่ง่ายที่สุดและอาจมีโครงสร้างที่ซับซ้อนมากขึ้นเช่นกัน

## ข้อดีของ APPCACHE Manifest

การใช้อินเทอร์เฟซแคชทำให้เว็บแอปพลิเคชันมีข้อดีดังต่อไปนี้

1. การเรียกดูแบบออฟไลน์ - อินเทอร์เฟซแคชช่วยให้ผู้ใช้สามารถเรียกดูไซต์ทั้งหมดของคุณได้เมื่อออฟไลน์
1. ความเร็ว - แคชช่วยให้สามารถเข้าถึงเนื้อหาออฟไลน์ได้โดยตรงจากแผ่นดิสก์ด้วยความเร็วสูง
1. การเข้าถึงตลอดเวลา - ในกรณีที่ไซต์ของคุณหยุดทำงาน ผู้ใช้จะยังสามารถเข้าถึงเนื้อหาเว็บและจะได้รับประสบการณ์ออฟไลน์

## อ้างอิง

* [คู่มือเริ่มต้นใช้งาน AppCache Manifest](https://web.dev/appcache-beginner/)

