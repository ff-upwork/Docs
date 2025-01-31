{
  "date" : "2020-03-16",
  "keywords" :[ "ไฟล์ PAT", "รูปแบบ", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"เรียนรู้เกี่ยวกับรูปแบบไฟล์ PAT และ API ที่สามารถสร้างและเปิดไฟล์ PAT",
  "title" :"รูปแบบไฟล์ PAT",
  "linktitle" : "PAT",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-10-25"
}

## ไฟล์ PAT คืออะไร??

ไฟล์ที่มีนามสกุล .pat คือไฟล์ CAD ที่ซอฟต์แวร์ AutoCAD ใช้ แอปพลิเคชันที่สามารถเปิดไฟล์ PAT จะใช้รูปแบบการฟักที่เก็บไว้ในไฟล์เหล่านี้เพื่อรับข้อมูลเกี่ยวกับพื้นผิว/การเติมพื้นที่ รูปแบบที่มีอยู่ให้ข้อมูลเกี่ยวกับลักษณะที่ปรากฏของวัสดุกับวัตถุที่วาด ไฟล์ PAT สามารถเปิดได้ในแอปพลิเคชัน เช่น Autodesk AutoCAD, CorelDRAW Graphics Suite และ Ketron Software ไฟล์ PAT สามารถแปลงเป็นรูปแบบภาพต่างๆ เช่น JPG, PNG, BMP เป็นต้น

## รูปแบบไฟล์ PAT

ไฟล์ PAT เขียนในรูปแบบข้อความธรรมดาและสามารถเปิดได้ในโปรแกรมแก้ไขข้อความใดๆ รูปแบบแฮทช์ในไฟล์เหล่านี้เป็นแบบเวกเตอร์และเป็นไปตามไวยากรณ์ที่ระบุไว้ในเอกสารประกอบของ AutoCAD

รูปแบบทั้งหมดเริ่มต้นที่จุด 0,0 รูปแบบจะถูกคำนวณเพื่อให้ครอบคลุมขอบเขตการฟักไข่

### คำจำกัดความของรูปแบบ

คำจำกัดความของรูปแบบทั้งหมดประกอบด้วยฟิลด์ต่อไปนี้:
* นำหน้า '\*'
* ชื่อ - ชื่อต้องไม่มีช่องว่าง เครื่องหมายวรรคตอน วงเล็บ หรือเครื่องหมายทับ
* คำอธิบาย

รูปแบบมาตรฐานสำหรับรูปแบบการฟักคือ `<\*><name> <, คำอธิบาย>`. ชื่อและคำอธิบายถูกคั่นด้วยเครื่องหมายจุลภาค และคำอธิบายต้องมีความยาวบรรทัดไม่เกิน 80 อักขระ รูปแบบการฟักถูกกำหนดหลังจากข้อมูลนี้

### ตัวอย่างรูปแบบการฟักไข่
ต่อไปนี้เป็นตัวอย่างของรูปแบบสี่เหลี่ยมจัตุรัส
```
* square, a square pattern
0,     0,0,   0,1,   1,-1
90,   0,1,   0,1,   1,-1
```
ตัวอย่างอื่นที่แสดงรูปแบบสี่เหลี่ยมด้านขนานมีดังนี้

```
*pgram, parallelogram pattern
0,     0,0,    1,1,                     1,-1
45,   0,0,    0,1.4142,   1.4142,-1.4142
45,   0,1,    0,1.4142,   1.4142,-1.4142
```
## อ้างอิง ##

* [รูปแบบแฮชโดย Autodesk](https://help.autodesk.com/view/ACDLT/2018/ENU/?guid=GUID-A6F2E6FF-1717-44B6-A476-0CA817ADD77E)

