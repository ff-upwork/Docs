{
  "date" : "2019-10-11",
  "keywords" :[ "vb", "ไฟล์", "นามสกุล", "รูปแบบไฟล์", "Visual Basic", "คู่มือการเขียนโปรแกรม" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VB - ไฟล์รหัส Visual Basic",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ VB และ API ที่สามารถสร้างและเปิดไฟล์ VB",
  "linktitle" : "VB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## ไฟล์ VB คืออะไร??

ไฟล์ VB เป็นไฟล์ซอร์สโค้ดที่สร้างด้วยภาษา Visual Basic ซึ่งสร้างโดย Microsoft สำหรับการพัฒนาแอปพลิเคชัน .NET อีกภาษาที่คล้ายกันซึ่งมีไวยากรณ์ต่างกันคือ C# ซึ่งไฟล์จะถูกบันทึกด้วยนามสกุลไฟล์ [.CS](/th/programming/cs/) รูปแบบไฟล์จัดเตรียมภาษาการเขียนโปรแกรมระดับต่ำสำหรับการเขียนโค้ดที่คอมไพล์เพื่อสร้างไฟล์เอาต์พุตสุดท้ายในรูปแบบของ EXE หรือ DLL สิ่งเหล่านี้สามารถสร้างและคอมไพล์ด้วย Microsoft Visual Studio นอกจากนี้ยังสามารถใช้ Microsoft Visual Studio Express เพื่อสร้างและอัปเดตไฟล์ดังกล่าวซึ่งเป็น IDE ฟรี โครงการ Visual Studio อย่างง่าย [โซลูชัน](/th/programming/sln/) ที่สร้างขึ้นด้วยภาษา VB สามารถประกอบด้วยไฟล์ดังกล่าวตั้งแต่หนึ่งไฟล์ขึ้นไป ไฟล์ที่ทำเครื่องหมายให้รวมอยู่ในการคอมไพล์จะแสดงอยู่ในไฟล์ [CSPROJ](/th/programming/csproj/) ซึ่งเป็นส่วนหนึ่งของโปรเจ็กต์และบอกให้คอมไพเลอร์ใช้ไฟล์ที่ทำเครื่องหมาย

## รูปแบบไฟล์ VB - ข้อมูลเพิ่มเติม

ไฟล์ VB เป็นรูปแบบไฟล์ข้อความที่สามารถเปิดได้ในโปรแกรมแก้ไขข้อความเพื่อแก้ไข อย่างไรก็ตาม เมื่อเปิดใน IDE ที่รองรับด้วยการเน้นไวยากรณ์ที่เหมาะสม โค้ดจะอ่านและจัดเรียงได้ง่าย ไฟล์ VB อย่างง่ายประกอบด้วย:

* การประกาศเนมสเปซ - สำหรับการอ้างอิงถึงฟังก์ชันเฉพาะที่กำหนดโดยเนมสเปซเฉพาะนั้น
* การประกาศตัวแปร - เพื่อประกาศตัวแปรระดับคลาสสำหรับการใช้งานเฉพาะ
* การประกาศเมธอด - เพื่อประกาศการประกาศเมธอดสำหรับการทำงานเฉพาะ

## ตัวอย่างรูปแบบไฟล์ VB

```
Imports System
Module Module1
   'This program will display Hello World
   Sub Main()
      Console.WriteLine("Hello World")
      Console.ReadKey()
   End Sub
End Module
```



