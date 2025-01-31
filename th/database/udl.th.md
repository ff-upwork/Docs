{
  "date" : "2021-06-21",
  "keywords" :[ "UDL", "นามสกุล", "ไฟล์ udl", "รูปแบบไฟล์ udl", "ประเภทไฟล์ฐานข้อมูล", "รูปแบบไฟล์ฐานข้อมูล", "ไฟล์ udl คืออะไร" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"เรียนรู้เกี่ยวกับรูปแบบไฟล์ UDL และ API ที่สามารถสร้างและเปิดไฟล์ UDL",
  "title" :"UDL - ไฟล์ Microsoft Universal Data Link",
  "linktitle" : "UDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-21"
}

## ไฟล์ UDL คืออะไร??
ไฟล์ที่มีนามสกุล .udl เรียกว่าไฟล์ Microsoft Universal Data Link; การระบุแอตทริบิวต์การเชื่อมต่อ ใช้โดยแอพ Windows เพื่อสร้างการเชื่อมต่อกับฐานข้อมูล ไฟล์ UDL มีสตริงการเชื่อมต่อสำหรับแหล่งข้อมูล OLE DB; ด้วยชื่อผู้ใช้และรหัสผ่านและคุณสมบัติสตริงการเชื่อมต่อที่จำเป็น เพื่อหลีกเลี่ยงการระบุคุณสมบัติด้วยมือโดยตรงในสตริงการเชื่อมต่อ สามารถใช้กล่องโต้ตอบคุณสมบัติการเชื่อมโยงข้อมูลเพื่อบันทึกข้อมูลการเชื่อมต่อในไฟล์ .udl แทนได้

## รูปแบบไฟล์ UDL
โดยพื้นฐานแล้ว ไฟล์ UDL (Universal Data Link) เป็นไฟล์ข้อความอย่างง่ายที่ประกอบด้วยสตริงการเชื่อมต่อฐานข้อมูลที่มีแอตทริบิวต์หรือคุณสมบัติเฉพาะ เมื่อสร้างไฟล์ UDL แล้ว สามารถทดสอบได้โดยใช้ SQL Server Management Studio เพื่อตรวจสอบการเชื่อมต่อ

### คุณสมบัติสตริงการเชื่อมต่อ
สามารถตั้งค่าคุณสมบัติต่อไปนี้ใน UDL เพื่อให้แน่ใจว่ามีการเชื่อมต่อที่เหมาะสม:

- **ชื่อเซิร์ฟเวอร์**: ตำแหน่งของเซิร์ฟเวอร์ที่มีฐานข้อมูลที่คุณต้องการเข้าถึง
- **ตัวเลือกการตรวจสอบสิทธิ์**
- **การรับรองความถูกต้องของ Windows**: การรับรองความถูกต้องไปยัง SQL Server โดยใช้ข้อมูลรับรองบัญชี Windows ของผู้ใช้ที่เข้าสู่ระบบในปัจจุบัน
- **การรับรองความถูกต้องของเซิร์ฟเวอร์ SQL**: การรับรองความถูกต้องโดยใช้ ID เข้าสู่ระบบและรหัสผ่าน
- **Active Directory - แบบรวม**: การตรวจสอบสิทธิ์แบบรวมด้วยข้อมูลประจำตัว Azure Active Directory; สามารถใช้สำหรับการรับรองความถูกต้องของ Windows กับ SQL Server
- **Active Directory - รหัสผ่าน**: การตรวจสอบ ID ผู้ใช้และรหัสผ่านด้วยข้อมูลประจำตัว Azure Active Directory
- **Active Directory - Universal พร้อมรองรับ MFA**: การรับรองความถูกต้องแบบโต้ตอบด้วยข้อมูลประจำตัว Azure Active Directory
- **Active Directory - Service Principal**: การรับรองความถูกต้องด้วย Azure Active Directory บริการหลัก
- **เซิร์ฟเวอร์ SPN**: หากคุณใช้การเชื่อมต่อที่เชื่อถือได้ คุณสามารถระบุชื่อบริการหลัก (SPN) สำหรับเซิร์ฟเวอร์ได้
- **ชื่อผู้ใช้**: พิมพ์ ID ผู้ใช้เพื่อใช้สำหรับการตรวจสอบสิทธิ์เมื่อคุณลงชื่อเข้าใช้แหล่งข้อมูล
- **รหัสผ่าน**: พิมพ์รหัสผ่านเพื่อใช้สำหรับการตรวจสอบสิทธิ์เมื่อคุณลงชื่อเข้าใช้แหล่งข้อมูล
- **รหัสผ่านเปล่า**: เมื่อเลือกตัวเลือกนี้ ให้เปิดใช้งานผู้ให้บริการที่ระบุเพื่อใช้รหัสผ่านเปล่าในสตริงการเชื่อมต่อ
- **อนุญาตให้บันทึกรหัสผ่าน**: อนุญาตให้บันทึกรหัสผ่านด้วยสตริงการเชื่อมต่อ
- **ใช้การเข้ารหัสที่แข็งแกร่งสำหรับข้อมูล**: ข้อมูลที่ส่งผ่านการเชื่อมต่อจะถูกเข้ารหัส
- **ใบรับรองเซิร์ฟเวอร์ที่เชื่อถือได้**: ใบรับรองของเซิร์ฟเวอร์จะได้รับการตรวจสอบ
- **ฐานข้อมูล**: ชื่อฐานข้อมูลที่คุณต้องการเข้าถึง
- **แนบไฟล์ฐานข้อมูลเป็นชื่อฐานข้อมูล**: ระบุชื่อไฟล์หลักสำหรับฐานข้อมูลที่แนบได้

## อ้างอิง ##

* [ส่วนประกอบการเข้าถึงข้อมูลของ Microsoft](https://en.wikipedia.org/wiki/Microsoft_Data_Access_Components#Universal_data_link)
* [การกำหนดค่า Universal Data Link (UDL)](https://learn.microsoft.com/en-us/sql/connect/oledb/help-topics/data-link-pages?view=sql-server-ver15)

