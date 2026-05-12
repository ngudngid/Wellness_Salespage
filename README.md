# Ployrada PRP Sales Pages — v2 (Brand Aligned)

Sales Page 2 หน้าสำหรับ Ployrada Wellness Clinic — รักษาผมร่วง และรักษาข้อเข่าเสื่อม
**ปรับ design ให้ตรงกับเว็บไซต์ต้นฉบับ [ployradawellness.com](https://www.ployradawellness.com)**

## 🎨 Design System ที่ใช้

| Element | Value | จาก |
|---------|-------|-----|
| สีหลัก (Primary) | `#47B9E3` Cyan | Brand color signature |
| สี Accent | `#FF4040` Red | สำหรับราคา/promo |
| สีตัวอักษร | `#000000` body / `#575757` muted | Body text |
| Font ไทย | Sukhumvit Set → fallback **Noto Sans Thai** | Wix encoded font ของ Ployrada |
| Font อังกฤษ | **Caudex** (Google Fonts) | English serif decoration |
| Heading size | 39px | Display |
| Body size | 18px | Standard |
| Radius ปุ่ม | 100px (pill) | Brand button style |
| Radius รูป | 20px | เพิ่มให้ premium |
| Signature element | `❝ ❞` Cyan quotes | Brand DNA |
| CTA Frame | "LIVE LONGER, BETTER AND HAPPIER" | จากเว็บต้นฉบับ |

## 📁 โครงสร้างไฟล์

```
ployrada-prp/
├── index.html          ← หน้า PRP Hair (รักษาผมร่วง)
├── prp-knee.html       ← หน้า PRP Knee (รักษาข้อเข่า)
├── sitemap.xml         ← บอก Google ว่ามี 2 หน้า
├── robots.txt          ← อนุญาตให้ Google crawl
├── vercel.json         ← config สำหรับ deploy
└── images/             ← รูปทั้งหมด 22 รูป
    ├── hair-1.jpg ... hair-11.jpg
    └── knee-1.jpg ... knee-11.jpg
```

## 🚀 วิธี Deploy ขึ้น Vercel (ฟรี + 10 นาทีเสร็จ)

### วิธีที่ 1: ผ่าน GitHub + Vercel (แนะนำ)

1. **สร้าง GitHub repo ใหม่**
   - ไปที่ https://github.com/new
   - ตั้งชื่อ: `ployrada-prp`
   - เลือก Public → คลิก Create

2. **Upload โค้ดเข้า GitHub** (ผ่านเว็บ — ไม่ต้อง terminal)
   - คลิก "uploading an existing file"
   - ลากไฟล์ทั้งหมด (รวม folder `images/`) เข้าไป
   - คลิก "Commit changes"

3. **เชื่อม Vercel กับ GitHub**
   - ไปที่ https://vercel.com/new
   - คลิก Import ตรง repo `ployrada-prp`
   - คลิก Deploy → รอ 1-2 นาที
   - ✅ ได้ URL `https://ployrada-prp-xxx.vercel.app`

### วิธีที่ 2: ผ่าน Vercel CLI

```bash
npm i -g vercel
cd ployrada-prp
vercel
# กด Enter ตามค่า default → เสร็จ
```

---

## 🔍 ทำให้ Google Search เจอ

### 1. แก้ Domain ใน sitemap.xml และ HTML

URL จริงจาก Vercel เช่น `ployrada-prp-abc123.vercel.app` ต้องแก้ใน:
- `sitemap.xml` — เปลี่ยน `https://ployrada-prp.vercel.app/` ให้ตรง
- `index.html` + `prp-knee.html` — หา `<link rel="canonical">` และ `og:url`

### 2. ส่งเข้า Google Search Console

1. https://search.google.com/search-console
2. Add Property → URL prefix → ใส่ URL เว็บไซต์
3. ยืนยันความเป็นเจ้าของ (ใช้ HTML meta tag — copy ไปวางใน `<head>`)
4. Sitemaps → submit `sitemap.xml`
5. URL Inspection → "Request Indexing" ทุกหน้า

### 3. Bing Webmaster Tools (เพิ่ม)
https://www.bing.com/webmasters — ทำแบบเดียวกัน

---

## ⏱️ Timeline หลัง Deploy

- **5 นาที**: เว็บออนไลน์ — ส่งลิงก์ลูกค้าได้ทันที
- **1-3 วัน**: Google เริ่ม index หน้าแรก
- **1-2 สัปดาห์**: Google index ครบทุกหน้า + เริ่มแสดงใน search
- **1-2 เดือน**: SEO ranking ขึ้น ถ้าคน click + engagement ดี

---

## 🎯 จุดเด่นของ v2 (ปรับจาก v1)

✅ **Match brand 100%** กับเว็บต้นฉบับ ployradawellness.com  
✅ **Color palette** — Cyan `#47B9E3` แทน Navy (ตรงกับเว็บแม่)  
✅ **Typography** — Noto Sans Thai + Caudex (replace Prompt + Bai Jamjuree)  
✅ **Signature elements** — `❝ ❞` quote marks, "LIVE LONGER, BETTER AND HAPPIER" CTA frame  
✅ **Button style** — Pill shape (100px radius) + Solid white on cyan  
✅ **Clean & medical feel** — White + Cyan dominant, ไม่ใช้ gradient เกินจำเป็น  
✅ **Mobile-first** — Font size auto-scale ที่ 600px breakpoint  
✅ **SEO ครบ** — title, description, OG tags, Schema.org MedicalBusiness, sitemap  
✅ **Floating Messenger** — ปุ่มลอย Facebook blue + pulse animation  
✅ **Cross-link** — หน้าผมลิงก์ไปหน้าเข่า และกลับ ขายข้ามได้  

---

## 📝 วิธีแก้ไขเนื้อหา

ทุกหน้าเป็น HTML ธรรมดา เปิดด้วย VS Code/Notepad แก้ได้เลย:

- **แก้สี Brand** → หา `:root` ส่วน `--color-primary` (จุดเดียวเปลี่ยนทั้งเว็บ)
- **แก้ headline** → หา `<h1>` หรือ `class="section-title"`
- **แก้ราคา** → หา `class="price"`
- **แก้ Facebook URL** → หา `facebook.com/hairployrada` หรือ `facebook.com/kneehealthcenter`
- **แก้เบอร์โทร** → หา `0657196555`
- **เปลี่ยนรูป** → แทนที่ไฟล์ใน `images/` (ใช้ชื่อเดิม)
- **เพิ่ม section** → copy `<section class="section fade-in">` block แล้วแก้

---

## 📞 ติดต่อ

**Ployrada Wellness Clinic ระยอง**
- ☎️ 065-719-6555
- 🌐 https://www.ployradawellness.com
- 📘 Facebook (ผม): https://www.facebook.com/hairployrada/
- 📘 Facebook (เข่า): https://www.facebook.com/kneehealthcenter
