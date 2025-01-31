{
  "date" : "2022-02-19",
  "keywords" :["xoj", "File", "Extension", "File Format", "File Extension", "Xournal notebook"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ XOJ - รูปแบบไฟล์สมุดบันทึก Xournal",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ XOJ และ API ที่สามารถสร้างและเปิดไฟล์ XOJ",
  "linktitle" : "XOJ",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-02-19"
}

## ไฟล์ XOJ คืออะไร??

ไฟล์ XOJ เป็นไฟล์โน้ตบุ๊กที่มีโน้ตที่จดโดยใช้ซอฟต์แวร์มือจดโน้ต Xournal Xournal เป็นแอปพลิเคชั่นฟรีหลายแพลตฟอร์มที่ให้คุณสร้างบันทึกด้วยเนื้อหาประเภทต่าง ๆ เช่น ข้อความ รูปภาพ และดูเดิลที่เขียนด้วยลายมือ ไฟล์ XOJ ถูกสร้างขึ้นเมื่อไฟล์โน้ตบุ๊กใหม่ถูกสร้างขึ้นด้วย Xournal ไฟล์ XOJ เหล่านี้สามารถแชร์กับผู้ใช้รายอื่นได้เช่นกันสำหรับการแชร์ข้อมูล Xournal เวอร์ชันล่าสุดคือ [Xournal++](https://github.com/xournalpp/xournalpp) ซึ่งเป็นเวอร์ชันข้ามแพลตฟอร์มของ Xournal

## รูปแบบไฟล์ XOJ

ไฟล์ XOJ อยู่ในรูปแบบไฟล์ XML และบันทึกลงดิสก์ในรูปแบบบีบอัดโดยใช้การบีบอัด [.gz](/th/compression/gz/) เนื่องจากการใช้รูปแบบ XML สากล ไฟล์ XOJ จึงสามารถเปิดและแก้ไขได้ด้วยตัวแปรข้ามแพลตฟอร์ม Xournal++

ไฟล์ XOJ แต่ละไฟล์อาจมีสมุดบันทึก Xournal อีกหนึ่งหน้า

## XOJ - แพลตฟอร์มที่รองรับ

Xournal เป็นหลายแพลตฟอร์มและสามารถบันทึกโน้ตบุ๊กเป็นไฟล์ XOJ บนระบบปฏิบัติการต่อไปนี้

* ลินุกซ์
* แมคโอเอส
* หน้าต่าง
* แอนดรอยด์
* iOS บิลด์

## อ้างอิง

* [Xournal++](https://github.com/xournalpp/xournalpp)

