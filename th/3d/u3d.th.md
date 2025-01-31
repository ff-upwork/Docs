{
  "date" : "2019-10-11",
  "keywords" :[ "ไฟล์ u3d", "รูปแบบไฟล์ u3d", "ไฟล์ u3d คืออะไร", "ไฟล์", "ตัวอย่าง u3d", "นามสกุลไฟล์ u3d","นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"U3D - รูปแบบไฟล์ Universal 3D",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ U3D และ API ที่สามารถเปิดและสร้างไฟล์ U3D",
  "linktitle" : "U3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ U3D คืออะไร??

**U3D** (Universal 3D) เป็นรูปแบบไฟล์บีบอัดและโครงสร้างข้อมูลสำหรับคอมพิวเตอร์กราฟิก 3 มิติ ประกอบด้วยข้อมูลโมเดล 3 มิติ เช่น ตาข่ายสามเหลี่ยม แสง เงา ข้อมูลการเคลื่อนไหว เส้นและจุดที่มีสีและโครงสร้าง รูปแบบนี้ได้รับการยอมรับเป็นมาตรฐาน [ ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) ในเดือนสิงหาคม 2548 เอกสาร 3D [PDF](/th/pdf/) รองรับ U3D ฝังวัตถุและสามารถดูได้ใน Adobe Reader (เวอร์ชัน 7 เป็นต้นไป)

รูปแบบ U3D ได้รับการพัฒนาโดยคำนึงถึงเป้าหมายในการสร้างมาตรฐานสากลสำหรับการจัดเก็บและแลกเปลี่ยนข้อมูลสามมิติ อย่างไรก็ตาม รูปแบบนี้พบการใช้งานหลักในการเข้ารหัสสำหรับ 3D PDF แทนที่จะใช้เป็นรูปแบบการแลกเปลี่ยน Acrobat 3D แปลงประเภทไฟล์ 3D ที่รองรับเป็น U3D หรือ PRC เมื่อแปลงเป็น PDF

## รูปแบบไฟล์ U3D

ไฟล์ U3D อยู่ในรูปแบบไฟล์ไบนารีที่มีสี่ฉบับตามที่อธิบายไว้ในเอกสารอ้างอิง [ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) ส่งผลให้มีการอัปเดตข้อมูลจำเพาะ ในแต่ละฉบับด้วย ไฟล์ PDF มาตรฐาน ISO-32000 ยอมรับ U3D เป็นประเภทคำอธิบายประกอบและมัลติมีเดียที่อนุญาต

U3D รุ่นแรกมุ่งเน้นไปที่การนำเสนอคุณสมบัติหลักของกราฟิก 3 มิติ เช่น รูปทรงเรขาคณิต สี พื้นผิว แสง กระดูก และแอนิเมชันแบบแปลงร่าง รุ่นที่สองและสามแก้ไขข้อผิดพลาดบางอย่างในรุ่นแรก โดยรุ่นที่สามเป็นประเภทที่ใช้บ่อยที่สุดในซอฟต์แวร์อุตสาหกรรม การพิมพ์ครั้งที่สี่ให้คำจำกัดความสำหรับวัสดุดั้งเดิมที่มีลำดับสูงกว่า (พื้นผิวโค้ง) [ข้อกำหนด U3D](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) พร้อมใช้งานทางออนไลน์สำหรับการอ้างอิงของผู้ใช้บนเว็บไซต์ ECMA

### ประเภทข้อมูลในไฟล์ U3D

ไฟล์ไบนารีจะมีประเภทต่อไปนี้: U8, U16, U32, U64, I16, I32, F32, F64 และสตริง

* U8 : จำนวนเต็ม 8 บิตที่ไม่ได้ลงนาม
* U16 : จำนวนเต็ม 16 บิตที่ไม่ได้ลงชื่อ
* U32 : จำนวนเต็ม 32 บิตที่ไม่ได้ลงนาม
* U64 : จำนวนเต็ม 64 บิตที่ไม่ได้ลงนาม
* I16 : จำนวนเต็ม 16 บิตที่มีลายเซ็น
* F32: โฟลตความแม่นยำเดี่ยว IEEE
* F64: ลูกลอยที่มีความแม่นยำสองเท่าของ IEEE
* สตริง: สตริงในไฟล์ U3D เริ่มต้นด้วยจำนวนเต็ม 16 บิตที่ไม่ได้ลงชื่อซึ่งกำหนดความยาวทั้งหมดของอักขระในสตริง สตริงจะถูกประมวลผลโดยคำนึงถึงขนาดตัวพิมพ์เสมอ

## โครงสร้างไฟล์ U3D

ไฟล์ U3D มีลำดับของบล็อก มีบล็อก 3 ประเภทที่แตกต่างกันในแต่ละไฟล์ U3D

* บล็อกส่วนหัวของไฟล์
* ประกาศบล็อก
* บล็อกต่อเนื่อง

ตัวโหลดจะกำหนดจุดสิ้นสุดของบล็อกหากไม่ต้องการข้อมูลในบล็อกนั้น หรือหากไม่มีตัวถอดรหัสสำหรับประเภทบล็อกนั้น

{{< figure src="../u3d.png" alt="รูปแบบไฟล์ U3D" >}}

### บล็อกส่วนหัวของไฟล์
บล็อกส่วนหัวของไฟล์มีข้อมูลไฟล์ที่ใช้โดยโหลดเพื่อกำหนดวิธีการอ่านไฟล์

### บล็อกการประกาศ

บล็อกการประกาศประกอบด้วยข้อมูลเกี่ยวกับวัตถุในไฟล์ ต้องกำหนดวัตถุในบล็อกการประกาศ

### บล็อกต่อเนื่อง

ข้อมูลเพิ่มเติมสำหรับออบเจกต์ที่ประกาศในบล็อกการประกาศมีอยู่ในบล็อกความต่อเนื่อง Continuation Block แต่ละอันต้องเชื่อมโยงกับ Declaration Block


## อ้างอิง ##

* [รูปแบบไฟล์ U3D - Wikipedia](https://en.wikipedia.org/wiki/Universal_3D)
* [ข้อกำหนดรูปแบบไฟล์ ECMA U3D](https://www.ecma-international.org/publications/standards/Ecma-363.htm)

