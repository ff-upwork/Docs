{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDB", "นามสกุล", "ไฟล์", "รูปแบบไฟล์", "ประเภทไฟล์ฐานข้อมูล", "รูปแบบไฟล์ฐานข้อมูล", "ไฟล์ฐานข้อมูล" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"เรียนรู้เกี่ยวกับรูปแบบไฟล์ ACCDB และ API ที่สามารถสร้างและเปิดไฟล์ ACCDB",
  "title" :"รูปแบบไฟล์ ACCDB - ไฟล์ฐานข้อมูล Microsoft Access 2007",
  "linktitle" : "ACCDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## ไฟล์ ACCDB คืออะไร??

ไฟล์ที่มีนามสกุล .accdb คือไฟล์ฐานข้อมูล Microsoft Access 2007 ที่เก็บข้อมูลผู้ใช้ไว้ในตาราง รองรับการจัดเก็บ
แบบฟอร์มที่กำหนดเอง แบบสอบถาม SQL และข้อมูลอื่นๆ ไฟล์ ACCDB แทนที่ไฟล์ [MDB](/th/database/mdb/) หลังจากที่ Microsoft เปลี่ยนไปใช้โครงสร้างไฟล์แบบ XML ไฟล์ ACCDB ยังสามารถแปลงเป็น MDB ด้วยความเข้ากันได้แบบเก่า อย่างไรก็ตาม ACCDB เป็นรูปแบบไฟล์ฐานข้อมูล Access ที่ใช้กันอย่างแพร่หลายในขณะนี้ นอกจากนี้ Microsoft ยังสนับสนุนคุณลักษณะเพิ่มเติมในรูปแบบ ACCDB เช่น ความเป็นไปได้ในการจัดเก็บไฟล์แนบ ข้อมูลไบนารี และการสนับสนุนฟิลด์แบบหลายค่า

## รูปแบบไฟล์ ACCDB

เช่นเดียวกับ MDB ไม่มีข้อมูลจำเพาะสาธารณะสำหรับรูปแบบไฟล์ ACCDB Microsoft สนับสนุนการเข้าถึงไฟล์เหล่านี้โดยทางโปรแกรมผ่านมาตรฐาน Open Database Connectivity (ODBC) และ Visual Basic for Applications (VBA)

### ข้อมูลเชิงลึก

การถ่ายโอนข้อมูลฐานสิบหกของไฟล์ ACCDB อย่างง่ายแสดงให้เห็นว่ามีความคล้ายคลึงกันทั่วไปในโครงสร้างกับรุ่นล่าสุดของตระกูลรูปแบบ MDB รุ่นก่อนหน้า ไฟล์ทั้งสองรูปแบบใช้ขนาดหน้าคงที่ 4096 ไบต์ ความคล้ายคลึงกันอีกอย่างระหว่าง ACCDB และ MDB คือรูปแบบของหมายเลขวิเศษ ซึ่งรวมถึงสตริง "Standard ACE DB" สำหรับ ACCDB รหัสเวอร์ชันหรือความเข้ากันได้อยู่ในตำแหน่งเดียวกันในทั้งสองรูปแบบ mdbtools | ไฟล์ HACKING ระบุว่า "Offset 0x14 มีเวอร์ชัน Jet ของฐานข้อมูลนี้" และคู่มือ MDB อย่างไม่เป็นทางการเห็นพ้องต้องกัน ข้อมูลในแหล่งข้อมูลเหล่านี้ เมื่อรวมกับรายการ Wikipedia สำหรับ [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine) แสดงว่าค่า 0x02 หมายถึง ACE 12 (Access 2007) และ 0x03 หมายถึง ACE 14 (เข้าถึง 2010). อย่างไรก็ตาม ฐานข้อมูลขั้นต่ำที่สร้างขึ้นใน Access 2010 และฐานข้อมูลที่คล้ายกันซึ่งสร้างขึ้นใน Access 2016 ทั้งสองมี 0x02 ในตำแหน่งนี้ ฐานข้อมูลขั้นต่ำที่สร้างขึ้นใน Access 2016 แต่การกำหนดคอลัมน์ด้วยชนิดข้อมูล "จำนวนเต็มขนาดใหญ่" ที่แนะนำใหม่ มีค่าเป็น 0x05 ในไฟล์ ACCDB ตัวบ่งชี้นี้จะแสดงถึงความเข้ากันได้ของไฟล์ แทนที่จะเป็นเวอร์ชันของเอ็นจิ้น ACE ที่ใช้ในการสร้าง

## อ้างอิง

* [รูปแบบการเข้าถึงไฟล์](https://support.microsoft.com/en-us/office/ which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41?redirectSourcePath=% 252fen-us%252farticle%252fIntroduction to-the-Access-2007-file-format-8cf93630-0b68-4a40-a13c-7528b9f074b6&ui=en-US&rs=en-US&ad=US)
* [ข้อมูลจำเพาะของ Access 2016](https://support.microsoft.com/en-us/office/access- specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c?ui=en-us&rs=en-us&ad=us)
* [โปรแกรมฐานข้อมูล Microsoft Jet](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)
* [ฉันควรใช้รูปแบบไฟล์ Access ใด](https://support.microsoft.com/en-us/office/where-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41?ui=en-us&rs=en-us&ad=us)