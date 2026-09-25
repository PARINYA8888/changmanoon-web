# changmanoon-web

Frontend ของ ระบบโรงกลึงช่างมนูญบ่อทอง สำหรับ GitHub Pages

## Backend
Google Sheets / Google Drive / PDF / รูปภาพ / การคำนวณยังอยู่ที่ Google Apps Script เดิมทั้งหมด

GitHub Pages ใช้ iframe bridge เพื่อให้ frontend เรียกฟังก์ชัน Apps Script เดิมได้ โดยไม่ต้องย้ายข้อมูล

## Setup
1. เพิ่ม ApiBridge.html เข้า Apps Script project เดิม
2. เปลี่ยน doGet(e) ตาม Code.gs.patch.txt
3. Deploy Web App เวอร์ชันใหม่
4. นำ URL ที่ลงท้ายด้วย /exec ไปใส่ใน APPS_SCRIPT_WEB_APP_URL ใน index.html
5. เปิด GitHub Pages: Settings -> Pages -> Deploy from branch -> main / root

อย่าใส่ secret หรือ API key ลงใน index.html เพราะ repository นี้เป็น public.
