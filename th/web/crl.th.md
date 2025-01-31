{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ CRL - รายการเพิกถอนใบรับรอง",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ CRL และ API ที่สามารถสร้างและเปิดไฟล์ CRL",
  "linktitle" : "CRL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-01"
}

## ไฟล์ CRL คืออะไร??

ไฟล์ CRL (รายการเพิกถอนใบรับรอง) เป็นบัญชีดำของใบรับรองดิจิทัล X.509 ที่ผู้ออกใบรับรอง (CA) เพิกถอนก่อนวันที่เพิกถอนที่กำหนด ประกอบด้วยข้อมูลเกี่ยวกับปัญหาและวันที่เพิกถอนซึ่งช่วยให้ผู้ดูแลระบบความปลอดภัยสามารถบล็อกใบรับรองดิจิทัลที่ได้รับผลกระทบได้ CRL ไม่รวมใบรับรองที่หมดอายุ เนื่องจากจุดประสงค์หลักคือเพื่อแจ้งเกี่ยวกับใบรับรองที่ไม่น่าเชื่อถือและไม่ถูกต้อง

แอปพลิเคชันที่สามารถ **เปิดไฟล์ CRL** ได้แก่ OpenSSL, Microsoft IIS Server และ Citrix NetScaler

## รูปแบบไฟล์ CRL - ข้อมูลเพิ่มเติม

ไฟล์ CRL มีข้อมูลในมาตรฐาน X.509 ซึ่งกำหนดความหมายสำหรับการแบ่งปันข้อมูลคีย์สาธารณะ ข้อมูลอื่นๆ ที่อยู่ในไฟล์ CRL อาจรวมถึงขีดจำกัดเวลาที่ใบรับรองถูกเพิกถอน เหตุผลในการเพิกถอน หมายเลขซีเรียลของใบรับรองที่ถูกเพิกถอน และการประทับเวลา


### เหตุผลหลักในการเพิ่มใบรับรองใน CRL

อาจมีสาเหตุหลายประการที่ทำให้ใบรับรองเว็บไซต์ของคุณถูกเพิกถอนและเพิ่มลงใน CRL บางคนอาจจะเป็น;

1. คีย์ส่วนตัวของใบรับรองของคุณถูกบุกรุก
1. ใบรับรองของคุณไม่ถูกต้องหรือออกโดย CA ที่ไม่ถูกต้อง
1. รายละเอียดองค์กรที่เกี่ยวข้องกับใบรับรองมีการเปลี่ยนแปลงและ CA ออกใบรับรองใหม่
1. เหตุอื่นใดที่ไม่อาจหลีกเลี่ยงได้ซึ่งใบรับรองถูกเพิกถอน

## อ้างอิง

* [สถาบันมาตรฐานและเทคโนโลยีแห่งชาติ (NIST)](https://csrc.nist.gov/glossary/term/CRL)
* [Internet Engineering Task Force's (IETF) RFC 5280](https://tools.ietf.org/html/rfc5280)
* [รายการเพิกถอนใบรับรอง](https://en.wikipedia.org/wiki/Certificate_revocation_list)

