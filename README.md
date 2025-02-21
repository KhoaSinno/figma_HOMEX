<div align="center">

# 🔖 Figma prototype  

## 🛖 HOSPITAL MANAGEMENT EXPERT SYSTEM

</div>

## 🔗 Project Resources  

### 🎨 Figma  

- **[Figma Working Prototype](https://www.figma.com/design/xxXo1yWBvQtZoEjQ2t7lCW/Project-Figma---PYN---HTTT2211?node-id=34-47&p=f&t=6KAOhodyA2UltDyg-0)**  
- **[Figma Reference - Customer](https://www.figma.com/design/KaxD6zBpUpMq0sLqzwJX8H/DoctorHunt---Doctor-Consultant-Mobile-App-(Community)?node-id=0-1&p=f&t=yByZ9BQnSAxSQLQA-0)**  
- **Figma Reference - Admin:** _(Chưa có link)_  

### 📄 Documents  

- **[Business Note](https://docs.google.com/document/d/1ya6UClV7KJTG5VzYEF8G8-yvrhJxeWHWIi_07qigAuI/edit?usp=sharing)**  
- **[Schedule Working](https://docs.google.com/spreadsheets/d/1VRaBpYTzO6Wa7p0dzqGcebUMFUa7zOEqVWh7437t3us/edit?usp=drive_link)**  

### 👀 Github: `KhoaSinno`

- **[figma_HOMEX](https://github.com/KhoaSinno/figma_HOMEX)**  

# 📌 Phân tích và Thiết kế Hệ thống Đặt lịch Khám bệnh Online  

## **1. Chức năng chính**  

- **🛠️ Quản trị viên (Admin):**  
  - Quản lý **bác sĩ, bệnh nhân, lịch khám bác sĩ**.  
  - Quản lý **blog, cuộc hẹn, giao dịch, danh sách hướng dẫn**.  
- **👤 Người dùng chung (None Actor):** Quản lý thông tin cá nhân.
- **🧑‍⚕️ Bệnh nhân (Patient):**  
  - Quản lý lịch khám cá nhân.  
  - Đặt lịch khám.  
  - Thanh toán trực tuyến qua **Ngân hàng, MoMo, VnPay**.  
- **👨‍⚕️ Bác sĩ (Doctor):**  
  - Quản lý lịch khám bệnh nhân.
  - Duyệt lịch khám bệnh nhân.
  - Quản lý lịch làm việc cá nhân.  
- **🛎️ Lễ tân (Receptionist):** Duyệt lịch khám.  

## **2. Yêu cầu Thiết kế - PlantUML**  

- **📌 Use Case Diagram**.  
- **📌 Class Diagram**.  
- **📌 Sequence Diagram**.  

## **3. Các Thành phần Chính của Hệ thống**  

- **👤 User:** `Admin`, `Patient`, `Doctor`, `Receptionist`.  
- **📅 Appointment:** Quản lý lịch hẹn giữa bệnh nhân và bác sĩ.  
- **🏥 Specialty:** Danh mục chuyên khoa của bác sĩ.  
- **📆 ScheduleWork:** Lịch làm việc của bác sĩ.  
- **📝 Blog:** Hệ thống bài viết, hướng dẫn cho bệnh nhân.  
