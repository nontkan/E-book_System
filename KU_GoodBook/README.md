# KU GoodBook

โปรแกรมอ่านหนังสือที่เขียนด้วย Java และใช้ Java Swing ทำหน้าจอ
ข้อมูลของแอปเก็บเป็นไฟล์ CSV ในโฟลเดอร์ `data`

## เปิดโปรแกรม

เปิดโปรเจกต์ใน Eclipse แล้วรัน `src/app/Main.java`

## ส่วนสำคัญของโปรเจกต์

| ต้องการแก้ส่วนไหน | ไฟล์หลัก |
| --- | --- |
| เริ่มโปรแกรม | `src/app/Main.java` |
| หน้าเข้าสู่ระบบสมาชิก | `src/ui/pages/LoginScreen.java` |
| หน้าเข้าสู่ระบบแอดมิน | `src/ui/pages/AdminLoginScreen.java` |
| หน้าแรกและรายการหนังสือ | `src/ui/pages/HomeScreen.java` |
| เพิ่มและแก้ไขหนังสือ/ตอน | `src/ui/pages/AdminScreen.java` |
| ตรวจข้อมูลหนังสือก่อนบันทึก | `src/logic/admin/AdminBookLogic.java` |
| อ่านและเขียนหนังสือกับเนื้อหาตอน | `src/storage/admin/AdminStorage.java` |
| อ่านและเขียนข้อมูลสมาชิก รายการโปรด และรีวิว | `src/storage/CsvStorage.java` |
| รูปแบบหน้าจอและสี | `src/ui/styles/Theme.java` และ `src/ui/styles/Fonts.java` |

## วิธีทำงานของการเพิ่มหนังสือ

1. แอดมินเข้าสู่ระบบจากลิงก์ในหน้าเข้าสู่ระบบ
2. หน้าแรกของแอดมินมีการ์ด `เพิ่มหนังสือ`
3. กรอกข้อมูลหนังสือ แล้วเพิ่มชื่อตอนและเนื้อหาทีละตอน
4. เมื่อกดบันทึก `AdminBookLogic` ตรวจข้อมูล และ `AdminStorage` เขียนลง CSV
5. หนังสืออยู่ใน `data/books.csv` ส่วนเนื้อหาแต่ละตอนอยู่ใน `data/book_chapters`

## แก้ข้อมูลตัวอย่าง

- รายชื่อหนังสือตัวอย่างอยู่ใน `src/books/BookData.java`
- บัญชีสมาชิกอยู่ใน `data/users.csv`
- บัญชีแอดมินอยู่ใน `data/admins.csv`
- หมวดหมู่อยู่ใน `data/categories.csv`

ไฟล์ CSV มีหัวตารางแถวแรก ควรเก็บหัวตารางไว้เมื่อแก้ข้อมูล
