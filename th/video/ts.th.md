{
  "date" : "2021-12-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ TS - ไฟล์สตรีมการขนส่งวิดีโอ",
  "keywords" :[ "ts", "บิน", "ส่วนขยาย", "ส่วนขยาย", ".ts", "รูปแบบ" ],
  "description":"เรียนรู้เกี่ยวกับไฟล์ TS และ API ที่สามารถสร้างและเปิดไฟล์ TS ได้",
  "linktitle" : "TS",
  "menu" : {
    "docs" : {
      "identifier":"video-ts",
      "parent" : "video"
}
},
  "lastmod" : "2021-12-16"
}

## ไฟล์ TS คืออะไร??

ไฟล์ที่มีนามสกุล .ts คือสตรีมวิดีโอที่เก็บข้อมูลไว้ในแผ่นดีวีดี ใช้อัลกอริธึมการบีบอัด MPEG-2 ([.mpeg](/th/video/mpg/)) เพื่อให้ได้ประสิทธิภาพสูงสุดและความเข้ากันได้ในสื่อประเภทต่างๆ เช่น การสตรีมอินเทอร์เน็ตและการแพร่ภาพ รูปแบบไฟล์ TS ถูกสร้างขึ้นเพื่อให้สามารถเล่นบนอุปกรณ์ที่มีการเชื่อมต่ออินเทอร์เน็ตที่ไม่ดี เช่น สมาร์ททีวี

## รูปแบบไฟล์ TS - ข้อมูลเพิ่มเติม

ข้อมูลในไฟล์ TS คล้ายกับไฟล์ [MP4](/th/video/mp4/) แต่จะแบ่งออกเป็นส่วนเล็กๆ แต่ละส่วนประกอบด้วยวิดีโอชิ้นเล็กๆ ตามด้วยเสียงเล็กน้อย และคำบรรยายเพิ่มเติม ไฟล์ TS ไฟล์เดียวประกอบด้วยชิ้นส่วนดังกล่าวจำนวนมาก นอกจากวิดีโอ เสียง และคำบรรยายแล้ว แต่ละกลุ่มยังประกอบด้วยข้อมูลเพิ่มเติมบางส่วนสำหรับตรวจหาข้อผิดพลาดในกลุ่ม ด้วยเหตุนี้ ไฟล์ TS จึงมีขนาดค่อนข้างใหญ่

### ทำไมต้องใช้รูปแบบไฟล์ TS

ดังนั้น หากไฟล์ TS มีขนาดค่อนข้างใหญ่ มีประโยชน์อย่างไรในการใช้แทนไฟล์รูปแบบอื่น ในการออกอากาศ วิดีโอและเสียงชิ้นเล็กๆ สามารถส่งผ่านสื่อสื่อสาร (แบบมีสายหรือวิทยุ) ได้แบบเรียลไทม์ ผู้รับจะใช้ข้อมูลเพิ่มเติมในส่วนข้อมูลเพื่อข้ามส่วนที่เกิดข้อผิดพลาดได้ง่าย

นอกจากนี้ยังใช้ไฟล์ TS เนื่องจากระบบการออกอากาศไม่ต้องการสตรีมทั้งหมดเพื่อเล่น สามารถรับการส่งสัญญาณและใช้งานได้แบบเรียลไทม์โดยการประกอบเสียงและวิดีโอเข้าด้วยกัน

## วิธีเล่นไฟล์ TS

ไฟล์ TS สามารถเปิดและเล่นได้ใน [เครื่องเล่นสื่อ VideoLAN VLC](https://www.videolan.org/vlc/features.html) ยอดนิยม ซึ่งดาวน์โหลดได้ฟรี

## อ้างอิง ##

* [สตรีมการขนส่ง MPEG - Wikipedia](https://en.wikipedia.org/wiki/MPEG_transport_stream)
