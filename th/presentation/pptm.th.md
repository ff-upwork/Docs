{
  "date" : "2019-10-11",
  "keywords" :[ "ไฟล์ pptm", "รูปแบบไฟล์ pptm", "ไฟล์ pptm คืออะไร", "ไฟล์", "ตัวอย่าง pptm", "นามสกุลไฟล์ pptm","นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PPTM - รูปแบบไฟล์งานนำเสนอ PowerPoint ที่เปิดใช้งานมาโคร",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ PPTM และ API ที่สามารถสร้างและเปิดไฟล์ PPTM",
  "linktitle" : "PPTM",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

ไฟล์ที่มีนามสกุล PPTM เป็นไฟล์นำเสนอที่เปิดใช้งานมาโครซึ่งสร้างด้วย Microsoft PowerPoint 2007 หรือเวอร์ชันที่สูงกว่า คล้ายกับไฟล์ [PPTX](/th/presentation/pptx/) โดยมีข้อแตกต่างตรงที่ไฟล์ด้านข้างไม่สามารถเรียกใช้งานมาโครแม้ว่าจะมีมาโครอยู่ก็ตาม ไฟล์ PPTM สามารถแก้ไขได้โดยเปิดใน Microsoft PowerPoint และอัปเดตเนื้อหา อีกรูปแบบที่คล้ายกันคือ PPSM แต่เป็นแบบอ่านอย่างเดียวโดยค่าเริ่มต้น และเริ่มสไลด์โชว์เมื่อเปิด PPTM เช่น PPTX มีสไลด์สำหรับองค์ประกอบการนำเสนอต่างๆ เช่น ข้อความ รูปภาพ วิดีโอ กราฟ และเนื้อหาอื่นๆ ที่เกี่ยวข้อง

## ประวัติย่อ ##

รูปแบบไฟล์ PPTM เปิดตัวในปี 2550 และใช้มาตรฐาน Open XML ที่ดัดแปลงโดย Microsoft ในปี 2543 ไฟล์ประเภทใหม่ได้เพิ่มข้อดีของขนาดไฟล์ที่เล็ก การเปลี่ยนแปลงความเสียหายน้อยลง และการแสดงรูปภาพที่มีรูปแบบที่ดี ในช่วงต้นปี 2000 Microsoft ตัดสินใจทำการเปลี่ยนแปลงเพื่อรองรับมาตรฐานสำหรับ **Office Open XML** ภายในปี 2550 รูปแบบไฟล์ใหม่นี้กลายเป็นส่วนหนึ่งของ Office 2007 และใช้ใน Microsoft Office เวอร์ชันใหม่ด้วย

## ข้อมูลจำเพาะของรูปแบบไฟล์ ##

ไฟล์ที่สร้างด้วยรูปแบบไฟล์ office Open XML คือชุดของไฟล์ XML พร้อมกับไฟล์อื่นๆ ที่มีลิงก์ระหว่างไฟล์ที่เป็นส่วนประกอบทั้งหมด คอลเล็กชันนี้เป็นไฟล์เก็บถาวรแบบบีบอัดที่สามารถแตกไฟล์เพื่อดูเนื้อหาได้ ในการทำเช่นนั้น เพียงเปลี่ยนชื่อนามสกุลไฟล์ PPTM ด้วย zip และแตกไฟล์เพื่อดูเนื้อหา

ส่วนต่อไปนี้ให้ความกระจ่างเกี่ยวกับแต่ละส่วน

### [Content_Types].xml ###

ไฟล์นี้เป็นไฟล์เดียวที่พบที่ระดับฐานเมื่อแตก zip จะแสดงรายการประเภทเนื้อหาสำหรับชิ้นส่วนภายในแพ็คเกจ การอ้างอิงทั้งหมดไปยังไฟล์ XML ที่รวมอยู่ในแพ็คเกจจะถูกอ้างอิงในไฟล์ XML นี้ ต่อไปนี้เป็นประเภทเนื้อหาสำหรับส่วนของสไลด์:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
หากจำเป็นต้องเพิ่มส่วนใหม่ลงในแพ็คเกจ สามารถทำได้โดยการเพิ่มส่วนใหม่และอัปเดตความสัมพันธ์ใดๆ ภายในไฟล์ .rels โปรดทราบว่าสำหรับการเปลี่ยนแปลงดังกล่าว Content_Types.xml จะต้องได้รับการอัปเดตด้วย

### \_rels (โฟลเดอร์) ###

ความสัมพันธ์ระหว่างส่วนอื่นๆ และทรัพยากรภายนอกแพ็คเกจนั้นถูกรักษาไว้โดยส่วนความสัมพันธ์ โฟลเดอร์ความสัมพันธ์มีไฟล์ XML ไฟล์เดียวที่เก็บความสัมพันธ์ระดับแพ็คเกจ ลิงก์ไปยังส่วนสำคัญของไฟล์งานนำเสนอมีอยู่ในไฟล์นี้เป็น URI URI เหล่านี้จะระบุประเภทของความสัมพันธ์ของส่วนสำคัญแต่ละส่วนกับแพ็คเกจ ซึ่งรวมถึงความสัมพันธ์กับเอกสารสำนักงานหลักที่อยู่ใน ppt/presentation.xml และส่วนอื่นๆ ภายใน docProps เป็นคุณสมบัติหลักและคุณสมบัติเพิ่มเติม
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```
แต่ละส่วนของเอกสารที่เป็นแหล่งที่มาของความสัมพันธ์ตั้งแต่หนึ่งความสัมพันธ์ขึ้นไปจะมีส่วนความสัมพันธ์ของตัวเอง โดยแต่ละส่วนของความสัมพันธ์ดังกล่าวจะอยู่ในโฟลเดอร์ย่อย \_rels ของส่วนนั้น และตั้งชื่อโดยการต่อท้าย '.rels' ต่อท้ายชื่อ ส่วนหนึ่ง. ส่วนเนื้อหาหลัก (presentation.xml) มีส่วนความสัมพันธ์ของตัวเอง (presentation.xml.rels) ประกอบด้วยความสัมพันธ์กับส่วนอื่นๆ ของเนื้อหา เช่น slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml รวมถึง URIs สำหรับลิงก์ภายนอก

#### ความสัมพันธ์ที่ชัดเจน ####

สำหรับความสัมพันธ์ที่ชัดเจน ทรัพยากรจะถูกอ้างอิงโดยใช้แอตทริบิวต์ Id ของ a<Relationship> ธาตุ. นั่นคือ Id ในซอร์สแมปโดยตรงกับ Id ของรายการความสัมพันธ์ โดยมีการอ้างอิงอย่างชัดเจนถึงเป้าหมาย

ตัวอย่างเช่น สไลด์อาจมีไฮเปอร์ลิงก์ดังนี้:
```
<a:hlinkClick r:id#"rId2">
```
r:id#"rId2" อ้างอิงถึงความสัมพันธ์ต่อไปนี้ภายในส่วนของความสัมพันธ์สำหรับสไลด์ (slide1.xml.rels)
```
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
```
#### ความสัมพันธ์โดยนัย ####

สำหรับความสัมพันธ์โดยปริยาย ไม่มีการอ้างอิงโดยตรงถึง a `<Relationship> รหัส แทนที่จะเข้าใจการอ้างอิง

### โฟลเดอร์ ppt ###

นี่คือโฟลเดอร์หลักที่มีรายละเอียดทั้งหมดเกี่ยวกับเนื้อหาของงานนำเสนอ ตามค่าเริ่มต้น จะมีโฟลเดอร์ต่อไปนี้:

* \_rels
* ธีม
* สไลด์
* เค้าโครงสไลด์
* สไลด์มาสเตอร์

และไฟล์ xml ต่อไปนี้:

* งานนำเสนอ.xml
* presProps.xml
* tableStyles.xml
* viewProps.xml

## อ้างอิง ##

* [[MS-PPTX] - รูปแบบไฟล์ PPTX](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

