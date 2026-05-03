# 📊 Google Play Store Data Analysis

## 🎯 Objective
Phân tích dữ liệu Google Play Store nhằm hiểu đặc điểm của các ứng dụng và xác định các yếu tố ảnh hưởng đến rating, từ đó tìm ra loại ứng dụng có tiềm năng phát triển.

---

## 📂 Dataset
- Nguồn: Google Play Store dataset  
- Bao gồm các thông tin:
  - App name
  - Category
  - Rating
  - Reviews
  - Price
  - ...

---

## ⚙️ Data Cleaning
Các bước xử lý dữ liệu:
- Xóa các giá trị thiếu (`dropna`)
- Xóa dữ liệu trùng lặp theo App (`drop_duplicates`)
- Sắp xếp theo số lượng reviews để giữ lại dữ liệu tốt nhất
- Chuyển đổi kiểu dữ liệu:
  - `Reviews` → float  
  - `Rating` → float  
  - `Price` → float (loại bỏ ký tự `$`)

---

## 🔍 Analysis

### 1. Tổng quan rating
- Tính mean, max, min của rating

### 2. So sánh Free vs Paid
- So sánh rating trung bình giữa ứng dụng miễn phí và trả phí

### 3. Phân tích theo Category
- Sử dụng `groupby` để tính:
  - Rating trung bình
  - Số lượng ứng dụng
- Lọc các category có đủ dữ liệu để đảm bảo độ tin cậy

### 4. Phân tích Rating và Reviews
- Đánh giá độ tin cậy của rating dựa trên số lượng reviews

---

## 📊 Visualization
- Biểu đồ bar chart thể hiện rating trung bình theo category
- Giúp so sánh trực quan giữa các nhóm ứng dụng

---

## 💡 Key Insights

- Phần lớn ứng dụng có rating khá cao (~4.17), cho thấy mức độ hài lòng chung của người dùng ở mức tốt  
- Ứng dụng trả phí có rating cao hơn ứng dụng miễn phí, tuy nhiên chênh lệch không lớn  
- Một số category có rating cao nhưng số lượng ứng dụng thấp, có thể gây bias trong phân tích  
- Các category có nhiều ứng dụng và rating ổn định sẽ phản ánh xu hướng người dùng chính xác hơn  

---

## 📖 Data Storytelling

Phân tích dữ liệu cho thấy phần lớn ứng dụng trên Google Play có rating cao, phản ánh chất lượng chung của nền tảng. Mặc dù các ứng dụng trả phí có rating nhỉnh hơn, nhưng ứng dụng miễn phí vẫn chiếm phần lớn thị trường và có khả năng cạnh tranh tốt.

Bên cạnh đó, sự khác biệt giữa các category cho thấy không phải lĩnh vực nào cũng có mức độ hài lòng giống nhau. Một số category có rating cao nhưng thiếu dữ liệu, điều này có thể làm sai lệch kết quả phân tích.

Từ đó, có thể kết luận rằng nên tập trung vào các category có nhiều ứng dụng và rating ổn định để đảm bảo tiềm năng phát triển lâu dài.

---

## 🛠️ Technologies Used
- Python  
- Pandas  
- Matplotlib  

---

## 🚀 Project Structure

