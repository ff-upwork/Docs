{
  "date" : "2021-06-09",
  "keywords" :[ "cda", "ไฟล์", "นามสกุล", "รูปแบบ", "ไฟล์ cda คืออะไร", "เพลง", "รูปแบบไฟล์ cda", "ข้อกำหนดรูปแบบไฟล์ cda"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"เรียนรู้เกี่ยวกับรูปแบบไฟล์ CDA และ API ที่สามารถสร้าง แปลง และเปิดไฟล์ CDA",
  "title" :"CDA - ไฟล์ทางลัดแทร็กเสียงซีดี",
  "linktitle" : "CDA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## ไฟล์ CDA คืออะไร??

ไฟล์ที่มีนามสกุล .cda เป็นไฟล์สตับขนาดเล็กที่สร้างโดย Microsoft Windows สำหรับแต่ละแทร็กเสียงในซีดีเพลง ไฟล์เหล่านี้ประกอบด้วยข้อมูลทั่วไป เช่น เวลาของแทร็กและทางลัดของ Windows ที่ช่วยให้ผู้ใช้สามารถเข้าถึงแทร็กเสียงเฉพาะได้ ไฟล์ CDA ไม่ใช่เพลง แต่ชี้ไปที่ไฟล์เพลงที่มีอยู่ในที่เก็บข้อมูล เราสามารถพูดได้ว่าเป็นทางลัดของไฟล์เสียงที่อยู่ในแผ่นซีดี

## รูปแบบไฟล์ CDA

รูปแบบไฟล์ CDA ใช้เพื่อบอกคอมพิวเตอร์ว่าจะเล่นไฟล์เสียงใดในซีดี ดังนั้นไฟล์ CDA จึงไร้ประโยชน์โดยแยกออกจากซีดีที่เป็นตัวแทน ไฟล์ CDA โดยทั่วไปถือว่าเป็นทรัพยากร RIFF มีเพียงอันเดียวที่ชื่อ "CDDA" และมีเพียงบล็อกข้อมูลเดียวชื่อ "FMT" ในไฟล์ .cda เวอร์ชันปัจจุบัน บล็อกนี้มีความยาว 24 ไบต์ ตัวระบุที่สร้างโดย Windows นั้นใช้โดยไดรฟ์ซีดีที่เกี่ยวข้องกับ Windows 95 และ Windows 98 และเครื่องเล่นไม่สามารถเชื่อมต่อกับ FreeDB หรือ CDDB เพื่อให้สามารถแสดงชื่อเพลงและชื่อศิลปินได้ ซึ่งคุณต้องป้อนข้อมูลนี้ด้วยตนเองในไฟล์ cdplayer.ini

### การจัดระเบียบไฟล์ CDA

ตารางต่อไปนี้แสดงข้อมูลเกี่ยวกับการชดเชยทั่วไป:
| ชดเชย | ความยาว | เนื้อหา |
---|---|---|
| 0x00 | 4 | อักขระ ASCII 4 ตัว "RIFF" |
| 0x04 | 4 | ขนาดของอันต่อไปนี้: เสมอ 36 (44 - 8), บน 4 ไบต์ (คำสั่งของ Intel) |
| 0x08 | 4 | ตัวระบุกลุ่ม: อักขระ ASCII 4 ตัว "CDDA" |
| 0x0C | 4 | อักขระ ASCII 3 ตัว "fmt" ตามด้วยช่องว่าง |
| 0x10 | 4 | ความยาวของก้อน: เสมอ 24 บน 4 ไบต์ (คำสั่งของ Intel) |
| 0x14 | 2 | เวอร์ชันของรูปแบบซีดี 2 ไบต์ (คำสั่งของ Intel) ในเดือนพฤษภาคม 2549 เท่ากับ 1 เสมอ |
| 0x016 | 2 | จำนวนช่วง 2 ไบต์ (คำสั่งของ Intel) แทร็กแรกมีหมายเลข 1 |
| 0x18 | 4 | ตัวระบุที่คำนวณโดย Windows สำหรับ cdplayer.exe |
| 0x1c | 4 | ช่วงออฟเซ็ต จำนวนเฟรม (คำสั่งของ Intel) |
| 0x20 | 4 | ระยะเวลาของแทร็ก จำนวนเฟรมทั้งหมด (คำสั่งของ Intel) |
| 0x24 | 1 | ตำแหน่งช่วง: เฟรม |
| 0x25 | 1 | ตำแหน่งช่วง: วินาที |
| 0x26 | 1 | ตำแหน่งช่วง: นาที |
| 0x27 | 1 | ไบต์ว่าง (ค่าไบนารี 0) |
| 0x28 | 1 | ระยะเวลาของแทร็ก: เฟรม |
| 0x29 | 1 | ระยะเวลาของแทร็ก: วินาที |
| 0x2a | 1 | ระยะเวลาของแทร็ก: นาที |
| 0x2b | 1 | ไบต์ว่าง (ค่าไบนารี 0) |

## อ้างอิง

* [ไฟล์ .cda - โดย Wikipedia](https://en.wikipedia.org/wiki/.cda_file)

