{
  "date" : "2021-07-13",
  "keywords" :[ "CFM", "นามสกุล", "ไฟล์", "รูปแบบ", "ระบบ", "Cold Fusion Markup Language", "ภาษา", "เว็บเพจ CFM", "เครื่องมือ CFML", "CFML" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFM - มาร์กอัปฟิวชั่นเย็น",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ CFM และ API ที่สามารถสร้างและเปิดไฟล์ CFM",
  "linktitle" : "CFM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## ไฟล์ CFM คืออะไร?? ##

หน้าเว็บและไฟล์ที่ใช้ใน **Cold Fusion Markup Language** มีนามสกุลของ CFM และมีชื่อว่าหน้าเว็บ CFM ภาษาสคริปต์การพัฒนาเว็บนี้ทำงานบน Google App Engine, .NET framework และ JVM อาจมีภาษาโปรแกรมหรือรหัสของภาษานั้นๆ เมื่อผู้ใช้เข้าถึงหน้าใด ๆ เว็บเซิร์ฟเวอร์ของ ColdFusion จะดำเนินการ สามารถใช้ CFScript (ที่ใกล้เคียงกับ JavaScript) หรือแท็กเพื่อเขียน CFML สามารถใช้ CFML สำหรับสร้างภาษาอื่นๆ นอกเหนือจาก [HTML](/th/web/html/) เช่น [CSS](/th/web/css/), [JavaScript](/th/web/js/), [XML](/th/web/ xml/) และอื่นๆ

การใช้ภาษาและแท็กนี้ที่สนับสนุนส่วนใหญ่ในการพัฒนาแอปพลิเคชันเว็บแบบไดนามิก ไฟล์สามารถเรียกใช้โดยตรงในเบราว์เซอร์ออนไลน์หากเกิดข้อผิดพลาดใด ๆ ระหว่างการใช้งานออฟไลน์ของแพลตฟอร์มการพัฒนาแอปพลิเคชัน
 

CFML ทำงานในลักษณะที่กำหนดนามสกุลไฟล์เซิร์ฟเวอร์เฉพาะ (.cfc, .cfm) สำหรับการประมวลผลไปยังกลไก CFML หากเอ็นจิ้นใช้ Java จะทำได้โดยใช้เซิร์ฟเล็ต Java กลไกของ CFML จะประมวลผลฟังก์ชันและแท็กเท่านั้น และจะส่งคืนฟังก์ชันและข้อความนอกแท็ก CFML ไปยังเว็บเซิร์ฟเวอร์โดยไม่มีการเปลี่ยนแปลงใดๆ


## ประวัติย่อ ##

ในปี 1995 มันถูกสร้างขึ้นครั้งแรกโดยบริษัทชื่อ Allaire ในปี 2548 Adobe เข้าซื้อกิจการและให้บริการสำหรับการพัฒนา ColdFusion ในขณะนี้ หลายปีที่ผ่านมาได้รับการพัฒนาและปรับปรุงโดยผู้คนและบริษัทมากมาย ในปี 2012 มีการเปิดตัวมูลนิธิชื่อ OpenCFML ต่อมาในปี 2558 อดีต Railo ได้ให้บริการเพื่อปรับปรุงประสิทธิภาพของ CFM และทำให้ทรัพยากรน้อยลงเพื่อการทำงานที่ดีขึ้น การอัปเดตล่าสุดของมันเปิดตัวในปี 2020 ซึ่งประกาศให้ดำเนินการต่อไปจนถึงปี 2028

## รูปแบบไฟล์ CFM ##

โค้ดของไฟล์และเว็บเพจ CFM ส่วนใหญ่ประกอบด้วยแท็กเช่น HTML แต่มีความแตกต่างเล็กน้อย ไฟล์เหล่านี้มีหน้าที่ในการดำเนินการต่างๆ ที่สคริปต์ ColdFusion เปิดใช้งานให้เรียกใช้
* ไฟล์เหล่านี้สามารถเข้าถึงและเรียกใช้ได้โดยตรงทั้งบน Windows และ macOS โดยใช้เบราว์เซอร์ของระบบปฏิบัติการใดก็ได้
* Adobe ColdFusion เป็นแพลตฟอร์มสำหรับการพัฒนาเว็บเพจและแอพพลิเคชั่นแบบไดนามิกบนพีซี
* โปรแกรมแก้ไขข้อความใดๆ เช่น NotePad หรือโปรแกรมแก้ไขข้อความอื่นๆ ในระบบปฏิบัติการสามารถใช้เปิดไฟล์เหล่านี้ได้ เนื่องจากไฟล์เหล่านี้เป็นแบบข้อความ
* เมื่อเปิดไฟล์ CFM ใดๆ ในโปรแกรมแก้ไขข้อความ ไฟล์จะแสดงโค้ดที่ประกอบด้วยแท็กและสคริปต์ที่ไม่มีใครเข้าใจเว้นแต่เขาจะเป็นนักพัฒนาเว็บ

## ตัวอย่างการใช้ CFM ##

ต่อไปนี้แสดงไฟล์ CFM ตัวอย่างการใช้งานอย่างง่าย

### เอกสาร CFM ###

```html
<!--- temperature.cfc --->
<cfcomponent>
  <cffunction name="FtoC" access="public" returntype="numeric">
    <cfargument name="fahrenheit" required="yes" type="numeric" />
    <cfset answer= (fahrenheit - 32)*100/180 />
    <cfreturn answer />
  </cffunction>
</cfcomponent>
<!--- test.cfm --->
<cfset fDegrees = 212 />
<cfinvoke component="temperature" method="FtoC" returnvariable="result">
  <cfinvokeargument name="fahrenheit" value="#fDegrees#" />
</cfinvoke>
<cfoutput>#fDegrees#&deg;F = #result#&deg;C</cfoutput> <br />
```

## อ้างอิง ##

- [CFM - Wikipedia](https://en.wikipedia.org/wiki/ColdFusion_Markup_Language)

