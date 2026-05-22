# 📦 Item Exchange - ระบบแลกเปลี่ยนสิ่งของออนไลน์
 
> แพลตฟอร์มแลกเปลี่ยนสิ่งของออนไลน์ที่ออกแบบมาเพื่อให้ผู้ใช้สามารถค้นหา แลกเปลี่ยน และสื่อสารได้อย่างสะดวก
 
---
 
## ✨ ภาพรวมโปรเจค
 
**Item Exchange** คือระบบแลกเปลี่ยนสิ่งของออนไลน์ที่ช่วยให้ผู้ใช้สามารถ:
 
- 🏪 ขายและแลกเปลี่ยนสิ่งของกับผู้อื่น
- 💬 สื่อสารผ่านระบบแชทเรียลไทม์
- ⭐ ให้คะแนนและรีวิวหลังการแลกเปลี่ยน
- 📊 ติดตามประวัติการแลกเปลี่ยนของตัวเอง
- 🏆 ดู Leaderboard ของผู้ใช้ที่เชื่อถือได้
---
 
## 🛠️ เทคโนโลยีที่ใช้
 
| ประเภท | เทคโนโลยี | เวอร์ชั่น |
|--------|-----------|----------|
| **Backend** | PHP | 7.4+ |
| **Frontend** | HTML5, CSS3, JavaScript | ES6 |
| **Database** | MySQL | 5.7+ |
| **Email Service** | PHPMailer | SMTP |
| **Web Server** | Apache (XAMPP) | 2.4+ |
| **Version Control** | Git | 2.40+ |
 
---
 
## 🎯 ฟีเจอร์หลักของระบบ
 
### 👤 ฟีเจอร์สำหรับผู้ใช้ทั่วไป
 
#### การจัดการบัญชี
- ✅ ลงทะเบียนผู้ใช้ใหม่พร้อมตรวจสอบอีเมล
- ✅ เข้าสู่ระบบด้วย Email หรือ Username
- ✅ ตั้งรหัสผ่านใหม่ (Password Reset)
- ✅ แก้ไขโปรไฟล์ส่วนตัว
#### จัดการสิ่งของ
- ✅ เพิ่มสิ่งของใหม่พร้อมรูปภาพ
- ✅ แก้ไขรายละเอียดสิ่งของ
- ✅ ลบสิ่งของออกจากระบบ
- ✅ ดูรายการของตัวเองทั้งหมด
#### การค้นหาและแลกเปลี่ยน
- ✅ ค้นหาสิ่งของด้วยคำค้นหา
- ✅ กรองตามหมวดหมู่
- ✅ ส่งคำขอแลกเปลี่ยน
- ✅ ติดตามสถานะคำขอ
- ✅ ดูเสนอแนะสิ่งของที่เหมาะสม
#### สื่อสารและรีวิว
- ✅ ส่งข้อความแชทเรียลไทม์
- ✅ ให้คะแนนการแลกเปลี่ยน (1-5 ดาว)
- ✅ เขียนรีวิวผู้ใช้อื่น
- ✅ ดูรีวิวที่ได้รับ
- ✅ ติดตามประวัติการแลกเปลี่ยน
#### อื่น ๆ
- ✅ ดู Leaderboard ผู้ใช้ที่มีคะแนนสูง
- ✅ รายงานปัญหาหรือพฤติกรรมไม่สุจริต
### 👨‍💼 ฟีเจอร์สำหรับแอดมิน
 
#### จัดการสิ่งของ
- ✅ ดูรายการสิ่งของที่รอการอนุมัติ
- ✅ อนุมัติหรือปฏิเสธรายการใหม่
- ✅ ลบสิ่งของที่ไม่เหมาะสม
- ✅ จัดการหมวดหมู่สินค้า
#### จัดการผู้ใช้
- ✅ ดูรายชื่อผู้ใช้ทั้งหมด
- ✅ แก้ไขข้อมูลผู้ใช้
- ✅ บล็อกหรือลบบัญชีผู้ใช้
- ✅ ตรวจสอบสถิติผู้ใช้
#### จัดการระบบ
- ✅ ดูประกาศและจัดการ
- ✅ ส่งประกาศไปยังผู้ใช้
- ✅ ดูรีวิวและการร้องเรียน
- ✅ ดูรายงานการใช้งาน
- ✅ วิเคราะห์สถิติการแลกเปลี่ยน
---
 
## 📁 โครงสร้างโปรเจค
 
```
item-exchange/
│
├── 📄 index.html                    # หน้าแรก (Public)
├── 📄 login.html                    # หน้าเข้าสู่ระบบ
├── 📄 register.html                 # หน้าลงทะเบียน
├── 📄 README.md                     # ไฟล์เอกสารนี้
├── 📄 item_exchange.sql             # โครงสร้างฐานข้อมูล
│
├── 📁 user/                         # 👤 ส่วนผู้ใช้ทั่วไป
│   ├── main.php                     # หน้าหลักผู้ใช้
│   ├── add_item.php                 # เพิ่มสิ่งของใหม่
│   ├── my_items.php                 # ดูสิ่งของของตัวเอง
│   ├── edit_item.php                # แก้ไขสิ่งของ
│   ├── market.php                   # ตลาด/ค้นหาสิ่งของ
│   ├── find_matches.php             # หาสิ่งของที่เหมาะสม
│   ├── item_detail.php              # ดูรายละเอียดสิ่งของ
│   ├── offer_exchange.php           # ส่งคำขอแลกเปลี่ยน
│   ├── exchange_requests_sent.php   # ดูคำขอที่ส่งไป
│   ├── exchange_requests_received.php # ดูคำขอที่รับมา
│   ├── chat.php                     # ระบบแชท
│   ├── fetch_messages.php           # ดึงข้อความแชท
│   ├── rate_exchange.php            # ให้คะแนนการแลก
│   ├── my_reviews.php               # ดูรีวิวของตัวเอง
│   ├── reviews_received.php         # ดูรีวิวที่ได้รับ
│   ├── leaderboard.php              # ดู Leaderboard
│   ├── edit_profile.php             # แก้ไขโปรไฟล์
│   └── ...
│
├── 📁 admin/                        # 👨‍💼 ส่วนแอดมิน
│   ├── admin_main.php               # Dashboard แอดมิน
│   ├── approve_item.php             # อนุมัติสิ่งของ
│   ├── manage_items.php             # จัดการสิ่งของ
│   ├── edit_item.php                # แก้ไขสิ่งของ
│   ├── delete_item.php              # ลบสิ่งของ
│   ├── manage_users.php             # จัดการผู้ใช้
│   ├── edit_user.php                # แก้ไขข้อมูลผู้ใช้
│   ├── manage_categories.php        # จัดการหมวดหมู่
│   ├── manage_announcements.php     # จัดการประกาศ
│   ├── manage_reviews.php           # จัดการรีวิว
│   ├── admin_reports.php            # ดูรายงาน
│   └── ...
│
├── 📁 PHPMailer-master/             # ไลบรารี่ส่งอีเมล
├── 📁 uploads/                      # 📂 โฟลเดอร์เก็บไฟล์
│   ├── item/                        # รูปสินค้า
│   ├── profile/                     # รูปโปรไฟล์ผู้ใช้
│   ├── chat/                        # ไฟล์แชท
│   └── user/                        # ไฟล์ผู้ใช้อื่น ๆ
│
└── 📁 tools/                        # 🛠️ เครื่องมือทดสอบ
```
 
---
 
## 🚀 วิธีการติดตั้ง
 
### ⚙️ ความต้องการเบื้องต้น (Prerequisites)
 
- **PHP 7.4** ขึ้นไป (หรือ PHP 8.0+)
- **MySQL 5.7** ขึ้นไป (รองรับ 8.0)
- **Apache 2.4** ขึ้นไป
- **Git** สำหรับ clone repository
- **Composer** (ตัวเลือก - สำหรับ PHPMailer)
- **XAMPP** (แนะนำสำหรับการพัฒนา)
### 📋 ขั้นตอนการติดตั้ง
 
#### 1️⃣ Clone Repository
 
```bash
cd C:\xampp\htdocs
git clone https://github.com/Punyawit1/item-exchange.git
cd item-exchange
```
 
#### 2️⃣ ตั้งค่าฐานข้อมูล MySQL
 
เปิด phpMyAdmin ที่ `http://localhost/phpmyadmin` แล้วทำตามนี้:
 
```sql
CREATE DATABASE item_exchange CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
USE item_exchange;
```
 
จากนั้น Import ไฟล์ `item_exchange.sql` ผ่าน phpMyAdmin
 
หรือใช้ Command Line:
 
```bash
mysql -u root -p
CREATE DATABASE item_exchange CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
USE item_exchange;
SOURCE item_exchange.sql;
```
 
#### 3️⃣ ตั้งค่าการเชื่อมต่อฐานข้อมูล
 
ตรวจสอบและแก้ไขไฟล์ config ของโปรเจค (ปกติอยู่ในไฟล์เชื่อมต่อฐานข้อมูลหรือ config file):
 
```php
$host     = "localhost";
$user     = "root";
$password = "";              // ใส่รหัสผ่านถ้ามี
$database = "item_exchange";
```
 
#### 4️⃣ เปิด Apache และ MySQL
 
1. เปิด **XAMPP Control Panel**
2. กด **Start** ที่ **Apache**
3. กด **Start** ที่ **MySQL**
#### 5️⃣ เข้าใช้งาน
 
| หน้า | URL |
|------|-----|
| 🌐 หน้าแรก | `http://localhost/item-exchange/` |
| 🔐 เข้าสู่ระบบ | `http://localhost/item-exchange/login.html` |
| 📋 สมัครสมาชิก | `http://localhost/item-exchange/register.html` |
| 👨‍💼 แอดมิน | `http://localhost/item-exchange/admin/admin_main.php` |
 
---
 
## 📖 วิธีการใช้งาน
 
### 👤 สำหรับผู้ใช้ทั่วไป
 
#### 1. สมัครสมาชิก
- ไปที่หน้า [Register](register.html)
- กรอก Email, ชื่อผู้ใช้, รหัสผ่าน
- ตรวจสอบอีเมลเพื่อยืนยันบัญชี
#### 2. เข้าสู่ระบบ
- ใช้ Email หรือ Username กับรหัสผ่าน
- ถ้าลืมรหัสผ่าน → ไปที่ **Forgot Password**
#### 3. เพิ่มสิ่งของ
- ไปที่ **Add Item** (เมนูหลัก)
- กรอกข้อมูล: ชื่อ, หมวดหมู่, คำอธิบาย, ราคา
- อัพโหลดรูปภาพ
- กด **Submit**
#### 4. ค้นหาสิ่งของ
- ไปที่ **Market** หรือ **Browse**
- ใช้ Search bar เพื่อค้นหา
- กรองตามหมวดหมู่
- คลิกสิ่งของเพื่อดูรายละเอียด
#### 5. ส่งคำขอแลกเปลี่ยน
- เลือกสิ่งของที่ต้องการ
- เลือกสิ่งของของตัวเองที่จะแลก
- กด **Send Exchange Request**
- รอให้เจ้าของยอมรับหรือปฏิเสธ
#### 6. แชทกับผู้ใช้
- ไปที่ **Chat**
- เลือกคู่สนทนา
- พูดคุยและตกลงรายละเอียด
#### 7. ให้คะแนนหลังการแลก
- ไปที่ **Rate Exchange**
- เลือกการแลกที่เสร็จแล้ว
- ให้คะแนน 1-5 ดาว
- เขียนรีวิว (ตัวเลือก)
### 👨‍💼 สำหรับแอดมิน
 
#### เข้าสู่ระบบแอดมิน
- URL: `http://localhost/item-exchange/admin/admin_main.php`
- ใช้บัญชี Admin ของคุณ
#### งานหลักของแอดมิน
 
**1. อนุมัติสิ่งของ**
- ไปที่ **Approve Items**
- ตรวจสอบสิ่งของใหม่ที่รอการอนุมัติ
- กด **Approve** หรือ **Reject**
**2. จัดการผู้ใช้**
- ไปที่ **Manage Users**
- ดูข้อมูลผู้ใช้ทั้งหมด
- บล็อกหรือลบบัญชี
- แก้ไขข้อมูลผู้ใช้
**3. จัดการสิ่งของ**
- ไปที่ **Manage Items**
- ลบสิ่งของที่ไม่เหมาะสม
- ตรวจสอบข้อมูลสิ่งของ
**4. ส่งประกาศ**
- ไปที่ **Announcements**
- สร้างข้อความประกาศใหม่
- ส่งไปยังผู้ใช้ทั้งหมด
**5. ดูรายงาน**
- ไปที่ **Reports**
- วิเคราะห์สถิติการใช้งาน
- ติดตามปัญหาและการร้องเรียน
---
 
## 🔧 การแก้ไขปัญหาทั่วไป
 
### ❌ ไม่สามารถเชื่อมต่อฐานข้อมูล
 
**สาเหตุที่พบบ่อย:**
- MySQL ไม่ได้รัน
- ชื่อผู้ใช้/รหัสผ่าน/ชื่อฐานข้อมูล ผิด
- Database ยังไม่ได้ import
**วิธีแก้:**
```bash
# 1. เปิด XAMPP Control Panel ให้ MySQL รัน
# 2. ตรวจสอบการตั้งค่า MySQL ในไฟล์ config
# 3. Import item_exchange.sql ไปที่ MySQL
mysql -u root -p < item_exchange.sql
```
 
### ❌ ส่งอีเมลไม่ได้
 
**สาเหตุที่พบบ่อย:**
- PHPMailer ตั้งค่า SMTP ไม่ถูกต้อง
- Gmail ต้องใช้ App Password แทนรหัสผ่านปกติ
- Firewall บล็อก SMTP port
**วิธีแก้:**
```php
// ตรวจสอบไฟล์ที่ส่งอีเมล
// ตั้งค่า SMTP Server ให้ถูกต้อง:
$mail->Host       = 'smtp.gmail.com';
$mail->Port       = 587;
$mail->Username   = 'your-email@gmail.com';
$mail->Password   = 'your-app-password'; // ใช้ App Password จาก Google
$mail->SMTPSecure = PHPMailer::ENCRYPTION_STARTTLS;
```
 
### ❌ ไฟล์อัพโหลดไม่ได้
 
**สาเหตุที่พบบ่อย:**
- โฟลเดอร์ `uploads/` ไม่มีสิทธิ์เขียน
- ไฟล์ขนาดใหญ่เกินกว่า `upload_max_filesize`
**วิธีแก้:**
```bash
# ตั้งสิทธิ์โฟลเดอร์ uploads/
chmod -R 755 uploads/
 
# ตรวจสอบ php.ini
upload_max_filesize = 10M
post_max_size = 10M
```
 
### ❌ หน้าเว็บ Blank หรือ Error 500
 
**วิธีแก้:**
```bash
# 1. เปิด Apache error log
# Windows: C:\xampp\apache\logs\error.log
# Linux: /var/log/apache2/error.log
 
# 2. เปิด PHP error log ใน php.ini
display_errors = On
log_errors = On
error_log = /path/to/php_error.log
 
# 3. ตรวจสอบ syntax ของไฟล์ PHP
php -l path/to/file.php
```
 
---
 
## 📞 แผนพัฒนาในอนาคต
 
- 📱 **Mobile App** - React Native
- 🔔 **Push Notifications** - Firebase Cloud Messaging
- 🌍 **Multi-language Support** - i18n
- 💳 **Payment Gateway** - Stripe / PayPal Integration
- 📊 **Advanced Analytics Dashboard**
- 🔐 **Two-Factor Authentication** - 2FA
- 🌙 **Dark Mode Support**
- 🚀 **Performance Optimization**
---
 
## 📝 ใบอนุญาต
 
โปรเจคนี้อยู่ภายใต้ใบอนุญาต **MIT License**
 
ดูรายละเอียด: [LICENSE](LICENSE)
 
---
 
## 👥 ผู้มีส่วนร่วม
 
- **Punyawit** - ผู้พัฒนาหลัก
---
 
## 💬 ติดต่อและสนับสนุน
 
หากมีคำถาม ข้อเสนอแนะ หรือพบปัญหา:
 
- 📧 **GitHub Issues**: [item-exchange Issues](https://github.com/Punyawit1/item-exchange/issues)
- 🔗 **GitHub Profile**: [@Punyawit1](https://github.com/Punyawit1)
- 📝 **Project Repository**: [item-exchange](https://github.com/Punyawit1/item-exchange)
---
 
## 📚 เอกสารอ้างอิง
 
- [PHP Documentation](https://www.php.net/)
- [MySQL Documentation](https://dev.mysql.com/doc/)
- [PHPMailer GitHub](https://github.com/PHPMailer/PHPMailer)
- [Git Guide](https://git-scm.com/doc)
- [HTML5 Standard](https://html.spec.whatwg.org/)
- [CSS Specifications](https://www.w3.org/Style/CSS/)
---
 
## ✅ Checklist เตรียมการก่อนไปใช้งาน
 
- [ ] Clone Repository
- [ ] ตั้งค่าฐานข้อมูล MySQL
- [ ] Import `item_exchange.sql`
- [ ] ตั้งค่าไฟล์ config (username, password, database)
- [ ] ตั้งค่า PHPMailer (SMTP settings)
- [ ] เปิด Apache และ MySQL ใน XAMPP
- [ ] ทดสอบหน้าแรก `http://localhost/item-exchange/`
- [ ] สร้างบัญชี Admin
- [ ] ทดสอบการลงทะเบียนและเข้าสู่ระบบ
