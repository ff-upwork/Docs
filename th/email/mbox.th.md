{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MBOX - ไฟล์กล่องจดหมายอีเมล",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ MBOX และ API ที่สามารถสร้างและเปิดไฟล์ MBOX",
  "linktitle" : "MBOX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ MBOX คืออะไร??

รูปแบบไฟล์ MBox เป็นคำทั่วไปที่แสดงถึงที่เก็บสำหรับรวบรวมข้อความจดหมายอิเล็กทรอนิกส์ ข้อความจะถูกเก็บไว้ในคอนเทนเนอร์พร้อมกับไฟล์แนบ ข้อความจากทั้งโฟลเดอร์จะถูกบันทึกในไฟล์ฐานข้อมูลไฟล์เดียว และข้อความใหม่จะถูกต่อท้ายไฟล์ แอปพลิเคชันและ API จำนวนมากให้การสนับสนุนรูปแบบไฟล์ MBox เช่น Apple Mail และ Mozilla Thunderbird

## รูปแบบไฟล์ MBOX ##

รูปแบบไฟล์ MBox ยังคงไม่เป็นมาตรฐานเป็นเวลานานจนกระทั่งปี 2548 เมื่อแอปพลิเคชัน/mbox ได้รับมาตรฐานเป็น [RFC 4155.](https://tools.ietf.org/rfc/rfc4155.txt) Messages ในรูปแบบ RFC 2822 จะถูกเชื่อมเข้าด้วยกันในรูปแบบไฟล์ MBox ทีละไฟล์ แต่ละข้อความจะขึ้นต้นด้วยบรรทัดคั่นที่ระบุผู้ส่งข้อความ และยังระบุวันที่และเวลาที่ผู้รับคนสุดท้ายได้รับข้อความด้วย (ระบบ Last-Hop ในเส้นทางการถ่ายโอน หรือระบบที่ทำหน้าที่เป็นผู้รับ ร้านไปรษณีย์). โดยทั่วไปแต่ละข้อความจะถูกยกเลิกโดยบรรทัดว่าง จุดสิ้นสุดของฐานข้อมูลมักรับรู้ได้จากการไม่มีข้อมูลเพิ่มเติมใดๆ หรือโดยการมีเครื่องหมายจุดสิ้นสุดของไฟล์ที่ชัดเจน

## การอ่านข้อความจากไฟล์ MBox ##

เครื่องอ่านสแกนผ่านไฟล์ mbox เพื่อค้นหาบรรทัด From_ บรรทัด From_ ใด ๆ ทำเครื่องหมายจุดเริ่มต้นของข้อความ ผู้อ่านไม่ควรพยายามใช้ประโยชน์จากความจริงที่ว่าทุกบรรทัด From_ (ผ่านจุดเริ่มต้นของไฟล์) บรรทัดว่าง เมื่อเครื่องอ่านพบข้อความ เครื่องจะแยกผู้ส่งซองจดหมาย (อาจเสียหาย) และวันที่ส่งออกจากบรรทัด From_ จากนั้นจะอ่านจนถึงบรรทัด From_ ถัดไปหรือจุดสิ้นสุดของไฟล์ แล้วแต่ว่าจะถึงอย่างใดก่อน มันตัดบรรทัดว่างสุดท้ายออกและลบเครื่องหมายคำพูดของ >From_ บรรทัดและ >>From_ บรรทัดและอื่นๆ ผลลัพธ์คือข้อความ RFC 822

## การพิจารณาการเข้ารหัส ##

เนื้อหาของไฟล์ MBox อาจปะปนกันกลับไม่ได้เมื่ออีเมลที่ได้รับมีไฟล์ Mbox เป็นไฟล์แนบ และบันทึกไว้ในไฟล์ Mbox อื่น เพื่อหลีกเลี่ยงปัญหานี้ ระบบการส่งข้อความต้องเข้ารหัสฐานข้อมูล mbox ด้วยการเข้ารหัสการถ่ายโอนแบบไม่โปร่งใส (เช่น BASE64 หรือ Quoted-Printable) เมื่อใดก็ตามที่วัตถุดังกล่าวถูกถ่ายโอนผ่านโปรโตคอลการส่งข้อความ ผู้ดำเนินการควรเตรียมพร้อมที่จะเข้ารหัสข้อมูล mbox ภายในเครื่อง หากได้รับข้อมูลที่ไม่เป็นไปตามข้อกำหนด

## อ้างอิง ##

* [MBox - RFC4155](https://tools.ietf.org/rfc/rfc4155.txt)
* [เอ็มบ็อกซ์ - วิกิพีเดีย](https://en.wikipedia.org/wiki/Mbox)

