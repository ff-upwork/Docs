{
  "date" : "2021-04-10",
  "keywords" :[ "TR3", "ไฟล์", "นามสกุล", "รูปแบบไฟล์", "eBook", "TomeRaider", "Yadabyte" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ TR3 และ API ที่สามารถสร้างและเปิดไฟล์ TR3",
  "title" :"ไฟล์ eBook TR3 - TomeRaider 3",
  "linktitle" : "TR3",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-04-10"
}

## ไฟล์ TR3 คืออะไร?? ##

ไฟล์ TR3 เป็น eBook ของ TomeRaider 3 ที่ให้การสนับสนุนการค้นหาและการบีบอัดที่รวดเร็ว ที่สามารถทำงานได้อย่างถูกต้องผ่านโปรแกรมที่เกี่ยวข้องกับ TomeRaider Yadabyte เป็นผู้พัฒนาซอฟต์แวร์นี้ ซึ่งเป็นบริษัทซอฟต์แวร์และการพัฒนาเว็บไซต์ของอังกฤษในสหราชอาณาจักร แอปพลิเคชันตัวอ่าน eBook ของ TomeRaider สามารถใช้เพื่อการทำงานที่เหมาะสมและการจัดการเนื้อหาของไฟล์ TR3 เหล่านี้ เครื่องอ่าน eBook ที่เกี่ยวข้องนี้สามารถติดตั้งในคอมพิวเตอร์ที่ทำงานบนระบบที่ใช้ Microsoft Windows และอุปกรณ์พกพาที่สามารถถ่ายโอนได้จำนวนมาก ไฟล์ TR3 อยู่ในกลุ่มของไฟล์ eBook ที่ใช้ในระบบปฏิบัติการเช่น Windows 10, Windows 7, Windows 8 / 8.1, Windows Vista, Windows XP

TR3 **แท็ก HTML** เฉพาะมีดังนี้:

|แท็ก|รายละเอียด|
---|---|
|\<new> |ในการสร้างไฟล์ TomeRaider จากไฟล์ข้อความ แท็กใหม่เป็นสิ่งที่จำเป็น<new> แท็กกำหนดจุดเริ่มต้นของหน้า |
|\<CATDEF> ... \</CATDEF> |กำหนดชื่อหมวดหมู่|
|\<META> ... \</META> |เป็นแท็กที่ใช้กำหนดข้อมูลเมตาทั้งหมดที่ใช้ในรูปแบบไฟล์ แท็กนี้มีพารามิเตอร์จำนวนหนึ่ง|
|\<EXPMSG> |แท็กนี้ควบคุมข้อความที่ปรากฏขึ้นเมื่อไฟล์หมดอายุ เมื่อใดก็ตามที่ผู้ใช้พยายามดูเพจหลังจากไฟล์หมดอายุ ข้อความหมดอายุจะปรากฏขึ้นแทนข้อความเพจจริง|
|\<DIEMSG> |แท็กนี้คล้ายกับ EXPMSG ใช้เพื่อแสดงข้อความเมื่อไฟล์ตาย|
|\<ENGMSG> |แท็กนี้ใช้เพื่อสร้างข้อความที่แสดงสำหรับเพจที่เข้ารหัส ข้อความนี้จะปรากฏขึ้นแทนข้อความของเพจหากผู้ใช้พยายามเปิดเพจที่เข้ารหัสก่อนที่จะปลดล็อค|
|\<expmsg> ,\<diemsg> และ \<encmsg> |ละเว้นภายในข้อความของหน้า ต้องวางไว้ในส่วนหัวของไฟล์ก่อนส่วนแรก<new> แท็ก.|
|\<SELECTION> . \</ SELECTION> |ใช้เพื่อสนับสนุน Query's แท็กนี้ต้องอยู่ก่อนแท็กแรก<new> แท็ก โดยจะรวบรวมข้อมูลการเลือกสำหรับการค้นหาของผู้ใช้|
|\<catset> . \</catset> | ใช้ในการกำหนดชื่อหมวดหมู่สำหรับแต่ละเรื่อง|


## ปัญหาในการเปิดไฟล์ TR3 ##

ต่อไปนี้คือรายการปัญหาทั่วไปที่อาจเกิดขึ้นและทำให้รูปแบบไฟล์ทำงานผิดพลาด:

* ไฟล์เสียหาย
* ไฟล์ติดไวรัสเนื่องจากไวรัส
* ลิงก์ที่ไม่เหมาะสมไปยังไฟล์ TR3 ในการเข้าถึงไฟล์เก็บถาวร
* ไม่มีสิทธิ์ในระบบในการเปิดไฟล์
* ไดรฟ์ที่ล้าสมัยในระบบของคุณ
* ลบรายงานของ TR3 ออกจากไฟล์เก็บถาวรของ Windows
* การติดต่อผู้พัฒนาอาจเป็นตัวเลือกที่ดีกว่าเพื่อให้ได้ผลลัพธ์ที่ดีขึ้น

