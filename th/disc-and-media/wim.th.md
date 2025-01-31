{
  "date" : "2021-08-11",
  "keywords" :[ "ไฟล์ wim", "รูปแบบไฟล์ wim", "ไฟล์ wim คืออะไร", "ไฟล์", "ตัวอย่าง wim", "นามสกุลไฟล์ wim","นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"เรียนรู้เกี่ยวกับรูปแบบไฟล์ WIM และ API ที่สามารถสร้างและเปิดไฟล์ WIM",
  "title" :"WIM - ไฟล์รูปแบบการถ่ายภาพของ Windows",
  "linktitle" : "WIM",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## ไฟล์ WIM คืออะไร??
ไฟล์ที่มีนามสกุล .wim ถูกพบเป็นครั้งแรกใน Windows Vista WIM เป็นของรูปแบบภาพตามไฟล์ซึ่งโดยทั่วไปจะนำมาใช้ใน Microsoft Windows Vista ช่วยให้อิมเมจดิสก์เดียวถูกนำไปใช้กับแพลตฟอร์มคอมพิวเตอร์ต่างๆ ไฟล์ WIM ใช้ในการจัดการไฟล์ต่างๆ เช่น การอัปเดต ไดรเวอร์ และส่วนประกอบต่างๆ โดยไม่ต้องบูตอิมเมจระบบปฏิบัติการใหม่ ไฟล์ AQ WIM มีชุดของไฟล์และข้อมูลเมตาที่เกี่ยวข้องซึ่งคล้ายกับรูปแบบไฟล์ดิสก์อื่นๆ

## รูปแบบไฟล์ WIM
รูปแบบไฟล์ WIM ไม่เหมือนกับรูปแบบตามเซกเตอร์ เช่น VHD หรือ IS อันที่จริงแล้วเป็นรูปแบบไฟล์ ซึ่งหมายความว่าหน่วยพื้นฐานของข้อมูลใน WIM คือไฟล์ ประโยชน์พื้นฐานของการใช้ไฟล์คือที่จัดเก็บอินสแตนซ์เดียวของไฟล์ที่อ้างอิงหลายครั้งในโครงสร้างระบบไฟล์และเป็นอิสระจากฮาร์ดแวร์ ซึ่งช่วยลดค่าใช้จ่ายในการเปิดและปิดไฟล์ต่างๆ ทีละไฟล์ เนื่องจากไฟล์ถูกจัดเก็บไว้ใน WIM เดียว ไฟล์. ไฟล์ WIM สามารถจัดเก็บดิสก์อิมเมจได้หลายไฟล์ ซึ่งถูกอ้างอิงด้วยชื่อเฉพาะหรือดัชนีตัวเลข
### รองรับอัลกอริธึมการบีบอัด
WIM รองรับตระกูลอัลกอริธึมการบีบอัดต่อไปนี้ในความเร็วจากมากไปน้อยและอัตราส่วนจากน้อยไปหามาก:
- เอ็กซ์เพรส
- LZX
- LZMS
- อัดแข็ง.
สามตระกูลแรกใช้ LZ77 ในขณะที่ Solid-compression ถูกนำมาใช้พร้อมกับ LZMS ใน WIMGAPI Windows 8 และ DISM Windows 8.1
### เครื่องมือสำหรับรูปแบบไฟล์ WIM
เครื่องมือต่อไปนี้มักจะรองรับรูปแบบไฟล์ WIM:

- **ImageX**: เครื่องมือบรรทัดคำสั่งที่ใช้ในการแก้ไข สร้าง และปรับใช้ดิสก์อิมเมจของ Windows ในรูปแบบ Windows Imaging พร้อมกับ WIMGAPI ที่เกี่ยวข้อง มีการแจกจ่ายโดยเป็นส่วนหนึ่งของชุดติดตั้ง Windows Automated ฟรี เริ่มต้นด้วย Windows Vista โปรแกรมติดตั้ง Windows ใช้ WAIK API เพื่อติดตั้ง Windows
- **DISM**: เครื่องมือที่นำมาใช้ใน Windows 7 และ Windows Server 2008 R2 ที่สามารถทำงานเกี่ยวกับบริการบนอิมเมจการติดตั้ง Windows ไม่ว่าจะเป็นอิมเมจออนไลน์หรืออิมเมจออฟไลน์ภายในโฟลเดอร์หรือไฟล์ WIM เครื่องมือนี้มีความสามารถในการเมานต์และยกเลิกการต่อเชื่อมอิมเมจ เพิ่มไดรเวอร์อุปกรณ์ลงในอิมเมจออฟไลน์ และสอบถามไดรเวอร์อุปกรณ์ที่ติดตั้งในอิมเมจออฟไลน์
 




## อ้างอิง


* [รูปแบบการถ่ายภาพของ Windows - โดย Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


