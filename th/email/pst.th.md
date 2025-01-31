{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PST - รูปแบบไฟล์ที่เก็บข้อมูลส่วนตัวของ Outlook",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ PST และ API ที่สามารถสร้างและเปิดไฟล์ PST",
  "linktitle" : "PST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ PST คืออะไร??

ไฟล์ที่มีนามสกุล .pst แสดงถึงไฟล์ที่เก็บข้อมูลส่วนตัวของ Outlook (เรียกอีกอย่างว่าตารางที่เก็บข้อมูลส่วนตัว) ที่เก็บข้อมูลต่างๆ ของผู้ใช้ ข้อมูลผู้ใช้ถูกจัดเก็บไว้ในโฟลเดอร์ประเภทต่างๆ ซึ่งรวมถึงอีเมล รายการปฏิทิน บันทึก รายชื่อ และรูปแบบไฟล์อื่นๆ ไฟล์ PST ใช้สำหรับเก็บข้อมูลอีเมลแบบออฟไลน์ซึ่งสามารถโหลดและดูในภายหลังในแอปพลิเคชันต่างๆ

## ข้อมูลจำเพาะรูปแบบไฟล์ PST

รูปแบบไฟล์ PST [ข้อมูลจำเพาะ](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546) มีให้ใช้งานจาก Microsoft เป็นสิทธิ์ใช้งานสิทธิบัตรฟรีและเพิกถอนไม่ได้ผ่าน Open Specifications Promise .

### ประเภทของรูปแบบ PST

รูปแบบไฟล์ PST แบ่งออกเป็นสองประเภทตามการเข้ารหัสของประเภทไฟล์ ไฟล์ PST ที่เข้ารหัส ANSI เป็นรูปแบบไฟล์ที่เก่ากว่าและรองรับโดย Outlook 2002 และเวอร์ชันก่อนหน้าเท่านั้น ไฟล์ดังกล่าวมีขนาดจำกัดสูงสุด 2 GB (2^^31^^ ไบต์) และไม่รองรับ Unicode ประเภทรูปแบบไฟล์ที่ทันสมัยกว่า ซึ่งใช้การเข้ารหัส Unicode ช่วยขจัดข้อจำกัดด้านขนาดไฟล์ และสามารถเข้าถึงขนาดข้อมูลสูงสุดที่ 50GB

### การจัดระเบียบเชิงตรรกะของรูปแบบไฟล์ PST

ที่ฐานของรูปแบบไฟล์ PST มี B-Tree ที่ช่วยจัดเรียงข้อมูลและอนุญาตให้ค้นหา เข้าถึงตามลำดับ แทรก ลบ ฯลฯ ในเวลาลอการิทึม โครงสร้างโดยรวมของไฟล์ PST แบ่งออกเป็นสามชั้น

![Logical layers of a PST file](/th/email/PST-1.png "Logical layers of a PST file")

`Node Database (NDB) Layer` - เลเยอร์ฐานข้อมูลโหนดอยู่ที่ระดับล่างของไฟล์ PST และรวมฐานข้อมูลของโหนด โหนดเหล่านี้เป็นตัวแทนของพื้นที่จัดเก็บระดับล่างของรูปแบบไฟล์ PST เลเยอร์ NDB ประกอบด้วยส่วนหัว ข้อมูลการจัดสรรไฟล์ บล็อก และ BTrees (โหนด BTree และ Block BTree) จากมุมมองของหน่วยเก็บข้อมูล โหนดและบล็อกของเลเยอร์ NDB ถูกเชื่อมโยงผ่าน Data BID ซึ่งเป็นหนึ่งในสี่คุณสมบัติของการอ้างอิงโหนด ได้แก่ NID (Node ID), Parent NID, Data BID (Block BID) และ SubNode BID

`Lists, Tables and Properties Layer -` เลเยอร์ LTP ให้ความเข้าใจเชิงตรรกะของแนวคิดระดับที่สูงกว่าบน NDB นอกจากองค์ประกอบอื่นๆ แล้ว เลเยอร์ LTP ยังประกอบด้วย Property Context (PC) และ Table Context (TC) เป็นหลัก พีซีคือกลุ่มของคุณสมบัติ ในขณะที่ TC เป็นตัวแทนของเมทริกซ์สองมิติของการรวบรวมคุณสมบัติ เทียบกับการมีอยู่ของคุณสมบัติเหล่านี้ การใช้งานพีซีและ TC อย่างมีประสิทธิภาพ เลเยอร์ LTP ใช้โครงสร้างข้อมูลสองประเภทต่อไปนี้บนโหนด NDB:

* Heap On Node (HN) - เปิดใช้งานการจัดสรรย่อยสตรีมข้อมูลของโหนดเป็นชิ้นส่วนขนาดเล็กที่มีขนาดตัวแปร
* BTree on Heap (BTH) - BTH มอบวิธีที่สะดวกและใช้งานได้จริงในการค้นหาผ่านดาต้าพีซี ดังที่อธิบายไว้ข้างต้น ใช้งานเป็น BTH และนั่นคือเหตุผลว่าทำไมจึงมีการใช้งานโดยสร้างภายในโครงสร้าง HN

`เลเยอร์ข้อความ -` กฎระดับที่สูงขึ้นและตรรกะทางธุรกิจสำหรับการทำงานกับไฟล์ PST ถูกนำมาใช้ในเลเยอร์นี้ ผลลัพธ์ทางลอจิคัลของเลเยอร์นี้ส่งผลให้เป็นวัตถุโฟลเดอร์ วัตถุข้อความ วัตถุแนบ และคุณสมบัติ ซึ่งเป็นไปได้โดยการรวมเลเยอร์ LTP และ NDB กฎและข้อกำหนดที่ต้องปฏิบัติตามเมื่อแก้ไขเนื้อหา PST จะกำหนดไว้ที่ชั้นนี้ด้วย

### การจัดระเบียบทางกายภาพของรูปแบบไฟล์ PST

การจัดระเบียบไฟล์ในระดับสูงของไฟล์ PST ดังแสดงในรูปด้านล่าง นี่เป็นเพียงภาพรวมของแนวคิดต่างๆ จากองค์ประกอบทางตรรกะของไฟล์ PST

![Physical organization of the PST file format](/th/email/PST-2.png "Physical organization of the PST file format")


#### ข้อมูลส่วนหัว PST

โครงสร้าง HEADER ของไฟล์ PST อยู่ที่ส่วนต้นสุดของไฟล์ที่ค่าชดเชย 0 ประกอบด้วยข้อมูลเมตาเกี่ยวกับไฟล์ PST และข้อมูล ROOT เพื่อเข้าถึงโครงสร้างข้อมูล NDB Layer ที่อธิบายไว้ข้างต้น โครงสร้างส่วนหัวจะแตกต่างกันสำหรับรูปแบบไฟล์ PST เวอร์ชัน Unicode และ ANSI

ส่วนหัวเริ่มต้นด้วย magic word ขนาด 4 ไบต์ **!BDN** แทนด้วยไบต์ (0x21, 0x42, 0x44, 0x4E) หมายเลขเวทย์มนตร์ 2 ไบต์อีกตัว **SM** (0x53, 0x4D) ตั้งอยู่ที่ออฟเซ็ต 8 จากจุดเริ่มต้นของไฟล์ ข้อมูลเวอร์ชัน (ANSI หรือ Unicode) อยู่ที่ออฟเซ็ต 10 จากจุดเริ่มต้นของไฟล์ ค่าฐานสิบหก (0x17) ระบุไฟล์ Unicode PST ในขณะที่ 0x0E หรือ 0x0F แสดงถึงรูปแบบไฟล์ ANSI

|ฟิลด์|คำอธิบาย
---|---|
|dwMagic (4 ไบต์)|ต้องเป็น "{ 0x21, 0x42, 0x44, 0x4E } ("!BDN")"
|dwCRCPartial (4 ไบต์)|ค่า CRC 32 บิตของข้อมูล 471 ไบต์ที่เริ่มต้นจาก wMagicClient (0ffset 0x0008)
|wMagicClient (2 ไบต์)|ต้องเป็น "{ 0x53, 0x4D }"
|wVer (2 ไบต์)|เวอร์ชันรูปแบบไฟล์ ค่านี้ต้องเป็น 14 หรือ 15 หากไฟล์เป็นไฟล์ ANSI PST และต้องเป็น 23 หากไฟล์เป็นไฟล์ Unicode PST
|wVerClient (2 ไบต์)|เวอร์ชันรูปแบบไฟล์ไคลเอนต์ เวอร์ชันที่ตรงกับรูปแบบที่อธิบายไว้ในเอกสารนี้คือ 19 ผู้สร้างไฟล์ PST ใหม่ที่ใช้เอกสารนี้ควรกำหนดค่าเริ่มต้นเป็น 19
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

### การป้องกันข้อมูล ###

เพื่อความปลอดภัย ไฟล์ PST ยังสามารถป้องกันด้วยรหัสผ่าน ซึ่งต้องใช้แอปพลิเคชันโหลดเพื่อใช้รหัสผ่านก่อนที่จะสามารถดูได้ รหัสผ่านที่ใช้กับไฟล์ PST จะถูกเก็บไว้ในที่เก็บข้อความ อย่างไรก็ตาม การดำเนินการนี้ไม่ได้ให้การปกป้องข้อมูลที่รัดกุมเนื่องจากเครื่องมือที่มีอยู่สามารถลบรหัสผ่านได้ นอกจากนี้ รหัสผ่านที่ผู้ใช้ระบุไม่ได้ถูกใช้เป็นส่วนหนึ่งของคีย์สำหรับการเข้ารหัสและถอดรหัสอัลกอริทึมการเข้ารหัส ดังนั้นจึงไม่มีประโยชน์ในการปกป้องข้อมูลที่จะเข้าถึงโดยบุคคลที่ไม่ได้รับอนุญาต การจัดเก็บรหัสผ่านเป็นแฮช CRC-32 ของสตริงเดิมทำให้เป็นวิธีที่อ่อนแอในการรักษาความปลอดภัยของข้อมูลจากการใช้วิธีเดรัจฉาน

## อ้างอิง ##

* [รูปแบบไฟล์โฟลเดอร์ส่วนบุคคลของ Outlook (.pst)](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [ข้อกำหนดรูปแบบไฟล์โฟลเดอร์ส่วนบุคคล](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

