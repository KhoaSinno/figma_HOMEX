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

# 📌 Quy Trình Đặt Lịch Khám Bệnh 🏥  

## **1. Quy trình chuẩn**  

### **🔹 Bước 1: Đăng nhập / Đăng ký**  

- Người dùng mở ứng dụng / trang web.  
- **Nếu đã có tài khoản** → Đăng nhập.  
- **Nếu chưa có tài khoản** → Đăng ký với thông tin cá nhân:  
  - Họ tên, SĐT, Email.  
  - CCCD/Bảo hiểm y tế (nếu cần).  
- Hệ thống xác thực danh tính bằng OTP (qua SMS/Email).  

---

### **🔹 Bước 2: Chọn dịch vụ khám**  

- Người dùng chọn:  
  - **Loại khám**: Tổng quát, chuyên khoa, tái khám…  
  - **Hình thức**: Trực tiếp hoặc từ xa (telemedicine).  
  - **Bác sĩ / Cơ sở y tế**: Lọc theo chuyên khoa, kinh nghiệm, khoảng cách.  
  - **Thời gian**: Chọn lịch trống từ hệ thống.  

---

### **🔹 Bước 3: Xác nhận & Thanh toán**  

- Hệ thống kiểm tra lịch trống.  
- Người dùng nhập **triệu chứng / ghi chú**.  
- Nếu có phí đặt cọc → Thanh toán qua:  
  - 🏦 Thẻ ngân hàng / Ví điện tử (MoMo, ZaloPay, VNPay…).  
  - 📑 Thanh toán bảo hiểm (nếu áp dụng).  
- Nhận xác nhận đặt lịch qua SMS/Email.  

---

### **🔹 Bước 4: Nhắc lịch & Khám bệnh**  

- Hệ thống gửi thông báo nhắc lịch **trước 24h & 1h**.  
- Bệnh nhân đến phòng khám → **Check-in (Quét QR / Nhập mã đặt lịch)**.  
- Bác sĩ khám bệnh, cập nhật hồ sơ sức khỏe.  
- Sau khám:  
  - Nhận đơn thuốc điện tử / lịch tái khám (nếu có).  

---

## **2. Xử lý các trường hợp ngoại lệ**  

### **❗ Bác sĩ hủy lịch hẹn**  

🔹 **Nguyên nhân**: Nghỉ đột xuất, sự cố phòng khám.  
✅ **Xử lý**:  

- Thông báo ngay cho bệnh nhân.  
- Gợi ý bác sĩ khác hoặc lịch mới.  
- Nếu bệnh nhân đã thanh toán, hoàn tiền hoặc đổi lịch.  

---

### **❗ Bệnh nhân hủy lịch**  

🔹 **Nguyên nhân**: Bận, quên, không cần khám nữa.  
✅ **Xử lý**:  

- Nếu hủy **trước 24h** → Hoàn tiền.  
- Nếu hủy **sát giờ (<2h)** → Mất phí đặt cọc.  
- Gợi ý đặt lịch lại.  

---

### **❗ Bệnh nhân đến muộn**  

🔹 **Nguyên nhân**: Kẹt xe, quên lịch.  
✅ **Xử lý**:  

- Nếu muộn **<15 phút** → Bác sĩ có thể vẫn khám.  
- Nếu **>30 phút** → Lịch hẹn có thể bị hủy.  
- Gợi ý đặt lịch lại vào khung giờ trống tiếp theo.  

---

### **❗ Hệ thống lỗi hoặc quá tải**  

🔹 **Nguyên nhân**: Server quá tải, lỗi thanh toán.  
✅ **Xử lý**:  

- Hiển thị thông báo lỗi rõ ràng.  
- Nếu lỗi thanh toán, kiểm tra & hoàn tiền nếu cần.  

---

### **❗ Bệnh nhân không đến khám (No-show)**  

🔹 **Nguyên nhân**: Không thông báo trước.  
✅ **Xử lý**:  

- Gửi **nhắc nhở 1 giờ trước** để xác nhận.  
- Nếu không phản hồi → **Mở slot cho người khác**.  
- Nếu liên tục vắng mặt → **Hạn chế đặt lịch trong tương lai**.  

---
