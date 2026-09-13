# ตารางคะแนน Performance จุดจอดรถพยาบาล
## Dashboard แบบฟุตบอล Bundesliga

ศูนย์เอราวัณ กรุงเทพมหานคร - ระบบติดตามประสิทธิภาพจุดจอดรถพยาบาล

---

## ⚡ วิธีใช้งาน Dashboard

### 1. เปิดแบบออนไลน์ (GitHub Pages)
- เข้าไปที่ลิงค์ GitHub Pages ของ repository นี้
- Dashboard จะโหลดขึ้นมาพร้อมใช้งาน

### 2. เปิดแบบไฟล์ในเครื่อง
- Download ไฟล์ `DASHBOARD_จุดจอด_PERFORMANCE.html` 
- เปิดด้วย Web Browser (Chrome, Firefox, Safari ฯลฯ)

### 3. อัปโหลดข้อมูลเดือนใหม่
1. เตรียมไฟล์ Excel (.xlsx) ที่มีคอลัมน์ข้อมูล:
   - `ALS_<MONTH>` - ข้อมูล ALS (Advanced Life Support)
   - `BLS_<MONTH>` - ข้อมูล BLS (Basic Life Support)
   - เช่น: `ALS_September`, `BLS_September` เป็นต้น

2. คลิกปุ่ม "📊 อัปโหลดข้อมูลเดือนใหม่"
3. ลากหรือเลือกไฟล์ Excel
4. ระบบจะอ่านข้อมูลและแสดงผลอัตโนมัติ

### 4. เลือกดูรูปแบบตาราง
- **แบบ A**: ข้อมูลรายเดือน (แสดงคะแนนต่อเดือน)
- **แบบ B**: ข้อมูลรายประเภท (ALS/BLS/รวม)
- **แบบ C**: ตารางรวมทุกเดือน (ตั้งแต่มิถุนายน 2569 ถึงปัจจุบัน)

### 5. จัดการ Logo จุดจอด
- คลิกที่ชื่อจุดจอด → คลิก "🖼️ เปลี่ยน Logo"
- เลือกรูป PNG หรือ JPG จากเครื่อง
- ระบบจะบันทึก logo ไว้ให้

---

## 📂 โครงสร้าง Repository

```
ambulance-performance-dashboard/
├── DASHBOARD_จุดจอด_PERFORMANCE.html    (ไฟล์ Dashboard หลัก)
├── README.md                             (ไฟล์นี้เอง)
├── LOGO_UPLOAD_GUIDE.md                  (คู่มือการอัปโหลด Logo)
└── logos/                                (โฟลเดอร์เก็บรูป Logo)
    ├── station1.png
    ├── station2.png
    └── ...
```

---

## 🚀 วิธีอัปโหลด Dashboard ขึ้น GitHub

### ขั้นตอนที่ 1: ตั้งค่า Git
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### ขั้นตอนที่ 2: สร้างโฟลเดอร์ Project
```bash
mkdir ambulance-performance-dashboard
cd ambulance-performance-dashboard
```

### ขั้นตอนที่ 3: Initialize Git
```bash
git init
```

### ขั้นตอนที่ 4: Copy ไฟล์ Dashboard
- Copy `DASHBOARD_จุดจอด_PERFORMANCE.html` เข้าโฟลเดอร์
- Rename เป็น `index.html` (เพื่อให้เป็นไฟล์เริ่มต้น)

### ขั้นตอนที่ 5: สร้างไฟล์ README
```bash
# Copy ไฟล์นี้เข้าโฟลเดอร์
```

### ขั้นตอนที่ 6: Add ไฟล์
```bash
git add .
```

### ขั้นตอนที่ 7: Commit
```bash
git commit -m "Initial commit: Add ambulance performance dashboard"
```

### ขั้นตอนที่ 8: สร้าง Repository บน GitHub
1. ไปที่ https://github.com/new
2. ตั้งชื่อ: `ambulance-performance-dashboard`
3. ไม่ต้องเลือก "Add README" (เพราะเรามีแล้ว)
4. คลิก "Create repository"

### ขั้นตอนที่ 9: Connect Local Repository
```bash
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/ambulance-performance-dashboard.git
```
(แทนที่ `YOUR_USERNAME` ด้วยชื่อ GitHub ของคุณ)

### ขั้นตอนที่ 10: Push ขึ้น GitHub
```bash
git push -u origin main
```

### ขั้นตอนที่ 11: เปิดใช้ GitHub Pages
1. ไปที่ Settings ของ Repository
2. ค้นหา "Pages" (ด้านซ้าย)
3. ในส่วน "Build and deployment" เลือก:
   - Source: "Deploy from a branch"
   - Branch: `main` Folder: `/ (root)`
4. คลิก Save
5. รอสักครู่ จะได้ URL เช่น `https://YOUR_USERNAME.github.io/ambulance-performance-dashboard/`

---

## 🎨 วิธีอัปโหลด Logo ขึ้น GitHub

### วิธีที่ 1: Upload ผ่าน GitHub Web Interface (ง่ายที่สุด)

**ขั้นตอนแรก: สร้างโฟลเดอร์ `logos/`**
1. ไปที่ GitHub Repository ของคุณ
2. คลิก "Add file" → "Create new file"
3. พิมพ์ชื่อไฟล์เป็น: `logos/.gitkeep`
4. คลิก "Commit changes"
5. ตอบ "Commit message" ได้เป็น "Add logos folder"

**อัปโหลด Logo ใหม่:**
1. ไปที่ Repository → คลิก "Add file" → "Upload files"
2. ลากรูป Logo ขึ้นไป หรือ คลิกเลือกไฟล์
3. ตรวจสอบว่าไฟล์อยู่ในโฟลเดอร์ `logos/` (ถ้าไม่ให้ย้ายไฟล์)
4. คลิก "Commit changes"

### วิธีที่ 2: Upload ผ่าน Git Command Line

**ถ้า logo ยังไม่อยู่ใน GitHub:**
```bash
# 1. สร้างโฟลเดอร์ logos ในเครื่องของคุณ
mkdir logos

# 2. Copy รูป logo เข้าไปที่โฟลเดอร์ logos/
# เช่น: logos/station1.png, logos/station2.png

# 3. Add ไฟล์
git add logos/

# 4. Commit
git commit -m "Add logo files for ambulance stations"

# 5. Push ขึ้น GitHub
git push
```

**ถ้าต้องการอัปเดต logo เดิม:**
```bash
# 1. Replace ไฟล์เดิมใน logos/
# 2. Add, Commit, Push เหมือนเดิม
git add logos/station1.png
git commit -m "Update logo for station 1"
git push
```

---

## 🔗 การใช้ Logo ใน Dashboard

### ถ้า Logo เก็บใน GitHub Repository:

Dashboard จะอ้างอิงไปยัง URL:
```
https://raw.githubusercontent.com/YOUR_USERNAME/ambulance-performance-dashboard/main/logos/station1.png
```

**หมายเหตุ:** Dashboard ปัจจุบันเก็บ logo เป็น Base64 ใน localStorage ของเบราว์เซอร์ ดังนั้น:
- ✅ เมื่ออัปโหลดผ่าน Dashboard → logo เก็บไว้ในอุปกรณ์นั้น
- ❌ ถ้าเปิดจากอุปกรณ์อื่น → logo จะไม่ปรากฏ

**เพื่อให้ logo ปรากฏร่วมกัน จำเป็นต้องอัปเดต HTML:**
- เพิ่มไฟล์ logo ลงใน `logos/` folder
- แก้ไข HTML เพื่อให้ชี้ไปยัง URL ของ GitHub repository

---

## 📝 การอัปเดตข้อมูลต่อไป

### อัปเดต Dashboard:
```bash
# 1. แก้ไขไฟล์ index.html ในเครื่อง
# 2. Commit
git add index.html
git commit -m "Update dashboard with new features"
# 3. Push
git push
```

### อัปเดต Logo:
```bash
# Replace รูป logo เดิม หรือ เพิ่มรูป logo ใหม่
git add logos/
git commit -m "Update logos"
git push
```

---

## ⚙️ การแก้ปัญหา

### GitHub Pages ไม่แสดงผล
- ตรวจสอบว่า Settings → Pages → ตั้ง Branch เป็น `main` และ Folder เป็น `/ (root)`
- รอ 1-2 นาทีให้ GitHub Pages สร้างไซต์เสร็จ

### Logo ไม่ปรากฏ
- ตรวจสอบว่าไฟล์ logo อยู่ในโฟลเดอร์ `logos/` ของ GitHub
- ตรวจสอบชื่อไฟล์ว่า ถูกต้อง (เช่น `station1.png`)

### ข้อมูล Excel ไม่อัปโหลด
- ตรวจสอบว่าไฟล์ Excel มีคอลัมน์ชื่อ `ALS_<MONTH>` และ `BLS_<MONTH>`
- ตรวจสอบว่าใช้ไฟล์ .xlsx (ไม่ใช่ .xls หรือ .csv)

---

## 📞 ติดต่อและสนับสนุน
หากมีปัญหาหรือข้อเสนอแนะ สามารถสร้าง Issue ใน GitHub repository ได้

---

**เวอร์ชัน:** 1.0  
**อัปเดตล่าสุด:** กันยายน 2569  
**ศูนย์เอราวัณ กรุงเทพมหานคร**
