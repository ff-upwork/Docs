{
  "date" : "2021-14-04",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ AVCHD",
  "keywords" :[ "avchd", "ไฟล์", "นามสกุล", "รูปแบบ", "รูปแบบวิดีโอ", "ไฟล์ avchd คืออะไร", "วิธีเปิดไฟล์ AVCHD"],
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ AVCHD และ API ที่สามารถสร้างและแสดงวิธีการเปิดไฟล์ AVCHD",
  "linktitle" : "AVCHD",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-14-04"
}

## ไฟล์ AVCHD คืออะไร?? ##

ไฟล์ AVCHD เป็นรูปแบบไฟล์การบันทึกที่แนะนำสำหรับการบันทึกวิดีโอความละเอียดสูง (HD) ลงในดีวีดี ฮาร์ดดิสก์ไดรฟ์ และการ์ดหน่วยความจำ วิดีโอ AVCHD ที่บันทึกลง DVD และ Blu-ray สามารถเล่นได้อย่างง่ายดายบนเครื่องเล่น Blu-ray Disc ส่วนใหญ่ นอกจากนี้ยังสามารถบันทึกเนื้อหา AVCHD ลงในการ์ด SD และเล่นโดยเครื่องเล่น Blu-ray Disc โทรทัศน์ และคอนโซลมีเดียจำนวนมาก **การทดสอบ ffdshow** และ **Libavcodec** เป็นตัวแปลงสัญญาณแบบโอเพ่นซอร์สที่สามารถถอดรหัสไฟล์ AVCHD ได้


## รูปแบบไฟล์ AVCHD

รูปแบบไฟล์ AVCHD ช่วยให้กล้องวิดีโอดิจิตอลความละเอียดสูงบันทึกสัญญาณ HD; โดยใช้เทคโนโลยีการเข้ารหัสการบีบอัดที่มีประสิทธิภาพสูง ในการบีบอัดวิดีโอ มีการใช้รูปแบบ [MPEG-4](/th/video/mp4/) AVC/[H.264](/th/video/h264/) และใช้ Dolby Digital® เพื่อบีบอัดข้อมูลเสียง ในขณะที่รูปแบบ MPEG-4 AVC/H.264 มีประสิทธิภาพมากกว่ารูปแบบการบีบอัดภาพทั่วไป นอกจากนี้ รูปแบบวิดีโอ 3D (รูปแบบ MVC) และ 1080/60p (1080/50p) ได้ถูกเพิ่มเป็นส่วนขยายของรูปแบบไฟล์ AVCHD สำหรับรูปแบบเวอร์ชัน 2.0 (AVCHD 3D, AVCHD Progressive)
โปรดทราบว่าอุปกรณ์ต้องเข้ากันได้กับ AVCHD V. 2.0 เพื่อจัดการกับวิดีโอที่เกี่ยวข้องกับ AVCHD V. 2.0

## การเปรียบเทียบระหว่างรูปแบบไฟล์ AVCHD และ MP4 ##

รูปแบบไฟล์ Advanced Video Codec High Definition (AVCHD) เหมาะอย่างยิ่งสำหรับการสร้างการบันทึก Blu-ray Disc® และรับชม HDTV เมื่อเปรียบเทียบกันแล้ว MP4 นั้นเล่นบนอุปกรณ์พกพาได้ง่ายกว่ามาก และยังง่ายต่อการย้าย คัดลอก และบันทึกบนเว็บอีกด้วย

ความแตกต่างของทั้งสองรูปแบบแสดงไว้ในตารางด้านล่าง:

|ข้อมูลจำเพาะ |AVCHD|MP4|
|-----------------------|----|----|
| ขนาดภาพ (สัดส่วนภาพ) |1920 x 1080/60i, 50i (16:9) 1440 x 1080/60i, 50i (16:9)|1440 x 1080/30p (16:9) 1280 x 720/30p (16: 9) 640 x 480/30p (4:3)|
| ช่องสัญญาณเสียง / ความถี่ตัวอย่าง | 2 ช่อง/48 kHz 5.1 ช่อง/48 kHz|2 ช่อง/48 kHz.|
| นามสกุลไฟล์ |.M2TS|.MP4|
| ความเข้ากันได้ | เข้ากันได้กับรูปแบบ Blu-ray Disc | เข้ากันได้กับรูปแบบ Apple® QuickTime®|
| |เข้ากันได้กับอุปกรณ์สื่อบันทึกหลายชนิด เช่น ฮาร์ด|เข้ากันได้กับสื่อบันทึกและเครือข่ายต่างๆ รวมถึง PlayStation® Video โดย PlayStation Network|
| |เข้ากันได้กับเทคโนโลยี xv.Color|เข้ากันได้กับระบบปฏิบัติการ Windows 7 ขึ้นไปโดยกำเนิดรองรับ MP4|
| |เข้ากันได้กับระบบปฏิบัติการ Windows® 7 ขึ้นไป โดยรองรับ AVCHD||


## อ้างอิง ##

- [AVCHD - วิกิพีเดีย](https://en.wikipedia.org/wiki/AVCHD)
- [รูปแบบ AVCHD คืออะไร](https://www.sony.com/electronics/support/articles/00016537)


