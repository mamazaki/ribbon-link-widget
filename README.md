# Ribbon Link Widget (วิดเจ็ตริบบิ้นลิงก์)

วิดเจ็ตริบบิ้นสำหรับติดมุมหน้าเว็บ โดยตั้งค่าให้คลิกลิงก์ไปยังหน่วยงานหรือหน้าที่ต้องการได้ทันที
ตัวอย่างนี้ตั้งให้ไปยังลิงก์พระราชประวัติสมเด็จพระนางเจ้าสิริกิติ์ พระบรมราชินีนาถ พระบรมราชชนนีพันปีหลวง และมี CSS พร้อมคลาสกำหนดตำแหน่ง 4 มุม + ตัวเลือก Grayscale

## คุณสมบัติ
- ติดริบบิ้นได้ 4 มุม: บนซ้าย/บนขวา/ล่างซ้าย/ล่างขวา
- ปรับขนาดง่ายด้วย CSS ตัวแปร `--ribbon-size`
- ตัวเลือก `grayscale(50%)` และเอฟเฟกต์ hover กลับเป็นสี
- ใช้ HTML/CSS ล้วน ติดตั้งง่าย นำไปใช้กับทุกเว็บได้
- มีตัวอย่างหน้า `index.html` สำหรับทดสอบ

## การใช้งานแบบเร็ว (Quick Start)

1) ใส่ไฟล์ CSS
```html
<link rel="stylesheet" href="styles.css">
```

2) วางโค้ดลิงก์ริบบิ้นใน `<body>` (ตัวอย่างล่างซ้าย):
```html
<a class="ribbon ribbon--bottom-left gray-50"
   href="https://www.royaloffice.th/25/10/2025/%E0%B8%9E%E0%B8%A3%E0%B8%B0%E0%B8%A3%E0%B8%B2%E0%B8%8A%E0%B8%9B%E0%B8%A3%E0%B8%B0%E0%B8%A7%E0%B8%B1%E0%B8%95%E0%B8%B4-12-08-2566/"
   target="_blank" rel="noopener">
  <img src="assets/ribbon-bottom-left.svg" class="wpm-ribbon" alt="กลับหน้าแรก">
</a>
```

> เปลี่ยนภาพเป็นมุมอื่นได้: `assets/ribbon-top-left.svg`, `assets/ribbon-top-right.svg`, `assets/ribbon-bottom-right.svg`  
> เปลี่ยนตำแหน่งโดยสลับคลาส: `ribbon--top-left`, `ribbon--top-right`, `ribbon--bottom-left`, `ribbon--bottom-right`

3) ป้ายคลาส `gray-50` ถ้าต้องการโทนเทา 50% (เอาออกได้ถ้าไม่ต้องการ)

---

## ปรับแต่ง
- ขนาดริบบิ้น: ตั้งค่าที่ตัวแปร CSS
```css
:root { --ribbon-size: 120px; } /* ค่าเริ่มต้น */
```
- ปรับค่า Grayscale:
```css
:root { --grayness: 50%; } /* 0% = สีปกติ, 100% = ขาวดำ */
```
- ปิดเอฟเฟกต์โทนเทาเฉพาะบางอัน: เอาคลาส `gray-50` ออก หรือเพิ่มคลาส `no-gray`

## โครงสร้างโปรเจกต์
```
ribbon-link-widget/
├─ assets/
│  ├─ ribbon-bottom-left.svg
│  ├─ ribbon-bottom-right.svg
│  ├─ ribbon-top-left.svg
│  └─ ribbon-top-right.svg
├─ index.html
├─ styles.css
├─ LICENSE
└─ README.md
```

## License
MIT — ใช้ได้อิสระทั้งส่วนตัวและเชิงพาณิชย์