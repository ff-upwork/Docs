{
  "date" : "2021-02-15",
  "keywords" :[ "ไฟล์ vp6", "รูปแบบไฟล์ vp6", "ไฟล์ vp6 คืออะไร", "ไฟล์", "ตัวอย่าง vp6", "นามสกุลไฟล์ vp6","นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP6 - ไฟล์วิดีโอ TrueMotion",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ VP6 และ API ที่สามารถสร้างและเปิดไฟล์ VP6",
  "linktitle" : "VP6",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## ไฟล์ VP6 คืออะไร??

VP6 เป็นรูปแบบวิดีโอที่มีการบีบอัดแบบสูญเสียข้อมูลซึ่งเปิดตัวโดยเทคโนโลยี On2 ในเดือนพฤษภาคม 2546 เป็นส่วนหนึ่งของชุดตัวแปลงสัญญาณวิดีโอที่พัฒนาโดย TrueMotion ซึ่งรวมถึง V3, V4 และ V5 รูปแบบนี้ใช้ไม่นานในด้านการกระจายเสียง เช่น กับรายงานของ BBC และซอฟต์แวร์ QuickLink VP6 ประสบความสำเร็จโดย VP7 Codec ในเดือนมกราคม 2548 โดยมีความเข้ากันได้ในการบีบอัดที่ดีขึ้น

## รูปแบบไฟล์ VP6

ข้อมูลจำเพาะที่สมบูรณ์สำหรับไฟล์ V6 ไม่เปิดเผยต่อสาธารณะ On2 เผยแพร่ข้อมูลจำเพาะต่อสาธารณะในตอนแรก แต่ในไม่ช้าข้อมูลจำเพาะเหล่านี้ก็ไม่พร้อมใช้งานสำหรับผู้ใช้ทั่วไป เอกสารประกอบอย่างไม่เป็นทางการของรูปแบบไฟล์ VP6 มีอยู่ที่ [multimedia wiki](https://wiki.multimedia.cx/index.php?title=On2_VP6) ที่สามารถอ้างอิงสำหรับการอ้างอิงของผู้พัฒนา

### มาโครบล็อก (MB)

เช่นเดียวกับ MPEG-2, MPEG-4 ส่วนที่ 2 และ 10 แต่ละเฟรมวิดีโอของไฟล์ VP6 ประกอบด้วยอาร์เรย์ของมาโครบล็อกขนาด 16x16 (MB) แต่ละ MB สามารถอยู่ในโหมดใดโหมดหนึ่งต่อไปนี้:

* ภายใน MB
* Inter MB, null MV, การอ้างอิงเฟรมก่อนหน้า
* Inter MB, MV ส่วนต่าง, การอ้างอิงเฟรมก่อนหน้า
* Inter MB, สี่ MV, การอ้างอิงเฟรมก่อนหน้า
* Inter MB, MV 1, การอ้างอิงเฟรมก่อนหน้า
* Inter MB, MV 2, การอ้างอิงเฟรมก่อนหน้า
* Inter MB, null MV, การอ้างอิงเฟรมที่คั่นหน้า
* Inter MB, MV ส่วนต่าง, การอ้างอิงเฟรมที่คั่นหน้า
* Inter MB, MV 1, การอ้างอิงเฟรมที่คั่นหน้า
* Inter MB, MV 2, การอ้างอิงเฟรมที่คั่นหน้า

### ส่วนหัวของเฟรม

ส่วนหัวของเฟรมของ VP6 แสดงไว้ด้านล่างซึ่งตามหลังการบรรจุบิตของ big-endian

|ไวยากรณ์|จำนวนบิต|ประเภท|Symantecs|
---|---|---|---|
|frame_mode|1|Enum|0x0 หมายถึงภายในเฟรม|
|qp |6 |Unsigned |Quantization พารามิเตอร์ช่วงที่ถูกต้อง 0..63|
|เครื่องหมาย| 1| ค่าคงที่| 0=VP61/62, 1=VP60|
|ถ้า (frame_mode == 0) { | 0 | |เท่ากับ INTRA_FRAME|
|เวอร์ชั่น |5| ค่าคงที่| 6=VP60/61, 7=VP60(อิเล็กทรอนิกส์ศิลป์), 8=VP62|
|เวอร์ชั่น 2 |2| ค่าคงที่ |0=VP60, 3=VP61/62|
|อินเตอร์เลซ |1| บูลีน | จริง (1) หมายถึงอินเตอร์เลซจะถูกใช้|
|if (marker==1 หรือ version2==0) {||||
|ออฟเซ็ต |16 |ไม่ได้ลงชื่อ| ออฟเซ็ตบัฟเฟอร์รอง (ไบต์สัมพันธ์กับจุดเริ่มต้นของบัฟเฟอร์)|
|}||||
|dim_y |8| ไม่ได้ลงชื่อ| ความสูงมาโครบล็อกของวิดีโอ|
|dim_x |8| ไม่ได้ลงชื่อ| ความกว้างมาโครบล็อกของวิดีโอ|
|render_y |8 |ไม่ได้ลงนาม |แสดงความสูงของวิดีโอ|
|render_x |8 |ไม่ได้ลงนาม |แสดงความกว้างของวิดีโอ|
|}อื่นๆ{||||
|if (marker==1 หรือ version2==0) {||||
|ออฟเซ็ต |16 |ไม่ได้ลงชื่อ |ออฟเซ็ตบัฟเฟอร์รอง (ไบต์สัมพันธ์กับจุดเริ่มต้นของบัฟเฟอร์)|
|}||||
|}||||

## อ้างอิง

* [วิกิพีเดีย VP6](https://en.wikipedia.org/wiki/VP6#:~:text=On2%20TrueMotion%20VP6%20is%20a,Video%2C%20and%20JavaFX%20media%20files.)

