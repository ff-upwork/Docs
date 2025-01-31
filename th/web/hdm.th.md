{
  "date" : "2022-10-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ HDM - ไฟล์ภาษามาร์กอัปของอุปกรณ์พกพา",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ HDM และ API ที่สามารถสร้างและเปิดไฟล์ HDM",
  "linktitle" : "HDM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-10-12"
}

## ไฟล์ HDM คืออะไร??

ไฟล์ HDM เป็นไฟล์เว็บเพจภาษามาร์กอัปที่สร้างขึ้นในภาษามาร์กอัปของอุปกรณ์พกพา (HDML) มีแท็กมาร์กอัปที่คล้ายกับภาษา [HTML](/th/web/html/) แต่ออกแบบมาสำหรับอุปกรณ์อิเล็กทรอนิกส์พกพา เช่น สมาร์ทโฟนและพีดีเอ [ข้อกำหนดรูปแบบไฟล์ HDML](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) ถูกส่งไปยัง W3C เพื่อสร้างมาตรฐาน แต่ไม่สามารถกลายเป็นมาตรฐานได้ HDM ขึ้นอยู่กับข้อกำหนดรูปแบบไฟล์ [HDML](/th/web/hdml/) ที่มีอยู่ในเว็บไซต์ W3

## รูปแบบไฟล์ HDM - ข้อมูลเพิ่มเติม

ไฟล์ HDM ประกอบด้วยแท็กมาร์กอัปที่แสดงผลไปยังเว็บไซต์ที่ออกแบบด้วยสายตาบนอุปกรณ์พกพา ไฟล์ HDM จะถูกคัดลอกไปยังอุปกรณ์ที่ใช้โปรโตคอล HDTP (Handheld Device Transport Protocol) แทนโปรโตคอล HTTP ซึ่งใช้สำหรับหน้า HTML

## องค์ประกอบไฟล์ HDML

ต่อไปนี้เป็นองค์ประกอบเล็กน้อยที่ให้สภาพแวดล้อมรันไทม์สำหรับ HDML และเรียกว่าตัวแทนผู้ใช้

|องค์ประกอบ|คำอธิบาย|
---|---|
|การ์ด|นี่คือองค์ประกอบพื้นฐานของ HDML และแสดงและอนุญาตให้ผู้ใช้โต้ตอบกับการ์ดข้อมูล |
|เด็ค|การ์ด HDML จะถูกจัดกลุ่มเข้าด้วยกันเป็นเด็ค สำรับ HDML คล้ายกับหน้า HTML ซึ่งระบุโดย URL [RFC1738] และเป็นหน่วยของเนื้อหาที่ร้องขอจากเซิร์ฟเวอร์และแคชโดยตัวแทนผู้ใช้|
|การดำเนินการ|การดำเนินการสามารถเป็นประเภท PREV, SOFT1-SOFT8 และ HELP สิ่งเหล่านี้เป็นนามธรรมและได้รับการสนับสนุนในส่วนติดต่อผู้ใช้ในลักษณะเฉพาะของตัวแทนผู้ใช้|
|กิจกรรม|กิจกรรมเป็นเหมือนกลุ่มของการ์ดที่เกี่ยวข้องซึ่งทำหน้าที่ทางตรรกะอย่างหนึ่ง สิ่งเหล่านี้อาจครอบคลุมตั้งแต่หนึ่งสำรับขึ้นไป โมเดลการนำทางและสถานะของ HDML มีโครงสร้างตามกิจกรรม|
|การนำทางตามประวัติ|ตัวแทนผู้ใช้จะรักษาประวัติของการ์ดที่แสดงต่อผู้ใช้ การ์ดแต่ละใบที่เข้าถึงได้จะถูกเพิ่มลงในประวัติการ์ด ตัวแทนผู้ใช้ช่วยให้ผู้ใช้สามารถย้อนกลับไปยังการ์ดก่อนหน้าในประวัติได้อย่างง่ายดาย|

## อ้างอิง

* [HDML - Wikipedia](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)
* [ข้อกำหนดของ HDML - โรงเรียน W3](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)

