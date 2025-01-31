{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OST - รูปแบบไฟล์ที่เก็บข้อมูล Outlook",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ OST และ API ที่สามารถสร้างและเปิดไฟล์ OST",
  "linktitle" : "OST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ OST คืออะไร??

ไฟล์ OST หรือไฟล์จัดเก็บออฟไลน์แสดงข้อมูลกล่องจดหมายของผู้ใช้ในโหมดออฟไลน์บนเครื่องท้องถิ่นเมื่อลงทะเบียนกับ Exchange Server โดยใช้ Microsoft Outlook จะถูกสร้างขึ้นโดยอัตโนมัติเมื่อใช้ Microsoft Outlook ครั้งแรกเมื่อเชื่อมต่อกับเซิร์ฟเวอร์ เมื่อสร้างไฟล์แล้ว ข้อมูลจะถูกซิงโครไนซ์กับเซิร์ฟเวอร์อีเมลเพื่อให้สามารถใช้งานแบบออฟไลน์ได้ในกรณีที่ขาดการเชื่อมต่อจากเซิร์ฟเวอร์อีเมล ไฟล์ OST สามารถใช้รายการเมลบ็อกซ์ของผู้ใช้ เช่น อีเมล รายชื่อ ข้อมูลปฏิทิน บันทึกย่อ งาน และข้อมูลอื่นๆ ที่คล้ายคลึงกัน ผู้ใช้สามารถสร้างอีเมลและรายการข้อมูลอื่นๆ ในไฟล์ OST ได้แม้ว่าจะไม่มีการเชื่อมต่อกับเซิร์ฟเวอร์ แต่สิ่งเหล่านี้จะไม่ถูกซิงโครไนซ์กับเซิร์ฟเวอร์ เมื่อสร้างการเชื่อมต่อแล้ว ไฟล์ในเครื่องจะถูกซิงโครไนซ์กับเซิร์ฟเวอร์อีกครั้ง เพื่อให้ทั้งเซิร์ฟเวอร์และสำเนาในเครื่องอยู่ในระดับข้อมูลเดียวกัน

## รูปแบบไฟล์ OST

รูปแบบไฟล์ OST (Offline Storage Table) และ [PST](/th/email/pst/) (Personal Storage Table) ประกอบด้วยรูปแบบไฟล์โฟลเดอร์ส่วนบุคคล (PFF) ที่สอดคล้องกับการจัดเก็บอีเมล ผู้ติดต่อ และการนัดหมายของผู้ใช้ ข้อมูลในไฟล์ PFF จัดเก็บในรูปแบบ little-endian โดยมีวันที่และเวลาทั้งหมดแสดงเป็น FILETIME ในรูปแบบ UTC [MS-PST] กำหนด PFF สองประเภท:

* รูปแบบ ANSI 32 บิต
* รูปแบบ Unicode 64 บิต

รูปแบบไฟล์ PST [ข้อมูลจำเพาะ](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546) ที่มีให้จาก Microsoft ยังใช้กับรูปแบบไฟล์ OST ได้ฟรีและ การให้สิทธิ์ใช้งานสิทธิบัตรแบบเพิกถอนไม่ได้ผ่าน Open Specification Promise ประกอบด้วยองค์ประกอบที่แตกต่างดังต่อไปนี้:

* ส่วนหัวของเฟล
* ข้อมูลส่วนหัวของไฟล์
* โหนดสาขาดัชนี
* โหนดใบไม้ดัชนี
* (ไฟล์) ดัชนีชดเชย
* (รายการ) ดัชนีคำอธิบาย
* คำอธิบายท้องถิ่น
* ประเภทตารางรายการ

### ข้อมูลส่วนหัว

โครงสร้าง HEADER ของไฟล์ OST อยู่ที่ส่วนต้นสุดของไฟล์ที่ค่าชดเชย 0 ประกอบด้วยข้อมูลเมตาเกี่ยวกับไฟล์ OST และข้อมูล ROOT เพื่อเข้าถึงโครงสร้างข้อมูล NDB Layer ที่อธิบายไว้ข้างต้น โครงสร้าง HEADER แตกต่างกันสำหรับรูปแบบไฟล์ OST เวอร์ชัน Unicode และ ANSI

ส่วนหัวเริ่มต้นด้วย magic word ขนาด 4 ไบต์ **!BDN** แทนด้วยไบต์ (0x21, 0x42, 0x44, 0x4E) หมายเลขเวทย์มนตร์ 2 ไบต์อีกตัว **SM** (0x53, 0x4D) ตั้งอยู่ที่ออฟเซ็ต 8 จากจุดเริ่มต้นของไฟล์ ข้อมูลเวอร์ชัน (ANSI หรือ Unicode) อยู่ที่ออฟเซ็ต 10 จากจุดเริ่มต้นของไฟล์ ค่าฐานสิบหก (0x17) ระบุไฟล์ Unicode OST ในขณะที่ 0x0E หรือ 0x0F แสดงถึงรูปแบบไฟล์ ANSI

|ฟิลด์|คำอธิบาย
---|---|
|dwMagic (4 ไบต์)|ต้องเป็น "{ 0x21, 0x42, 0x44, 0x4E } ("!BDN")"
|dwCRCPartial (4 ไบต์)|ค่า CRC 32 บิตของข้อมูล 471 ไบต์ที่เริ่มต้นจาก wMagicClient (0ffset 0x0008)
|wMagicClient (2 ไบต์)|ต้องเป็น "{ 0x53, 0x4D }"
|wVer (2 ไบต์)|เวอร์ชันรูปแบบไฟล์ ค่านี้ต้องเป็น 14 หรือ 15 หากไฟล์เป็นไฟล์ ANSI PST และต้องเป็น 23 หากไฟล์เป็นไฟล์ Unicode PST
|wVerClient (2 ไบต์)|เวอร์ชันรูปแบบไฟล์ไคลเอนต์ เวอร์ชันที่สอดคล้องกับรูปแบบที่อธิบายไว้ในเอกสารนี้คือ 19 ผู้สร้างไฟล์ PST ใหม่ตามเอกสารนี้ควรกำหนดค่าเริ่มต้นเป็น 19
|bPlatformCreate (1 ไบต์)|ค่านี้ต้องตั้งค่าเป็น 0x01
|bPlatformAccess (1 ไบต์)|ค่านี้ต้องตั้งค่าเป็น 0x01
|dwReserved (8 ไบต์)|
|bidUnused (8 ไบต์ Unicode เท่านั้น)|ช่องว่างภายในที่ไม่ได้ใช้ถูกเพิ่มเมื่อสร้างรูปแบบไฟล์ Unicode PST
|bidNextP (Unicode: 8 ไบต์; ANSI: 4 ไบต์)|BID หน้าถัดไป หน้าต่างๆ มีตัวนับพิเศษสำหรับจัดสรรค่าดัชนีราคาเสนอ ค่าของ bidIndex สำหรับ BIDs สำหรับเพจได้รับการจัดสรรจากตัวนับนี้
|bidNextB (4 ไบต์ ANSI เท่านั้น): |BID ถัดไป ค่านี้เป็นตัวนับโมโนโทนิกที่ระบุ BID ที่จะกำหนดสำหรับบล็อกที่จัดสรรถัดไป ค่า BID จะเพิ่มขึ้นทีละ 4 สำหรับรายละเอียดเพิ่มเติม โปรดดูหัวข้อ 2.2.2.2
|dwUnique (4 ไบต์)|นี่คือค่าที่เพิ่มขึ้นแบบโมโนโทนซึ่งแก้ไขทุกครั้งที่มีการแก้ไขโครงสร้างส่วนหัวของไฟล์ PST ฟังก์ชันของค่านี้คือการให้ค่าที่ไม่ซ้ำกัน และเพื่อให้แน่ใจว่า HEADER CRCs แตกต่างกันหลังจากการแก้ไขส่วนหัวแต่ละครั้ง
|rgnid[]   (128 ไบต์)|อาร์เรย์คงที่ของ 32 NID แต่ละอันสอดคล้องกับหนึ่งใน 32 NID_TYPE ที่เป็นไปได้ (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE,NID_TYPE_ASSOC_MESSAGE)
|qwUnused (8 ไบต์)|พื้นที่ที่ไม่ได้ใช้; ต้องตั้งค่าเป็นศูนย์ รูปแบบไฟล์ Unicode PST เท่านั้น
|root (Unicode: 72 bytes; ANSI: 40 bytes)|โครงสร้าง ROOT (ส่วน 2.2.2.5)
|dwAlign (4 ไบต์)|ไบต์การจัดตำแหน่งที่ไม่ได้ใช้; ต้องตั้งค่าเป็นศูนย์ รูปแบบไฟล์ Unicode PST เท่านั้น
|rgbFM (128 ไบต์)|เลิกใช้ FMap ไม่ใช้แล้วและต้องเติมด้วย 0xFF ผู้อ่านควรละเว้นค่าของไบต์เหล่านี้
|rgbFP (128 ไบต์)|เลิกใช้ FPMap ไม่ใช้แล้วและต้องเติมด้วย 0xFF ผู้อ่านควรละเว้นค่าของไบต์เหล่านี้
|bSentinel (1 ไบต์)|ต้องตั้งค่าเป็น 0x80
|bCryptMethod (1 ไบต์)|ระบุวิธีเข้ารหัสข้อมูลภายในไฟล์ PST ต้องตั้งค่าเป็นค่าที่กำหนดไว้ล่วงหน้าค่าใดค่าหนึ่ง (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC)
|rgbReserved (2 ไบต์)| ที่สงวนไว้; ต้องตั้งค่าเป็นศูนย์
|bidNextB (8 ไบต์)|ระบุค่า BID ถัดไปที่มีอยู่ รูปแบบไฟล์ Unicode PST เท่านั้น
|bidNextB (Unicode เท่านั้น: 8 ไบต์)|BID ถัดไป ค่านี้เป็นตัวนับโมโนโทนิกที่ระบุ BID ที่จะกำหนดสำหรับบล็อกที่จัดสรรถัดไป ค่า BID จะเพิ่มขึ้นทีละ 4 สำหรับรายละเอียดเพิ่มเติม โปรดดูหัวข้อ 2.2.2.2
|dwCRCFull (4 ไบต์)|ค่า CRC 32 บิตของข้อมูล 516 ไบต์ที่เริ่มต้นจาก wMagicClient ถึง bidNextB รวมอยู่ด้วย รูปแบบไฟล์ Unicode PST เท่านั้น
|ullReserved (8 ไบต์)|สงวน; ต้องตั้งค่าเป็นศูนย์ รูปแบบไฟล์ ANSI PST เท่านั้น
|dwReserved (4 ไบต์)|สงวน; ต้องตั้งค่าเป็นศูนย์ รูปแบบไฟล์ ANSI PST เท่านั้น
|rgbReserved2 (3 ไบต์)|
|bสงวนไว้ (1 ไบต์) |
|rgbReserved3 (32 ไบต์) |

## อ้างอิง

* [รูปแบบไฟล์โฟลเดอร์ส่วนบุคคลของ Outlook (.ost)](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [ข้อกำหนดรูปแบบไฟล์โฟลเดอร์ส่วนบุคคล](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

