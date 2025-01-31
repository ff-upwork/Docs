{
  "date" : "2022.01.31",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ P7S - ข้อความอีเมลที่เซ็นชื่อแบบดิจิทัล",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ P7S และ API ที่สามารถสร้างและเปิดไฟล์ P7S",
  "linktitle" : "P7S",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2022.01.31"
}

## ไฟล์ P7S คืออะไร??

ไฟล์ P7S เป็นลายเซ็นดิจิทัลที่ได้รับพร้อมกับอีเมลที่เซ็นชื่อแบบดิจิทัล การมีอยู่ของไฟล์นี้เป็นสิ่งที่แนบมากับอีเมลเป็นการยืนยันว่าอีเมลนั้นถูกส่งมาจากแหล่งที่มาที่แท้จริง สิ่งนี้ทำให้มั่นใจได้ว่าผู้ส่งมีใบรับรองการเซ็นชื่ออีเมลติดตั้งอยู่ในคอมพิวเตอร์ เมื่ออีเมลที่ลงชื่อแล้วถูกส่งจากคอมพิวเตอร์ของผู้ใช้ ไฟล์ P7S จะถูกแนบมาพร้อมกับอีเมลที่มีชื่อผู้ส่ง ไคลเอนต์อีเมลที่รองรับอีเมลที่ลงนามแล้วสามารถดูข้อมูลของผู้ส่งได้

## รูปแบบไฟล์ P7S - ข้อมูลเพิ่มเติม

ไฟล์ S/MIME (Secure/Multipurpose Internet Mail Extensions) P7S มีข้อมูลในรูปแบบข้อความล้วนที่มนุษย์สามารถอ่านได้ ไคลเอนต์อีเมล เช่น Microsoft Outlook, Apple Mail และ Mozilla Thunderbird รองรับการอ่านข้อมูลที่เซ็นชื่อแบบดิจิทัลจากอีเมล S/MIME การลงชื่อในอีเมลเป็นการยืนยันตัวตนของผู้ส่งและบอกผู้รับว่าข้อความนั้นเป็นของจริง เมื่อดาวน์โหลดอีเมลจากไคลเอ็นต์อีเมล (ไม่ว่าจะเป็น [EML](/th/email/eml/) หรือ [MSG](/th/email/msg/)) ไฟล์ P7S เหล่านี้จะถูกแนบมากับอีเมลเหล่านี้

ไฟล์ P7S มีข้อมูลต่อไปนี้:

* แหล่งที่มาของที่มาของอีเมล
* วันที่และเวลาที่ส่ง
* ไม่ว่าจะได้รับการแก้ไขระหว่างการส่ง

ข้อมูลนี้ถูกฝังโดยใช้เทคโนโลยี Public-Key Cryptography Standard #7 (PKCS7) สำหรับการแนบลายเซ็นที่เข้ารหัสแบบดิจิทัลกับอีเมล

## อ้างอิง ##

* [เครื่องมือลงชื่อเข้าใช้ของ Microsoft](https://learn.microsoft.com/en-us/windows-hardware/drivers/devtest/signtool)

