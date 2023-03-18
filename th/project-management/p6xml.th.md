{
  "date" : "2021-04-16",
  "keywords" :[ "XML", "P6XML", "ไฟล์", "นามสกุล", "รูปแบบไฟล์", "โครงการ", "การจัดการ", "Primavera", "P6"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P6XML - โครงการ Primavera P6",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ P6XML และ API ที่สามารถสร้างและเปิดไฟล์ P6XML",
  "linktitle" : "P6XML",
  "menu" : {
    "docs" : {
      "parent" : "project-management"
}
},
  "lastmod" : "2021-05-07"
}

## ไฟล์ P6XML คืออะไร? ##

นามสกุลไฟล์ P6XML มีความสามารถในการอ่าน การปรับตัว และการใช้งานที่หลากหลายซึ่งทำให้เป็นรูปแบบในอุดมคติ Primavera P6 Professional มีฟังก์ชันในการส่งออกและนำเข้าทั้งไฟล์ [XER](/th/project-management/xer/) และไฟล์ XML XML ย่อมาจาก **Extensible Markup Language** รูปแบบทั่วไปนี้อนุญาตให้ผู้ใช้แบ่งปันข้อมูลโครงการระหว่างฐานข้อมูล Primavera P6 ข้อมูลโครงการสามารถจัดเก็บไว้ในไฟล์ข้อความผ่านไฟล์ XML ได้อย่างง่ายดาย สิ่งนี้ทำให้โปรแกรมซอฟต์แวร์จำนวนมากสามารถแลกเปลี่ยนข้อมูลได้ง่ายขึ้น ข้อมูลดังกล่าวสามารถแชร์และจัดการได้อย่างง่ายดายโดยผู้ใช้ Primavera P6

## ข้อดีของรูปแบบไฟล์ P6XML ##

* เป็นเรื่องง่ายสำหรับผู้ใช้ Primavera ในการกำหนด Baselines ที่จะส่งออกและนำเข้าโดยใช้ไฟล์ XML
* การส่งออก XML สามารถมีแผนปฏิบัติการโดยละเอียดของโครงการทั้งหมด
* ผู้ใช้ที่ใช้ Primavera 6 ซึ่งไม่สามารถแก้ไข เพิ่ม หรือลบรายการข้อมูลส่วนกลางบางรายการ เช่น รหัสกิจกรรม ปฏิทิน และทรัพยากร จะไม่สามารถนำเข้าข้อมูลเหล่านั้นได้
* นอกเหนือจากการตั้งค่า General และ Project Security Profile ที่ใช้โดย Primavera รายการข้อมูลที่จะส่งผลกระทบหรือเปลี่ยนแปลงข้อมูลในฐานข้อมูลจะไม่ถูกนำเข้า

## การส่งออกไฟล์ XML จาก Primavera P6 ##

สำหรับการส่งออกโปรเจ็กต์ P6 Professional และข้อมูลโปรเจ็กต์ไปยังไฟล์ P6XML ให้ใช้ Oracle Primavera Cloud คุณสามารถดาวน์โหลดไฟล์ได้เมื่อไฟล์ถูกสร้างขึ้นจากแอปพลิเคชันเดสก์ท็อป P6 Professional และนำเข้าไปยัง Primavera Cloud ก่อนดำเนินกระบวนการส่งออกอย่างต่อเนื่อง คุณควรควบคุมว่าคุณเชื่อมโยงกับฐานข้อมูล P6 Professional หรือ P6 EPPM หรือไม่ คุณลักษณะบางอย่างของกระบวนการส่งออกอาจแตกต่างกันไปตามฐานข้อมูลของคุณ การมีการตั้งค่า P6 Specialized กับฐานข้อมูล P6 Proficient กระบวนการส่งออกจะดำเนินการภายในระบบของคุณ การมีฐานข้อมูล P6 Professional คุณสามารถส่งออกและเปิดไฟล์ P6 XML จากการตั้งค่าในระบบของคุณได้อย่างง่ายดาย

ต่อไปนี้เป็นขั้นตอนบางส่วนที่อธิบายกระบวนการส่งออก:

* เปิดโครงการ Primavera P6
* หลังจากนั้น เลือกส่งออกบนแท็บไฟล์
* เลือก "Primavera P6 – (XML)" หลังจากนั้นคลิก ถัดไป
* ดับเบิลคลิกที่โครงการที่คุณจะส่งออก
* เลือกการตัดทอนสำหรับเส้นทางที่คุณต้องการวางไฟล์ที่ส่งออกแล้วเลือก "เสร็จสิ้น"
* เลือกตัวเลือกที่คุณต้องการบันทึกไฟล์อย่างไร
* หากไม่ต้องการเค้าโครงระดับโครงการกับไฟล์ส่งออก จำเป็นต้องล้างการเลือกเป็น "ส่งออกเค้าโครงระดับโครงการทั้งหมด"
* เลือกเสร็จสิ้น จากนั้นคุณจะได้รับการยืนยันการส่งออก XML

### เคล็ดลับสำคัญ ###

* เมื่อใดก็ตามที่เชื่อมต่อกับฐานข้อมูล P6 EPPM ผู้ดูแลระบบจะต้องส่ง URL ของแหล่งเนื้อหาไปยังฟิลด์ P6 URL ในหน้าทั่วไปของการตั้งค่าแอปพลิเคชันใน P6
* สะดวกในการส่งออกหลายโครงการเป็นไฟล์ XML ไฟล์เดียว
* ข้อมูลส่วนกลางที่จัดสรรให้กับโครงการจะถูกส่งออก
* สะดวกในการส่งออกไฟล์ XML โดยไม่ต้องขออนุญาตใช้ทรัพยากรทั้งหมด



## ปัญหาในการเปิดไฟล์ P6XML? ##

ปัญหาทั่วไปบางประการที่อาจเกิดขึ้นและทำให้รูปแบบ P6XML ทำงานผิดพลาดมีดังนี้:

* ไม่มีซอฟต์แวร์สนับสนุน
* ไฟล์เสียหาย
* ไฟล์ติดไวรัสเนื่องจากไวรัส
* คำอธิบาย P6XML ถูกลบออกจากรีจิสทรีของ Windows โดยไม่ได้ตั้งใจ
* ไม่มีสิทธิ์ในระบบในการเปิดไฟล์
* ไดรฟ์ที่ล้าสมัยในระบบของคุณ
* นามสกุลของไฟล์ถูกเปลี่ยนชื่อ


## อ้างอิง ##

* [Oracle - P6 XML](https://docs.oracle.com/cd/E80480_01/English/admin/p6_import_guide/index.html)