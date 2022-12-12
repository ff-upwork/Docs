{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ CR2 - ไฟล์ภาพ Canon Raw 2",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ CR2 และ API ที่สามารถสร้างและเปิดไฟล์ CR2",
  "linktitle" : "CR2",
  "menu" : {
    "docs" : {
      "identifier":"image-cr2",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## ไฟล์ CR2 คืออะไร??

ไฟล์ CR2 (Camera RAW 2) เป็นไฟล์ภาพ RAW ที่สร้างโดยกล้องดิจิตอล Canon โดยจะเก็บข้อมูลภาพต้นฉบับแบบไม่สูญเสียการประมวลผลที่กล้องถ่ายไว้ รูปแบบไฟล์ CR2 ได้รับการพัฒนาโดย Canon สำหรับกล้องดิจิทัลและสามารถบันทึกภาพคุณภาพสูงได้ถึง 14 บิตของ RGB สิ่งนี้สร้างภาพคุณภาพสูงพร้อมพื้นที่เพียงพอสำหรับการประมวลผลภายหลัง Canon ใช้รูปแบบภาพ CR2 ในกล้องรุ่น 350D, 20D และ 1D ไฟล์ CR2 เป็นไฟล์ RAW และมีข้อมูลเมตาเพิ่มเติม เช่น ข้อมูลกล้อง ข้อมูลเลนส์ ข้อมูลการถ่ายคร่อม สมดุลแสงขาว และการตั้งค่าอื่นๆ

## รูปแบบไฟล์ CR2

ไฟล์ CR2 จะถูกจัดเก็บไว้ในการ์ดหน่วยความจำของกล้องเป็นไฟล์ไบนารีในรูปแบบไฟล์ที่เป็นกรรมสิทธิ์ของ Canon รูปแบบไฟล์ CR2 แทนที่รูปแบบไฟล์ CRW ที่ใช้ในตอนแรก และถูกแทนที่ด้วยรูปแบบไฟล์ Canon RAW 3 ในภายหลัง รูปแบบไฟล์ CR2 เป็นไปตามข้อกำหนดเฉพาะของ [TIFF](/th/image/tiff/) ซึ่งมี Image File Directories (IFD) 4 รายการ

|ออฟเซ็ต |เนื้อหา |ความคิดเห็น|
---|---|---|
|0x0000 |ส่วนหัว |ประกอบด้วยการจัดลำดับไบต์ เวอร์ชัน และออฟเซ็ตของรูปภาพ RAW|
|คำนวณ |IFD#0 |ส่วนนี้ประกอบด้วยส่วน Exif ซึ่งมีส่วน Makernotes
ข้อมูลเกี่ยวกับภาพ#0|
|คำนวณ |รูปภาพ#0 |รูปภาพเวอร์ชันเล็ก (ขนาดหนึ่งในสี่ของต้นฉบับ) บีบอัดเป็น Jpeg|
|คำนวณ |IFD#1 |ข้อมูลเกี่ยวกับรูปภาพ#1|
|คำนวณ |รูปภาพ#1 |รูปภาพเวอร์ชันเล็ก บีบอัดเป็น Jpeg|
|คำนวณ |IFD#2 |ข้อมูลเกี่ยวกับรูปภาพ#2|
|คำนวณ |รูปภาพ#2 |รูปภาพเวอร์ชันเล็ก ไม่บีบอัด|
|ในส่วนหัว| ไอเอฟดี#3| ข้อมูลเกี่ยวกับภาพ#3, ภาพ RAW ขนาดเต็ม|
|คำนวณ |รูปภาพ#3 |ข้อมูลภาพ RAW บีบอัดโดยไม่สูญเสียข้อมูลในรูปแบบไฟล์ Jpeg (ไม่ใช่ข้อมูล RGB!)|

## ข้อได้เปรียบของรูปแบบไฟล์ CR2

การจัดเก็บรูปภาพในรูปแบบ RAW ช่วยให้สามารถปรับแต่งภาพภายหลังได้มากมาย เช่น การปรับค่าสมดุลแสงขาว ซึ่งทำได้ยากกว่ามากและสูญเสียคุณภาพอย่างมากเมื่อใช้รูปแบบไฟล์ภาพอื่นๆ เช่น [JPEG](/th/image/jpeg/)

## CR2 ดีกว่า JPEG หรือไม่

ไฟล์ CR2 เป็นไฟล์ดิบโดยไม่สูญเสียข้อมูล ดังนั้นจึงไม่มีการสูญเสียคุณภาพ JPEG เป็นรูปแบบไฟล์ภาพที่สูญหายเนื่องจากสูญเสียข้อมูลบางส่วนเพื่อลดขนาดไฟล์ ดังนั้น ไฟล์ CR2 จึงมีคุณภาพสูงและเหมาะสำหรับการรีทัชและปรับปรุง

## อ้างอิง

* [รูปแบบไฟล์ CR2](http://lclevy.free.fr/cr2/)
