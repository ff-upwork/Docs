---
date: 2021-07-05
keywords: ssp, .ssp, รูปแบบไฟล์ ssp, วิธีเปิดไฟล์ ssp, Scala Server Page,
ผู้เขียน:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SSP - รูปแบบไฟล์หน้าเซิร์ฟเวอร์ Scala,
linktitle: SSP
description: "เรียนรู้เกี่ยวกับรูปแบบไฟล์ SSP และ API ที่สามารถสร้างและเปิดไฟล์ SSP ได้"
menu:
  docs:
    identifier: "web-ssp"
    parent: "web"
lastmod: 2021-09-30
---

## ไฟล์ SSP คืออะไร??

ไฟล์ที่มีนามสกุล .ssp คือเว็บเพจที่สร้างด้วยโค้ด Scala สำหรับนิพจน์แทน HTML ธรรมดาเท่านั้น ทำหน้าที่เป็นสคริปต์ฝั่งเซิร์ฟเวอร์โดยใช้ HTML และ Scala ร่วมกัน ไฟล์เหล่านี้อยู่บนเซิร์ฟเวอร์และใช้เพื่อสร้างเว็บเพจแบบคงที่เพื่อให้บริการแก่ผู้ใช้ Scala เองเป็นภาษาการเขียนโปรแกรมสำหรับวัตถุประสงค์ทั่วไป ซึ่งไวยากรณ์เป็นที่คุ้นเคยสำหรับผู้ใช้ที่ทำงานกับ Velocity, JSP หรือ Erb ไฟล์ SSP สามารถวิเคราะห์และประเมินได้โดยใช้ [Scalate](https://scalate.github.io/scalate/) ซึ่งเป็นเครื่องมือเทมเพลตที่ใช้ Scala สำหรับสร้างข้อความและมาร์กอัป

## รูปแบบไฟล์ SSP - ข้อมูลเพิ่มเติม

ไฟล์ SSP จะถูกบันทึกเป็นไฟล์ข้อความธรรมดาและสามารถประเมินได้โดยใช้ Scalate เทมเพลต Ssp ประกอบด้วยข้อความล้วนซึ่งมักจะเป็นเอกสาร HTML มีแท็ก Ssp ฝังอยู่ในนั้นซึ่งทำให้เอ็นจิ้นการเรนเดอร์แสดงส่วนต่าง ๆ ของเอกสารแบบไดนามิก แท็กเริ่มต้นและสิ้นสุดด้วยลำดับ <% ... %> และ ${ ... } และสิ่งที่อยู่นอกเหนือเหล่านี้ถือเป็นข้อความตามตัวอักษร

### ตัวอย่าง SSP

ตัวอย่างต่อไปนี้แสดงโค้ด SSP และเอาต์พุตเมื่อแสดงผลโดยเอ็นจินการเรนเดอร์

```PHP
<p>
  <%= List("hi", "there", "reader!").mkString(" ") %>
  ${ "yo "+(3+4) }
</p>
```
ผลลัพธ์มีดังต่อไปนี้
```
<p>
  hi there reader!
  yo 7
</p>
```

## อ้างอิง

- [ข้อมูลอ้างอิง SSP](https://scalate.github.io/scalate/documentation/ssp-reference.html)
