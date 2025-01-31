{
  "date" : "2019-10-11",
  "keywords" :[ "ma", "ma file", "ma file format", "file format", "3d", "ma file download", ".ma file", ".ma"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ MA และ API ที่สามารถเปิดและสร้างไฟล์ MA",
  "title" :"รูปแบบไฟล์ MA",
  "linktitle" : "MA",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-06-04"
}

## ไฟล์ MA คืออะไร??

ไฟล์ที่มีนามสกุล .ma เป็นไฟล์โปรเจ็กต์ 3 มิติที่สร้างด้วยแอปพลิเคชัน Autodesk Maya ประกอบด้วยรายการคำสั่งที่เป็นข้อความจำนวนมากเพื่อระบุข้อมูลเกี่ยวกับไฟล์ ไฟล์ **.ma** สามารถเปิดและแก้ไขได้ในโปรแกรมแก้ไขข้อความใดๆ เพื่อแก้ไขปัญหาเกี่ยวกับคำสั่งในกรณีที่ไฟล์เสียหาย ไฟล์เหล่านี้มีข้อมูลสำหรับกำหนดข้อมูลฉาก 3 มิติ เช่น รูปทรงเรขาคณิต การจัดแสง ภาพเคลื่อนไหว และการเรนเดอร์

## รูปแบบไฟล์ MA

ไฟล์ MA จะถูกบันทึกลงในดิสก์ในรูปแบบข้อความ ASCII ซึ่งแตกต่างจากไฟล์ MB ที่บันทึกในรูปแบบไฟล์ไบนารีลงในดิสก์ ข้อมูลอ้างอิงโดยละเอียดสำหรับรูปแบบไฟล์ MA มีอยู่ใน [เอกสาร Autodesk Maya](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001) และสามารถอ้างอิงได้ เพื่อการอ้างอิงของนักพัฒนา

### ส่วนหัวของไฟล์ MA

ส่วนหัวของไฟล์ MA เริ่มต้นด้วยส่วนของความคิดเห็นที่ให้ข้อมูลการสร้างไฟล์และวันที่แก้ไข โปรแกรมอ่านไฟล์ Maya ไม่สนใจบล็อกนี้เนื่องจากใช้เพื่อจุดประสงค์ในการให้ข้อมูลเท่านั้น ส่วนหัวต้องขึ้นต้นด้วยอักขระหกตัวแรกเป็น "//Maya"

ส่วนหัวของไฟล์ ASCII มีลักษณะดังนี้

```
//Maya ASCII 1.0 scene
//Name: solstice.ma
//Last modified: Sun, Dec 21, 97 10:18:26 AM
```
### อ้างอิงไฟล์

ส่วนการอ้างอิงไฟล์ของไฟล์ .ma มีข้อมูลเกี่ยวกับไฟล์ Maya อื่นๆ ทั้งหมดที่ถูกอ้างถึงในไฟล์นี้ ไฟล์อ้างอิงแต่ละไฟล์สามารถอ่านได้โดยใช้คำสั่งไฟล์เดียวที่อยู่ในไฟล์เดียวกัน ไวยากรณ์ของคำสั่งไฟล์เมื่อใช้สำหรับการอ้างอิงคือ:

```
file -r -rpr prefixString fileName;
```
หรือ

```
file -r -ns nameSpace fileName
```
นี่คือตัวอย่างสตริง

```
file -r -rpr "solar" "/u/sally/work/solar.ma";
```
ตัวอย่างนี้แสดงให้เห็นว่าวัตถุดวงอาทิตย์ที่อยู่ในไฟล์ `solar` จะสามารถเข้าถึงได้ในไฟล์นี้โดยใช้ชื่อ "solar_sun"

### ความต้องการ

ส่วนข้อกำหนดของไฟล์ .ma ประกอบด้วยชุดคำสั่งที่จำเป็นและบอกข้อมูลเดือนพฤษภาคม เช่น ข้อมูลเวอร์ชันและปลั๊กอินที่จำเป็นสำหรับการอ่านไฟล์ ตัวอย่างส่วนข้อกำหนดมีดังนี้

```
requires maya "2.0";
requires specialPlugIn "1.2";
```


ส่วนถัดไประบุข้อกำหนด ประกอบด้วยชุดคำสั่งที่จำเป็น ส่วนนี้ของไฟล์จะบอก Maya ว่าต้องใช้ซอฟต์แวร์ใดในการโหลดไฟล์อย่างถูกต้อง โดยเฉพาะอย่างยิ่ง Maya รุ่นใดและปลั๊กอินใด

## ดาวน์โหลดไฟล์ MA
การค้นหาและดาวน์โหลดไฟล์ MA ของโมเดล 3 มิติค่อนข้างยาก ดังนั้น คุณสามารถดาวน์โหลดไฟล์ MA ตัวอย่างได้จากที่นี่:

- [Sample.ma](../sample.ma)


## อ้างอิง

* [การจัดระเบียบไฟล์ Maya ASCII - Autodesk](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001)

