{
  "date" : "2019-10-11",
  "keywords" :[ "mht","ไฟล์ mht", "รูปแบบไฟล์ mht", "ประเภทไฟล์ mht", "ไฟล์", "ประเภท", "ไฟล์ mht คืออะไร" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ MHT - MIME HTML",
  "description" :"เรียนรู้เกี่ยวกับรูปแบบไฟล์ MHT และ API เพื่อสร้างและเปิดไฟล์ MHT",
  "linktitle" : "MHT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## ไฟล์ MHT คืออะไร??

ไฟล์ที่มีนามสกุล .mht เป็นรูปแบบไฟล์เก็บถาวรที่เปิดใช้งาน MIME ซึ่งมีข้อมูลประเภทต่างๆ อยู่ในไฟล์เดียว สามารถจัดเก็บข้อมูล เช่น ข้อความ รูปภาพ การจัดรูปแบบหน้าในรูปแบบของไฟล์ [CSS](/th/web/css/) JavaScript และทรัพยากรอื่นๆ เป็นทรัพยากรแบบฝังในนั้น ไฟล์ MHT ซึ่งมีข้อความประเภท MIME/rfc822 สรุปเนื้อหาทั้งหมดของไฟล์ HTML เป็นไฟล์เก็บถาวรไฟล์เดียวสำหรับการจัดเก็บในการเก็บถาวรบนอุปกรณ์จัดเก็บข้อมูล แอปพลิเคชันซอฟต์แวร์ เช่น Microsoft Word ให้คุณแปลงเอกสาร WORD เป็น MHT โดยส่งออกเป็นไฟล์ MHT ไฟล์ MHT สามารถเปิดได้โดยใช้เบราว์เซอร์ยอดนิยม เช่น Microsoft Internet Explore และ Google Chrome

## รูปแบบไฟล์ MHT

เช่นเดียวกับ [MHTML](/th/web/mhtml/) MHT ยังเป็น MIME encapsulation ของเอกสาร HTML แบบรวม เนื้อหาเอกสารภายในเอกสาร MHT เช่น รูปภาพแบบอินไลน์ สไตล์ชีต แอพเพล็ต ฯลฯ จะถูกเข้ารหัสด้วย MIME ซึ่งสิ่งเหล่านี้เชื่อมโยงกับทรัพยากรรูทผ่าน URI อีเมลไคลเอ็นต์ เช่น Microsoft Outlook จะจัดเก็บอีเมล (โดยปกติจะเป็น [EML](/th/email/eml/)) ในรูปแบบไฟล์ MHT ข้อมูลจำเพาะที่สมบูรณ์ของรูปแบบไฟล์ MHT มีอยู่ใน [RFC 822](https://tools.ietf.org/html/rfc822) และสามารถอ้างอิงถึงการพัฒนาแอปพลิเคชันซอฟต์แวร์ที่สามารถประมวลผลไฟล์ MHT

## ความแตกต่างระหว่าง MHT และ MHTML

ขณะบันทึกเพจออนไลน์ ผู้ใช้จะถูกขอให้เลือกชนิดของไฟล์รูปแบบที่ต้องบันทึกเพจออนไลน์บนระบบเนทีฟ โดยทั่วไปแล้ว ผู้ใช้จะสับสนระหว่างภาษามาร์กอัปกับรูปแบบไฟล์ MHTML พวกเขาสังเกตเห็นว่าเป็นเรื่องยากที่จะดูว่ารูปแบบไฟล์นั้นมีประสิทธิภาพมากกว่าระหว่างสิ่งเหล่านี้

เมื่อผู้ใช้ตัดสินใจที่จะหลีกเลี่ยงการเสียหน้าออนไลน์เป็นภาษามาร์กอัป โฟลเดอร์จะถูกสร้างขึ้นซึ่งประกอบด้วยไฟล์หลายไฟล์สำหรับเนื้อหาต่างๆ ของหน้า เช่น หน่วยพื้นที่ไฟล์ที่แตกต่างกันโดยสิ้นเชิงซึ่งสร้างขึ้นสำหรับข้อความ กราฟิก แอพเพล็ต ฯลฯ ในทางกลับกัน การบันทึก หน้าออนไลน์เป็น MHTML สร้างไฟล์เดียวสำหรับหน้าออนไลน์ที่สมบูรณ์ องค์ประกอบทั้งหมดของหน้าพร้อมกับกราฟิก ลิงก์ และหน่วยพื้นที่ไฟล์ทางเลือกที่ฝังอยู่ภายในไฟล์เดียว

โดยปกติแล้ว การจัดการไฟล์ MHT หรือ MHTML นั้นตรงไปตรงมา เพราะไฟล์นั้นอาจได้รับการปกป้องและแบ่งปันผ่านทางอีเมล อย่างไรก็ตาม หน่วยพื้นที่ไฟล์ภาษามาร์กอัปที่อยู่ด้านล่างโอกาสที่ข้อมูลจะสูญหายเนื่องจากการสูญหายหรือถูกลบแม้แต่ไฟล์เดียวอาจทำให้โฟลเดอร์ภาษามาร์กอัปทั้งหมดไร้ประโยชน์สำหรับผู้ใช้

## อ้างอิง

* [MHTML - วิกิพีเดีย](https://en.wikipedia.org/wiki/MHTML)
* [MHT RFC](https://tools.ietf.org/html/rfc822)

