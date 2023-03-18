{
  "date" : "2021-06-24",
  "keywords" :[ "ไฟล์ค้างคาว", "ไฟล์ค้างคาวคืออะไร", "ไฟล์", "ตัวอย่างไฟล์ค้างคาว", "ส่วนขยาย", "รูปแบบ" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ BAT และ API ที่สามารถสร้างและเปิดไฟล์ BAT",
  "title" :"BAT - รูปแบบไฟล์แบทช์",
  "linktitle" : "BAT",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-24"
}

## ไฟล์ BAT คืออะไร??
ไฟล์ BAT เรียกว่าไฟล์แบตช์ที่ทำงานกับ DOS และ Windows ทุกรุ่นภายใต้ cmd.exe ประกอบด้วยชุดคำสั่งบรรทัดในข้อความล้วนที่จะดำเนินการโดยล่ามบรรทัดคำสั่งเพื่อทำงานต่างๆ เช่น การเรียกใช้ยูทิลิตี้การบำรุงรักษาภายใน Windows หรือการเริ่มโปรแกรมทั่วไป ไฟล์แบตช์อาจรวมคำสั่งใดๆ ที่ล่ามสามารถยอมรับได้แบบโต้ตอบ และใช้โครงสร้างของรหัสที่เปิดใช้งานการแยกสาขาตามเงื่อนไขและการวนซ้ำตามที่เขียนไว้ในแบตช์ไฟล์
## รูปแบบไฟล์ BAT
รูปแบบไฟล์ BAT เป็นเพียงสคริปต์ที่รวมไว้เพื่อทำให้ลำดับคำสั่งเป็นแบบอัตโนมัติซึ่งมีลักษณะซ้ำๆ คำว่า "แบทช์" ใช้สำหรับการประมวลผลแบบแบทช์ ซึ่งถือได้ว่าเป็น "การดำเนินการแบบไม่โต้ตอบ" ดังนั้นไฟล์แบทช์จึงไม่สามารถประมวลผลชุดข้อมูลหลายชุดได้ ในระบบปฏิบัติการดิสก์ (DOS) แบบเก่า ไฟล์แบตช์ถูกเรียกใช้ภายใต้อินเทอร์เฟซบรรทัดคำสั่งโดยพิมพ์ชื่อไฟล์และนามสกุล .bat ระบบปฏิบัติการที่ใช้ส่วนต่อประสานกราฟิกของ Microsoft รุ่นก่อนหน้า เช่น Microsoft Windows นั้นขึ้นอยู่กับ DOS ผู้ใช้ต้องใช้ DOS เพื่อดำเนินการทั่วไป เช่น ซ่อมแซม เพิ่มประสิทธิภาพ หรือติดตั้ง Windows ใหม่ ต่อมา Microsoft ได้เปิดตัว Windows NT ซึ่งไม่ขึ้นอยู่กับระบบปฏิบัติการ DOS ดังนั้น ไฟล์แบตช์สามารถเรียกใช้ได้โดยใช้ Command Prompt หรือ **cmd.exe** ในระบบปฏิบัติการ Microsoft สมัยใหม่
### พารามิเตอร์แบตช์ไฟล์
พรอมต์คำสั่งรองรับตัวแปรพิเศษจำนวนหนึ่ง เช่น **%0, %1 ถึง %9** เพื่ออ้างถึงชื่อและเส้นทางของชุดงานและพารามิเตอร์การเรียกเก้าตัวจากภายในงานชุดงาน พารามิเตอร์ที่ไม่มีอยู่จะถูกแทนที่ด้วยสตริงที่มีความยาวเป็นศูนย์ แม้ว่าจะสามารถใช้คล้ายกับตัวแปรสภาพแวดล้อม แต่จะไม่บันทึกไว้ในสภาพแวดล้อม Microsoft และ IBM อ้างถึงตัวแปรเหล่านี้เป็นพารามิเตอร์แทนที่ ในขณะที่ Novell, Digital Research และ Caldera แนะนำคำว่าตัวแปรแทนที่สำหรับตัวแปรเหล่านั้น

ต่อไปนี้เป็นคำสั่งไฟล์แบทช์ที่มีประโยชน์:
| คำสั่ง | คำอธิบาย |
------|------------|
| เวอร์ | คำสั่งแบทช์นี้แสดงเวอร์ชันของ MS-DOS ที่คุณกำลังใช้ |
|ก.บ.ภ.| นี่คือคำสั่งแบตช์ที่เชื่อมโยงส่วนขยายกับประเภทไฟล์ (FTYPE) แสดงการเชื่อมโยงที่มีอยู่ หรือลบการเชื่อมโยง |
|ซีดี| คำสั่งแบทช์นี้ช่วยในการเปลี่ยนแปลงไดเร็กทอรีอื่น หรือแสดงไดเร็กทอรีปัจจุบัน |
|ซีแอลเอส| คำสั่งแบทช์นี้จะล้างหน้าจอ |
|คัดลอก| คำสั่งแบตช์นี้ใช้สำหรับคัดลอกไฟล์จากที่หนึ่งไปยังอีกที่หนึ่ง |
|เดล| คำสั่งแบทช์นี้จะลบไฟล์ ไม่ใช่ไดเร็กทอรี |
|DIR| คำสั่งแบทช์นี้แสดงรายการเนื้อหาของไดเร็กทอรี |
|วันที่| คำสั่งแบทช์นี้ช่วยในการค้นหาวันที่ของระบบ |
|เอคโค่| คำสั่งแบทช์นี้แสดงข้อความหรือเปิดหรือปิดคำสั่งสะท้อน |
|ทางออก| คำสั่งแบทช์นี้ออกจากคอนโซล DOS |
|นพ.| คำสั่งแบทช์นี้สร้างไดเร็กทอรีใหม่ในตำแหน่งปัจจุบัน |
|ย้าย| คำสั่งแบทช์นี้จะย้ายไฟล์หรือไดเร็กทอรีระหว่างไดเร็กทอรี |
|เส้นทาง| คำสั่งแบทช์นี้แสดงหรือตั้งค่าตัวแปรพาธ |
|หยุดชั่วคราว| คำสั่งแบทช์นี้พร้อมต์ผู้ใช้และรอให้ป้อนบรรทัดอินพุต |
|พรอมต์| คำสั่งแบทช์นี้สามารถใช้เพื่อเปลี่ยนหรือรีเซ็ตพรอมต์ cmd.exe |
|RD| คำสั่งแบตช์นี้ลบไดเร็กทอรี แต่ไดเร็กทอรีต้องว่างเปล่าก่อนจึงจะสามารถลบไดเร็กทอรีได้ |
|เรน| เปลี่ยนชื่อไฟล์และไดเร็กทอรี |
|REM| คำสั่งแบตช์นี้ใช้สำหรับหมายเหตุในแบตช์ไฟล์ ป้องกันไม่ให้ดำเนินการเนื้อหาของหมายเหตุ |
|เริ่ม| คำสั่งแบทช์นี้เริ่มโปรแกรมในหน้าต่างใหม่หรือเปิดเอกสาร |
|เวลา| ชุดคำสั่งนี้ตั้งค่าหรือแสดงเวลา |
|ประเภท| คำสั่งแบตช์นี้พิมพ์เนื้อหาของไฟล์ไปยังเอาต์พุต |
|VOL| คำสั่งแบทช์นี้แสดงป้ายกำกับโวลุ่ม |
|ATTRIB| แสดงหรือตั้งค่าแอตทริบิวต์ของไฟล์ในไดเร็กทอรี curret |
|CHKDSK| คำสั่งแบทช์นี้จะตรวจสอบดิสก์เพื่อหาปัญหาใดๆ |
|ทางเลือก| คำสั่งชุดนี้มีรายการตัวเลือกสำหรับผู้ใช้ |
|CMD| คำสั่งแบทช์นี้เรียกใช้อินสแตนซ์ของพรอมต์คำสั่งอื่น |
|คอมพ์| คำสั่งแบทช์นี้เปรียบเทียบ 2 ไฟล์ตามขนาดไฟล์ |
|แปลง| คำสั่งแบทช์นี้แปลงวอลุ่มจากระบบไฟล์ FAT16 หรือ FAT32 เป็นระบบไฟล์ NTFS |
|คำถามเกี่ยวกับไดรเวอร์| คำสั่งแบทช์นี้แสดงไดรเวอร์อุปกรณ์ที่ติดตั้งทั้งหมดและคุณสมบัติต่างๆ |
|ขยาย| คำสั่งแบทช์นี้จะแตกไฟล์จากไฟล์ .cab cabinet ที่ถูกบีบอัด |
|ค้นหา| คำสั่งแบทช์นี้ค้นหาสตริงในไฟล์หรืออินพุต โดยส่งออกบรรทัดที่ตรงกัน |
|รูปแบบ| คำสั่งแบทช์นี้จัดรูปแบบดิสก์ให้ใช้ระบบไฟล์ที่รองรับ Windows เช่น FAT, FAT32 หรือ NTFS ดังนั้นจึงเขียนทับเนื้อหาก่อนหน้าของดิสก์ |
|ช่วยเหลือ| คำสั่งแบทช์นี้แสดงรายการคำสั่งที่มาจาก Windows |
|IPCONFIG| คำสั่งแบทช์นี้แสดงการกำหนดค่า IP ของ Windows แสดงการกำหนดค่าตามการเชื่อมต่อและชื่อของการเชื่อมต่อนั้น |
|ฉลาก| คำสั่งแบทช์นี้จะเพิ่ม ตั้งค่า หรือลบป้ายชื่อดิสก์ |
|เพิ่มเติม| คำสั่งแบทช์นี้แสดงเนื้อหาของไฟล์ทีละหนึ่งหน้าจอ |
|เน็ต| ให้บริการเครือข่ายต่างๆ ขึ้นอยู่กับคำสั่งที่ใช้ |
|ปิง| คำสั่งแบทช์นี้จะส่งแพ็กเก็ต "echo" ของ ICMP/IP ผ่านเครือข่ายไปยังที่อยู่ที่กำหนด |
|ปิดเครื่อง| คำสั่งแบทช์นี้ปิดคอมพิวเตอร์หรือล็อกออฟผู้ใช้ปัจจุบัน |
|เรียง| คำสั่งแบตช์นี้ใช้อินพุตจากไฟล์ต้นฉบับและเรียงลำดับเนื้อหาตามตัวอักษร จาก A ถึง Z หรือ Z ถึง A ซึ่งจะพิมพ์เอาต์พุตบนคอนโซล |
|ย่อย| คำสั่งแบทช์นี้กำหนดอักษรระบุไดรฟ์ให้กับโฟลเดอร์ในเครื่อง แสดงการมอบหมายปัจจุบัน หรือลบการมอบหมาย |
|ระบบ| คำสั่งแบทช์นี้แสดงการกำหนดค่าของคอมพิวเตอร์และระบบปฏิบัติการ |
|งานทักษะ| คำสั่งแบทช์นี้สิ้นสุดงานตั้งแต่หนึ่งงานขึ้นไป |
|รายการงาน| คำสั่งแบทช์นี้แสดงรายการงาน รวมถึงชื่องานและรหัสกระบวนการ (PID) |
|XCOPY| คำสั่งแบทช์นี้คัดลอกไฟล์และไดเร็กทอรีด้วยวิธีขั้นสูง |
|ต้นไม้| คำสั่งแบทช์นี้แสดงแผนผังของไดเร็กทอรีย่อยทั้งหมดของไดเร็กทอรีปัจจุบันในระดับการเรียกซ้ำหรือความลึกใดๆ |
|FC |คำสั่งแบทช์นี้แสดงรายการความแตกต่างจริงระหว่างสองไฟล์ |
|DISKPART |คำสั่งแบทช์นี้แสดงและกำหนดค่าคุณสมบัติของพาร์ติชั่นดิสก์ |
|TITLE |คำสั่งแบทช์นี้ตั้งชื่อเรื่องที่แสดงในหน้าต่างคอนโซล |
|SET | แสดงรายการตัวแปรสภาพแวดล้อมในระบบปัจจุบัน |

## ตัวอย่างไฟล์ BAT
สคริปต์ชุดมักจะบันทึกเป็นไฟล์ข้อความอย่างง่าย มีคำสั่งที่ได้รับการดำเนินการตามลำดับ ไฟล์เหล่านี้บันทึกด้วยนามสกุล .bat; รู้จักและดำเนินการโดยใช้ซอฟต์แวร์ **Command Interpreter** ซอฟต์แวร์นี้มีอยู่ใน Microsoft Windows ด้วยชื่อ **cmd.exe**

นี่คือตัวอย่าง Batch Script ซึ่งจะลบไฟล์ทั้งหมดในไดเร็กทอรีปัจจุบัน:
```
:: Deletes All files in the Current Directory With Prompts and Warnings
::(Hidden, System, and Read-Only Files are Not Affected)
:: @ECHO OFF
DEL . DR
```


## อ้างอิง

* [ชุดสคริปต์ - คู่มือฉบับย่อ](https://www.tutorialspoint.com/batch_script/batch_script_quick_guide.htm)
* [ไฟล์แบทช์ - โดย Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)
