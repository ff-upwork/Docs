{
  "date" : "2019-10-11",
  "keywords" :[ "asp","ไฟล์ asp", "รูปแบบไฟล์ asp", "ประเภทไฟล์ asp", "ไฟล์", "ประเภท", "ไฟล์ asp คืออะไร" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASP - รูปแบบไฟล์เพจเซิร์ฟเวอร์ที่ใช้งานอยู่",
  "description" :"เรียนรู้เกี่ยวกับไฟล์ ASP และ API ที่สามารถสร้างและเปิดได้",
  "linktitle" : "ASP",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ ASP คืออะไร??

ASP ย่อมาจาก Active Server Pages ซึ่งเป็นกรอบการพัฒนาสำหรับการสร้างเว็บเพจ ช่วยให้รหัสคอมพิวเตอร์สามารถดำเนินการโดยเซิร์ฟเวอร์ภายในเพื่อตอบสนองคำขอเว็บ เมื่อเว็บเบราว์เซอร์สร้างคำขอสำหรับไฟล์ ASP เซิร์ฟเวอร์จะอ่านไฟล์และเรียกใช้โค้ด/สคริปต์ใดๆ ที่อยู่ภายในเพื่อสร้างผลลัพธ์ **[HTML](/th/web/html/)** ซึ่งส่งคืนไปยัง เบราว์เซอร์สำหรับแสดงผล

ซึ่งแตกต่างจากเพจ HTML ซึ่งเป็นเพจแบบสแตติกที่ให้บริการโดยเซิร์ฟเวอร์ ไฟล์ ASP สร้างเนื้อหาแบบไดนามิกที่รันไทม์ซึ่งอาจเกี่ยวข้องกับการร้องขอข้อมูลจากฐานข้อมูล โดยทั่วไป หน้า ASP จะใช้นามสกุล .asp แทน .html เนื่องจากโค้ด/สคริปต์ภายในไฟล์ ASP ถูกดำเนินการที่ฝั่งเซิร์ฟเวอร์ เบราว์เซอร์ที่ร้องขอจึงไม่สามารถเห็นโค้ดที่ใช้สร้างเพจที่ให้บริการได้ เบราว์เซอร์สมัยใหม่ทั้งหมดสามารถแสดงหน้าที่สร้างขึ้นตามผลลัพธ์ได้ สร้างขึ้นจากเทคโนโลยีของ Microsoft เพจที่สร้างด้วย ASP จะโฮสต์บนเซิร์ฟเวอร์ Microsoft Internet Information Services (IIS)

## ประวัติโดยย่อของรูปแบบไฟล์ ASP
ASP ได้ผ่านการแก้ไขเพียงไม่กี่ครั้งจนกระทั่งถูกแทนที่ด้วย ASP.NET ซึ่งเป็นวิธีการที่ทันสมัยและมีประสิทธิภาพมากขึ้นในการพัฒนาและจัดการเพจฝั่งเซิร์ฟเวอร์ การสนับสนุน ASP จะรวมอยู่ในค่าเริ่มต้นพร้อมกับ Internet Information Services (IIS) ASP ได้รับการเผยแพร่ในสามเวอร์ชันที่แตกต่างกันโดยมีการปรับปรุงในแต่ละเวอร์ชัน

* ASP 1.0 เปิดตัวเมื่อเดือนธันวาคม 2539 โดยเป็นส่วนหนึ่งของ IIS 3.0
* ASP 2.0 เปิดตัวในเดือนกันยายน 2540 โดยเป็นส่วนหนึ่งของ IIS 4.0
* ASP 3.0 เปิดตัวในเดือนพฤศจิกายน 2543 โดยเป็นส่วนหนึ่งของ IIS 5.0

## ออบเจกต์การทำงานของ ASP

ไฟล์ ASP ใช้วัตถุฝั่งเซิร์ฟเวอร์เพื่อประมวลผลคำขอของผู้ใช้ และสร้างหน้าเอาต์พุตที่จะให้บริการแก่ผู้ใช้ แต่ละออบเจกต์มีชุดของคอลเลกชัน คุณสมบัติ และวิธีการสำหรับการประมวลผลคำขอและการตอบกลับ วัตถุเหล่านี้รวมถึง:

### ขอวัตถุ

เมื่อเบราว์เซอร์ขอหน้าเว็บจากเซิร์ฟเวอร์ จะเรียกว่าคำขอ วัตถุร้องขอใช้เพื่อรับข้อมูลจากผู้เยี่ยมชม

### วัตถุตอบสนอง

วัตถุตอบสนอง ASP ถูกใช้เพื่อส่งออกไปยังผู้ใช้จากเซิร์ฟเวอร์

### วัตถุเซิร์ฟเวอร์

วัตถุ ASP Server ใช้เพื่อเข้าถึงคุณสมบัติและวิธีการบนเซิร์ฟเวอร์ อนุญาตการเชื่อมต่อกับฐานข้อมูล (ADO) ระบบไฟล์ และการใช้ส่วนประกอบที่ติดตั้งบนเซิร์ฟเวอร์

### วัตถุเซสชัน

วัตถุเซสชั่นเป็นเหมือนลิงค์ระหว่างเบราว์เซอร์ของผู้ใช้ที่ร้องขอเพจจากเซิร์ฟเวอร์และเซิร์ฟเวอร์เอง สิ่งนี้ทำได้โดยคุกกี้ที่สร้างโดย ASP และส่งไปยังคอมพิวเตอร์ของผู้ใช้ วัตถุเซสชันเก็บข้อมูลเกี่ยวกับหรือเปลี่ยนการตั้งค่าสำหรับเซสชันผู้ใช้ ข้อมูลถูกเก็บไว้ใน Session object ที่ใช้ร่วมกันในทุกหน้าของแอปพลิเคชัน ข้อมูลทั่วไปที่จัดเก็บในตัวแปรเซสชัน ได้แก่ ชื่อ รหัส และค่ากำหนด เซิร์ฟเวอร์สร้างวัตถุเซสชันใหม่สำหรับผู้ใช้ใหม่แต่ละคน และทำลายวัตถุเซสชันเมื่อเซสชันหมดอายุ

### วัตถุแอปพลิเคชัน

วัตถุแอปพลิเคชันเก็บข้อมูลที่จะใช้โดยหลาย ๆ หน้าในแอปพลิเคชัน (เช่น ข้อมูลการเชื่อมต่อฐานข้อมูล) ข้อมูลสามารถเข้าถึงได้จากหน้าใดก็ได้ ข้อมูลยังสามารถเปลี่ยนแปลงได้ในที่เดียว และการเปลี่ยนแปลงจะมีผลโดยอัตโนมัติในทุกหน้า Application object ใช้เพื่อจัดเก็บและเข้าถึงตัวแปรจากหน้าใดๆ เช่นเดียวกับ Session object

### วัตถุ ASPERrror

วัตถุ ASPError ถูกนำมาใช้ใน ASP 3.0 และพร้อมใช้งานใน IIS5 และใหม่กว่าวัตถุ ASPError ใช้เพื่อแสดงข้อมูลรายละเอียดของข้อผิดพลาดที่เกิดขึ้นในสคริปต์ในหน้า ASP

**หมายเหตุ:** วัตถุ ASPError ถูกสร้างขึ้นเมื่อเรียก Server.GetLastError ดังนั้นข้อมูลข้อผิดพลาดสามารถเข้าถึงได้โดยใช้เมธอด Server.GetLastError เท่านั้น

## อ้างอิง

* [ASP - โดย W3C](https://www.w3schools.com/asp/default.asp)
* [การสร้างหน้า ASP อย่างง่าย](https://docs.microsoft.com/en-us/previous-versions/iis/6.0-sdk/ms524741(v=vs.90))
