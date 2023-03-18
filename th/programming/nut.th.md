{
  "date" : "2021-09-23", 
  "keywords" :[ "NUT", "ไฟล์", "นามสกุล", "รูปแบบไฟล์", "ภาษา NUT рrоgrаmming", "คู่มือการเขียนโปรแกรม", "ตัวอย่าง NUT", "รูปแบบไฟล์ NUT", "ภาษากระรอก", "ไฟล์นามสกุล .nut ", "ไฟล์ NUT" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NUT - ไฟล์ภาษากระรอก",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ NUT และ API ที่สามารถสร้างและเปิดไฟล์ NUT",
  "linktitle" : "NUT",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-23"
}

## ไฟล์ NUT คืออะไร??

NUT หมายถึงไฟล์ NUT Open Container Format รูปแบบไฟล์ NUT นี้เป็นของภาษาโปรแกรมที่เรียกว่า Squirrel เป็นภาษาการเขียนโปรแกรมเชิงวัตถุระดับสูงและจำเป็นซึ่งส่วนใหญ่ใช้ในระบบฝังตัวและวิดีโอเกม

ภาษากระรอกถือเป็นภาษาสคริปต์ที่มีน้ำหนักเบาซึ่งสามารถปรับเปลี่ยนตามขนาดและแบนด์วิธได้อย่างง่ายดาย มันเกี่ยวข้องกับข้อได้เปรียบของการนับการอ้างอิงอัตโนมัติและการจัดการขยะในหน่วยความจำ

ไวยากรณ์ของภาษากระรอกดึงดูดนักพัฒนาเนื่องจากเป็นภาษา C และเกี่ยวข้องกับคุณลักษณะของภาษาสคริปต์ แต่ถึงกระนั้น มันก็มีข้อได้เปรียบน้อยกว่าเมื่อเทียบกับภาษาโปรแกรมอื่นๆ ที่ได้รับความนิยมมากกว่าสำหรับจุดประสงค์นี้



## ประวัติย่อ ##

ได้รับการออกแบบโดย Alberto Demichelis ในปี 2003 อย่างไรก็ตาม เวอร์ชันเสถียรของภาษานี้เปิดตัวในปี 2016 ได้รับการออกแบบภายใต้ลิขสิทธิ์ของ zlib/libpng ในปี 2010 ใบอนุญาตถูกเปลี่ยนและโอนไปยัง MIT ภาษานี้ถือเป็นเวอร์ชันที่ได้รับแรงบันดาลใจจาก [LUA](/th/programming/lua/) (ภาษาการเขียนโปรแกรม) มีรายการคำแนะนำสำหรับภาษาเดิมบนเว็บไซต์ที่ออกแบบโดย Alberto เพื่อให้ได้เปรียบยิ่งขึ้น


## ข้อมูลทางเทคนิค ##

คุณลักษณะและข้อกำหนดของภาษากระรอกมีหลายประการ อำนวยความสะดวกในการพิมพ์ไดนามิก คุณสมบัติของการมอบหมาย การใช้คลาสและอินเทอร์เฟซต่างๆ ไวยากรณ์ของภาษานี้มีความคล้ายคลึงกับไวยากรณ์ของภาษาซี แอปพลิเคชัน เช่น Enduro/X (เซิร์ฟเวอร์แอปพลิเคชันคลัสเตอร์) ใช้ภาษานี้ เนื่องจาก Squirrel ใช้สำหรับวิดีโอเกมเช่นกัน บางส่วนเช่น OpenTTD, GTA IV เป็นต้น

เวอร์ชันเสถียรของภาษาคือ 3.0.7 ชุดเครื่องมือที่เรียกว่า MirthKit ใช้ภาษาการเขียนโปรแกรม Squirrel เพื่อจัดหาโอเพ่นซอร์สและข้ามแพลตฟอร์มสำหรับเกมสองมิติ ธรรมชาติของภาษานี้เป็นแบบไดนามิกและคุณสมบัติส่วนใหญ่คล้ายกับ [Python](/th/programming/py/), LUA และอื่นๆ นอกจากนี้ยังเกี่ยวข้องกับการใช้งาน VM ที่ลงทะเบียน ประสิทธิภาพของ Squirrel นั้นช้ากว่า LUA

นอกจากนี้ยังมีไฟล์นามสกุล ".nut" อีกประเภทหนึ่งซึ่งเป็นเหตุผลที่คุณควรดูขนาดของไฟล์เพื่อดูว่าคุณมีไฟล์ NUT ใด ไฟล์ NUT ของสคริปต์ Squirrel ส่วนใหญ่มีขนาดเล็กกว่า 1 MB ในขณะที่ไฟล์ NUT ของวิดีโอมักจะมีขนาดใหญ่กว่า 1 MB


## ตัวอย่างรูปแบบไฟล์ NUT ##

```
function factorial(x)
  {
    if (x == 0) {
      return 1;
}
    else {
      return x * factorial(x-1);
}
  }
```

```

class BaseVector {
    constructor(...)
    {
      if(vargv.len() >= 3) {
        x = vargv[0];
        y = vargv[1];
        z = vargv[2];
  }
}
    x = 0;
    y = 0;
    z = 0;
  }

  class Vector3 extends BaseVector {
    function _add(other)
    {
      if(other instanceof ::Vector3)
        return ::Vector3(x+other.x,y+other.y,z+other.z);
      else
        throw "wrong parameter";
}
    function Print()
    {
      ::print(x+","+y+","+z+"\n");
}
  }

  local v0 = Vector3(1,2,3)
  local v1 = Vector3(11,12,13)
  local v2 = v0 + v1;
  v2.Print();

```

## อ้างอิง ##

* [NUT - โดย Wikipedia](https://en.wikipedia.org/wiki/Squirrel_(programming_language))


