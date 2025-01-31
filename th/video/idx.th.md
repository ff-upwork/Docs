{
  "date" : "2022-07-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IDX - ตัวแปลงสัญญาณวิดีโอประสิทธิภาพสูง",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ IDX และ API ที่สามารถสร้างและเปิดไฟล์ IDX",
  "linktitle" : "IDX",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-12"
}

## ไฟล์ IDX คืออะไร??

ไฟล์ IDX คือไฟล์ดัชนีคำบรรยายที่ชี้ไปยังรายการข้อมูลเมตาสำหรับคำบรรยายภายในไฟล์ .sub (VobSub Subtitles) มันถูกสร้างและใช้งานโดยแอพพลิเคชั่นซอฟต์แวร์ VobSub ที่ให้ผู้ใช้แยกคำบรรยายจากดีวีดีและดัมพ์ในไฟล์ SUB ไฟล์ IDX มีการประทับเวลาและการชดเชยไบต์ที่ใช้เพื่อชี้ไปที่ทุกคำบรรยาย VobSub จะสร้างไฟล์ IDX พร้อมกับไฟล์ SUB ที่เกี่ยวข้องเสมอ

## รูปแบบไฟล์ IDX - ข้อมูลเพิ่มเติม

ไฟล์ IDX ถูกสร้างขึ้นและบันทึกเป็นไฟล์ข้อความล้วนที่สามารถเปิดได้ในโปรแกรมแก้ไขข้อความ ไฟล์ IDX ประกอบด้วยข้อมูลที่อ่านโดยเครื่องเล่นมีเดียเพื่ออ่านพารามิเตอร์ เช่น สีของข้อความคำบรรยายที่จะแสดงบนหน้าจอ ตำแหน่งของข้อความคำบรรยายบนหน้าจอ

### การตั้งค่าคำบรรยาย IDX

ไฟล์ IDX ทั่วไปจะเก็บข้อมูลเมทาดาทานี้ไว้ที่ส่วนเริ่มต้นของไฟล์ การตั้งค่าคำบรรยายเริ่มต้นด้วย **#** การประทับเวลาและการอ้างอิงรูปภาพจะถูกเพิ่มหลังจากการตั้งค่าคำบรรยายเหล่านี้ทั้งหมด และเริ่มด้วย **การประทับเวลา:**

## ตัวอย่างรูปแบบไฟล์ IDX

```
# VobSub index file, v7 (do not modify this line!)
#
# To repair desyncronization, you can insert gaps this way:
# (it usually happens after vob id changes)
#
#	 delay: [sign]hh:mm:ss:ms
#
# Where:
#	 [sign]: +, - (optional)
#	 hh: hours (0 <= hh)
#	 mm/ss: minutes/seconds (0 <= mm/ss <= 59)
#	 ms: milliseconds (0 <= ms <= 999)
#
#	 Note: You can't position a sub before the previous with a negative value.
#
# You can also modify timestamps or delete a few subs you don't like.
# Just make sure they stay in increasing order.


# Settings

# Original frame size
size: 720x576

# Origin, relative to the upper-left corner, can be overloaded by aligment
org: 0, 0

# Image scaling (hor,ver), origin is at the upper-left corner or at the alignment coord (x, y)
scale: 100%, 100%

# Alpha blending
alpha: 100%

# Smoothing for very blocky images (use OLD for no filtering)
smooth: OFF

# In millisecs
fadein/out: 50, 50

# Force subtitle placement relative to (org.x, org.y)
align: OFF at LEFT TOP

# For correcting non-progressive desync. (in millisecs or hh:mm:ss:ms)
# Note: Not effective in DirectVobSub, use "delay: ... " instead.
time offset: 0

# ON: displays only forced subtitles, OFF: shows everything
forced subs: OFF

# The original palette of the DVD
palette: 000000, 828282, 828282, 828282, 828282, 828282, 828282, ffffff, 828282, bababa, 828282, 828282, 828282, 828282, 828282, 828282

# Custom colors (transp idxs and the four colors)
custom colors: OFF, tridx: 1000, colors: 000000, bababa, 828282, 000000

# Language index in use
langidx: 0

# English
id: en, index: 0
# Decomment next line to activate alternative name in DirectVobSub / Windows Media Player 6.x
# alt: English
# Vob/Cell ID: 1, 1 (PTS: 0)
timestamp: 00:01:25:880, filepos: 000003800
timestamp: 00:01:46:160, filepos: 000008000
timestamp: 00:02:08:880, filepos: 00000c800
# Vob/Cell ID: 1, 2 (PTS: 222840)
timestamp: 00:03:58:800, filepos: 000011000
timestamp: 00:04:00:680, filepos: 000016800
timestamp: 00:04:04:640, filepos: 00001d800
```

## จะใช้ไฟล์ IDX ได้อย่างไร?

หากคุณมีไฟล์ Sub และ IDX สำหรับภาพยนตร์ คุณสามารถเล่นคำบรรยายเหล่านี้พร้อมกับภาพยนตร์ที่สร้างคำบรรยายเหล่านี้ได้ แอปพลิเคชั่นมากมาย เช่น VLC, GOM Player, PotPlayer หรือ PowerDVD มีความสามารถในการโหลดไฟล์ SUB และ IDX เหล่านี้ และเล่นควบคู่ไปกับภาพยนตร์ แอปพลิเคชันซอฟต์แวร์ยังสามารถฝังไฟล์คำบรรยาย SUB และ IDX ไว้ในไฟล์ [.mkv](/th/video/mkv/)

## แปลง IDX เป็น SRT

[SRT](/th/video/srt/) (รูปแบบไฟล์ SubRip) เป็นไฟล์คำบรรยายธรรมดาที่บันทึกในรูปแบบไฟล์ SubRip เป็นที่นิยมใช้มากกว่าเมื่อเทียบกับรูปแบบไฟล์ VobSub ดังนั้น หากคุณต้องการแปลงไฟล์ SUB/IDX เป็นรูปแบบไฟล์ SRT มีเครื่องมือของบุคคลที่สามที่สามารถใช้เพื่อดำเนินการนี้ได้ ตัวแปลง SUB/IDX เป็น SRT ซึ่งมีอยู่ใน SubtitleTools.com เป็นเครื่องมือหนึ่งที่รับไฟล์ SUB และ IDX เป็นอินพุต และแปลงคำบรรยาย VobSub เป็นไฟล์ SRT

## อ้างอิง

* [VobSub](https://www.videohelp.com/software/VobSub)
* [VOBsub - วิกิมัลติมีเดีย](https://wiki.multimedia.cx/index.php?title=VOBsub)

