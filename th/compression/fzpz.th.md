{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ FZPZ - ไฟล์ Fritzing Part",
  "description":"เรียนรู้เกี่ยวกับไฟล์ FZPZ และ API ที่สามารถสร้างและเปิดไฟล์ FZPZ ได้",
  "linktitle" : "FZPZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-20"
}

## ไฟล์ FZPZ คืออะไร??

ไฟล์ FZPZ เป็นส่วนประกอบ/ชิ้นส่วนที่ใช้ในการออกแบบวงจรอิเล็กทรอนิกส์ที่สร้างขึ้นด้วยการสร้างต้นแบบวงจรและแอปพลิเคชันการออกแบบ **Fritzing** เป็นไฟล์เก็บถาวรแบบบีบอัดที่มีไฟล์ [FZP](/th/cad/fzp/) และรูปภาพ [SVG](/th/page-description-language/svg/) สี่ภาพซึ่งอธิบายส่วนโดยรวมใน Fritzing ข้อดีของการใช้ไฟล์เหล่านี้คือผู้ใช้สามารถแบ่งปันไฟล์ FZPZ กับแต่ละไฟล์ได้จากมุมมองของการใช้ซ้ำ การแบ่งปันชิ้นส่วน FZPZ ช่วยในการรวมชิ้นส่วนวงจรเพื่อสร้างการออกแบบ PCB ขนาดใหญ่ขึ้นอย่างรวดเร็ว

## รูปแบบไฟล์ FZPZ - ข้อมูลเพิ่มเติม

ไฟล์ FZPZ จะถูกบันทึกลงดิสก์เป็นไฟล์บีบอัด [ZIP](/th/compression/zip/) คุณสามารถเปลี่ยนชื่อนามสกุลจาก .fzpz เป็น .zip และใช้ยูทิลิตี้คลายการบีบอัดมาตรฐานใดๆ เช่น WinZIP เพื่อแยกไฟล์ออกจากไฟล์เก็บถาวร

### ข้อมูลโครงสร้างไฟล์ FZPZ

ตามที่กล่าวไว้ ไฟล์ FZPZ เป็นไฟล์เก็บถาวรที่มีไฟล์หลายไฟล์สำหรับเป็นตัวแทนของชิ้นส่วนที่ใช้ในแผงวงจรพิมพ์ FZPZ มีไฟล์ต่อไปนี้:

* `ไฟล์ SVG สี่ไฟล์` - ที่แสดงถึงชิ้นส่วนของเขียงหั่นขนม แผนผัง PCB และภาพไอคอน
* `ไฟล์ FZP` - ไฟล์ XML ที่มีข้อมูลเกี่ยวกับคุณสมบัติของชิ้นส่วน ตัวเชื่อมต่อ และบัส

ไฟล์มักจะมีชื่อดังต่อไปนี้

* part.file.fzp
* svg.breadboard.file.svg
* svg.icon.file.svg
* svg.pbc.file.svg
* svg.schematic.file.svg

## อ้างอิง ##

* [ส่วนใหม่พร้อมส่วนขยาย fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

