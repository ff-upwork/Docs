{
  "date" : "2019-10-11",
  "keywords" :[ "jhtml","ไฟล์ jhtml", "รูปแบบไฟล์ jhtml", "ประเภทไฟล์ jhtml", "ไฟล์", "ประเภท", "ไฟล์ jhtml คืออะไร" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JHTML - ไฟล์ Java HTML",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ JHTML และ API ที่สามารถสร้างและเปิดไฟล์ JHTML",
  "linktitle" : "JHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-09"
}

## ไฟล์ JHTML คืออะไร?

ไฟล์ที่มีนามสกุล .jhtml คือไฟล์ [HTML](/th/web/html/) ที่มีรหัส [Java](/th/programming/java/) ซึ่งทำงานบนเซิร์ฟเวอร์เมื่อไคลเอนต์ร้องขอหน้านี้ในเบราว์เซอร์ เซิร์ฟเวอร์ประมวลผลคำขอ เรียกใช้ฟังก์ชัน Java ที่มีอยู่ในฟังก์ชัน และส่งเพจกลับไปยังเบราว์เซอร์ของไคลเอ็นต์ ออบเจกต์ Java ที่ฝังอยู่ในเพจ JHTML ทำงานบนเซิร์ฟเวอร์เพื่อจัดการคำขอสำหรับเพจประเภทนี้ ไฟล์ JHTML ยังสามารถเข้าถึงข้อมูลจากฐานข้อมูลโดยใช้การเชื่อมต่อ JDBC (Java [Database](/th/database/) Connectivity) ไฟล์ JHTML สามารถเปิดได้ในโปรแกรมแก้ไขข้อความและดูในเว็บเบราว์เซอร์ เช่น Google Chrome, Firefox และ Safari

## รูปแบบไฟล์ JHTML

JHTML เป็นเทคโนโลยีที่เป็นกรรมสิทธิ์ของ ATG และอาจสร้างขึ้นโดยใช้ ATG (Art Technology Group) Dynamo Document Editor ไฟล์ JHTML เขียนในรูปแบบไฟล์ข้อความล้วนโดยใช้โค้ด HTML และ Java มาตรฐาน แท็กเหล่านี้มีแท็ก HTML มาตรฐานนอกเหนือจากแท็กที่เป็นกรรมสิทธิ์ซึ่งอ้างอิงอ็อบเจ็กต์ Java เมื่อผู้ใช้ร้องขอเพจดังกล่าว เซิร์ฟเวอร์ HTTP จะส่งต่อคำขอไปยังแอปพลิเคชันเซิร์ฟเวอร์ Java เพจ JHTML จะถูกแปลงเป็นไฟล์ .java ก่อน และคอมไพล์เพื่อสร้างไฟล์ [.class](/th/programming/class/) ที่ดำเนินการเป็นเซิร์ฟเล็ต สิ่งนี้สร้างกระแสของข้อมูล HTTP และ HTML มาตรฐานที่ส่งคืนกลับไปยังเบราว์เซอร์ที่ร้องขอเพื่อแสดงต่อผู้ใช้ สิ่งนี้มีประโยชน์ในการเรียกใช้แบบสอบถามที่เกี่ยวข้องกับฐานข้อมูลบนเซิร์ฟเวอร์และส่งคืนผลลัพธ์สะสมที่สรุปแล้วไปยังเบราว์เซอร์ของไคลเอ็นต์

## อ้างอิง

* [โครงสร้างส่วนกลางของเอกสาร HTML](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)
