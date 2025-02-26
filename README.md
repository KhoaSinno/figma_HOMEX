<div align="center">

# 🔖 Figma prototype  

## 🛖 HOSPITAL MANAGEMENT EXPERT SYSTEM

</div>

## 🔗 Project Resources

### 🎨 Figma  

- **[Figma Working Prototype](https://www.figma.com/design/xxXo1yWBvQtZoEjQ2t7lCW/Project-Figma---PYN---HTTT2211?node-id=34-47&p=f&t=6KAOhodyA2UltDyg-0)**  
- **[Figma Reference - Customer](https://www.figma.com/design/KaxD6zBpUpMq0sLqzwJX8H/DoctorHunt---Doctor-Consultant-Mobile-App-(Community)?node-id=0-1&p=f&t=yByZ9BQnSAxSQLQA-0)**  
- **Figma Reference - Admin:** _(Có trong Drive store)_  

### 📄 Documents  

- **[Drive store](https://drive.google.com/drive/folders/1mBtJBRh6lXeO76s_DRYE0q8tgLGPaQVD?usp=drive_link)**  
- **[Business Note](https://docs.google.com/document/d/1ya6UClV7KJTG5VzYEF8G8-yvrhJxeWHWIi_07qigAuI/edit?usp=sharing)**  
- **[Schedule Working](https://docs.google.com/spreadsheets/d/1VRaBpYTzO6Wa7p0dzqGcebUMFUa7zOEqVWh7437t3us/edit?usp=drive_link)**  

### 👀 Github: `KhoaSinno`

- **[figma_HOMEX](https://github.com/KhoaSinno/figma_HOMEX)**  

# 📌 Phân tích và Thiết kế Hệ thống Đặt lịch Khám bệnh Online  

## **1. Chức năng chính**  

- **🛠️ Quản trị viên (Admin):**  
  - Quản lý **bác sĩ, bệnh nhân, lịch khám bác sĩ**.  
  - Quản lý **blog, cuộc hẹn, giao dịch, danh sách hướng dẫn**.  
- **👤 Người dùng chung (None Actor):** Quản lý thông tin cá nhân (CRUD thông tin cá nhân, SignUp, SignIn, Logout, Forgot password, Change password).
- **🧑‍⚕️ Bệnh nhân (Patient):**  
  - Quản lý lịch khám cá nhân.  
  - Đặt lịch khám.  
  - Xem lịch hẹn cá nhân
  <!-- - Thanh toán trực tuyến qua **Ngân hàng, MoMo, VnPay**.   -->
- **👨‍⚕️ Bác sĩ (Doctor):**  
  - Quản lý cuộc hẹn bệnh nhân (CRUD).
  - Duyệt lịch khám bệnh nhân.
  - Quản lý lịch làm việc cá nhân (CRUD).  

## **2. Yêu cầu Thiết kế - PlantUML**  

- **📌 Use Case Diagram**.  
- **📌 Class Diagram**.  
- **📌 Sequence Diagram** `(⚠️Option)`.  

## **3. Các Thành phần Chính của Hệ thống**  

- **👤 User:** `Admin`, `Patient`, `Doctor`.  
- **📅 Appointment:** Quản lý lịch hẹn giữa bệnh nhân và bác sĩ.  
- **🏥 Specialty:** Danh mục chuyên khoa của bác sĩ.  
- **📆 ScheduleWork:** Lịch làm việc của bác sĩ.  
- **📝 Blog:** Hệ thống bài viết, hướng dẫn cho bệnh nhân.  

# 📌 Quy Trình Đặt Lịch Khám Bệnh 🏥  

## **1. Quy trình chuẩn**  

### **🔹 Bước 1: Đăng nhập / Đăng ký**  

- Người dùng mở ứng dụng trên điện thoại
- **Nếu đã có tài khoản** → Đăng nhập.  
- **Nếu chưa có tài khoản** → Đăng ký với thông tin cá nhân:  
  - Họ tên, SĐT, Email.  
  - Bảo hiểm y tế (nếu cần).  
- Hệ thống xác thực danh tính bằng OTP (qua SMS/Email).  

---

### **🔹 Bước 2: Chọn dịch vụ khám**  

- Người dùng chọn:  
  - **Loại khám**: Tổng quát, chuyên khoa, tái khám…  
  - **Hình thức**: Trực tiếp `hoặc từ xa (telemedicine)(⚠️Option)`.  
  - **Bác sĩ / Cơ sở y tế**: Lọc theo chuyên khoa, kinh nghiệm, khoảng cách.  
  - **Thời gian**: Chọn lịch trống từ hệ thống.  

---

### **🔹 Bước 3: Xác nhận & Thanh toán**  

- Hệ thống kiểm tra lịch trống.  
- Người dùng nhập **triệu chứng / ghi chú**.  
- Nếu có phí đặt cọc → Thanh toán qua:  
  - 🏦 Thẻ ngân hàng / Ví điện tử (MoMo, ZaloPay, VNPay…).
- Nhận xác nhận đặt lịch qua SMS/Email.  

---

### **🔹 Bước 4: Nhắc lịch & Check-in khám bệnh**  

- Hệ thống gửi thông báo nhắc lịch **trước 24h & 1h**.  
- Bệnh nhân đến phòng khám → **Mã đặt lịch`/ Check-in bằng mã QR(⚠️Option)`**.  
- Doctor xác nhận bệnh nhân đã đến.  

---

### **🔹 Bước 5: Bác sĩ thực hiện khám bệnh**  

- **Bác sĩ/Admin** đăng nhập hệ thống và chọn/tìm trên mã lịch hẹn trên điện thoại bệnh nhân.  
- Kiểm tra thông tin bệnh nhân, triệu chứng đã khai báo trước.  
- **Khám bệnh & chẩn đoán**:  
  - Cập nhật hồ sơ bệnh án (nếu có).  
  - Đưa ra chẩn đoán, nhập kết luận vào hệ thống.  
  <!-- - Lập đơn thuốc điện tử (nếu cần).   -->
  <!-- - Đề xuất lịch tái khám (nếu cần).   -->
- Cập nhật trạng thái lịch hẹn từ **"Chờ" → "Đã khám"**.  
- Gửi kết quả khám cho bệnh nhân qua ứng dụng (Gmail).  

---

<!-- ### **🔹 Bước 6: Thanh toán bổ sung (nếu có) & Hoàn thành**  

- Nếu có phát sinh thêm phí (xét nghiệm, thuốc…) → Hệ thống gửi yêu cầu thanh toán.  
- Bệnh nhân thanh toán ngay tại phòng khám hoặc qua ứng dụng.  
- Sau khi thanh toán xong → Lịch khám chuyển sang trạng thái **"Hoàn thành"**.  
- Hệ thống gửi email hóa đơn và đơn thuốc điện tử.  

--- -->

## **2. Xử lý các trường hợp ngoại lệ**  

### **❗ Bác sĩ hủy lịch hẹn**  

🔹 **Nguyên nhân**: Nghỉ đột xuất, sự cố phòng khám.  
✅ **Xử lý**:  

- **Admin** thông báo ngay cho bệnh nhân qua sđt/sms/email.  
- Đề xuất **bác sĩ khác** hoặc **lịch hẹn mới**.  
- Nếu bệnh nhân đã thanh toán, **hoàn tiền** hoặc đổi lịch.  

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
