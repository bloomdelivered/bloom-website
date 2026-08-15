# สิ่งที่แก้ไขให้ (SEO)

## ไฟล์ที่แก้ไข/เพิ่มใหม่
- `index.html` — เพิ่ม title/description ที่มีคีย์เวิร์ดไทย, Open Graph, Twitter Card, canonical URL, และ Structured Data (Organization + Product) แบบ JSON-LD, เพิ่มลิงก์ไปหน้า FAQ ใน nav และ footer
- `faq.html` **(ใหม่)** — หน้าคำถามที่พบบ่อย มีเนื้อหาให้ความรู้จริง (ตอบคำถามที่คนค้นหาบ่อยเช่น "เลือกผ้าอนามัยยังไงให้เหมาะกับตัวเอง") พร้อม FAQPage schema ช่วยให้มีโอกาสขึ้น Google ในรูปแบบ rich snippet
- `privacy-policy.html` — เพิ่ม canonical + robots meta ให้ครบ
- `robots.txt` **(ใหม่)** — บอก Google ว่าเข้าถึงเว็บได้ทั้งหมด และชี้ไปที่ sitemap
- `sitemap.xml` **(ใหม่)** — แผนผัง URL ทั้งหมดของเว็บ ให้ Google เก็บ index ได้ครบ

## วิธีอัปโหลดใช้งานจริง
1. เข้า Netlify dashboard ของเว็บ blooooooom
2. ลาก-วางไฟล์ทั้งหมดในโฟลเดอร์นี้ทับของเดิม (deploy แบบ drag & drop) หรือ push ผ่าน Git ถ้าคุณต่อ repo ไว้
3. รอ deploy เสร็จ (ไม่กี่วินาที) แล้วเช็คว่าเว็บขึ้นปกติที่ https://blooooooom.netlify.app/

## สิ่งที่ต้องทำต่อ (ฟรีทั้งหมด)
1. **Google Search Console** → เข้า https://search.google.com/search-console → เพิ่มเว็บ blooooooom.netlify.app → ยืนยันความเป็นเจ้าของ (เลือกวิธี HTML tag ง่ายสุด แปะใน `<head>` ของ index.html) → ไปที่เมนู Sitemaps → ใส่ `sitemap.xml` → Submit
2. **ขอให้ Google Index หน้าใหม่ทันที** ใน Search Console ใช้ "URL Inspection" แล้วกด "Request Indexing" กับทั้ง index.html และ faq.html
3. **เขียนบทความเพิ่ม** — หน้า FAQ ช่วยได้เยอะแล้ว แต่ถ้ามีเวลาแนะนำเพิ่มบทความยาวๆ อีก 2-3 เรื่อง เช่น "ผ้าอนามัยแบบไหนเหมาะกับวันมามาก" แล้วลิงก์กลับมาที่หน้าแพ็กเกจ
4. **แชร์ลิงก์ FAQ** ในกลุ่ม Facebook/Pantip ที่เกี่ยวกับสุขภาพผู้หญิง แทนการแชร์ลิงก์ขายตรง — คนคลิกเข้ามาอ่านแล้วเจอสินค้าเองโดยธรรมชาติ ไม่โดนมองว่าเป็นสแปม

## หมายเหตุ
- โดเมนที่ใช้อ้างอิงในทุกไฟล์คือ `https://blooooooom.netlify.app/` — ถ้าซื้อโดเมนของตัวเองในอนาคต ต้องแก้ URL นี้ในทุกไฟล์ (canonical, og:url, sitemap.xml, robots.txt) ให้เป็นโดเมนใหม่
