# Dữ liệu và Cơ sở dữ liệu

## Dữ liệu
- Là những thông tin rời rạc.

## Cơ sở dữ liệu
- Chương trình, hệ thống, nơi lưu trữ dữ liệu cho ứng dụng đang phát triển.
- Dữ liệu lưu trữ gắn với ngữ nghĩa cụ thể (cần thiết cho dự án).
- Là tập hợp các **bảng (table)** dữ liệu, mỗi bảng gồm nhiều **cột (columns)** và **hàng (rows)**.

---

# SQL (Structured Query Language)
- Ngôn ngữ truy vấn: tập hợp các lệnh cho phép thao tác với dữ liệu trong cơ sở dữ liệu.
- Các thao tác truy vấn:
  - **Thêm** dữ liệu.
  - **Sửa** dữ liệu.
  - **Xóa** dữ liệu.
  - **Lấy** dữ liệu ra.

---

# RDBMS (Hệ quản trị CSDL)
- Là chương trình hệ thống cho phép người dùng:
  - Tạo cơ sở dữ liệu.
  - Cung cấp ngôn ngữ truy vấn để thao tác với dữ liệu.

---

# Các bước thiết kế cơ sở dữ liệu

## B1: Mô hình quan niệm
1. **Xác định yêu cầu:**
   - Xác định các **đối tượng**, **thuộc tính** cần lưu trữ.
   - Thuộc tính có thể là đơn trị (số, chuỗi), danh sách hoặc đối tượng.
   - Không yêu cầu phải chính xác 100% ngay lập tức.

## B2: Mô hình logic
- Hai cách tiếp cận:
  1. **ERD (Entity Relationship Diagram):** Vẽ sơ đồ trực quan (thường dùng cho báo cáo, khách hàng).
  2. **Mẫu tin:** Ghi chú nhanh, không cần vẽ (thực hiện nhanh chóng).

### Các bước cụ thể:
1. **Xác định tập thực thể:**
   - Đối tượng (B1) → Tập thực thể (B2).
   - Java tương ứng: `class` (tập thực thể) và `object` (thực thể).

2. **Xác định thuộc tính:**
   - Từ thuộc tính (B1) → Thuộc tính (B2).
   - Loại thuộc tính: đơn trị, đa trị, kết hợp, dẫn xuất.

3. **Xác định khóa:**
   - Yêu cầu: Dữ liệu phải là kiểu đơn (số, chuỗi, ngày/tháng/năm).
   - Loại quan hệ: 1-1, 1-n, n-n.

4. **Xác định mối quan hệ giữa các tập thực thể.**

## B3: Mô hình quan hệ (vật lý - database)
1. **Xác định bảng (TABLE):**
   - Tập thực thể (B2) → Bảng (B3).

2. **Xác định cột (COLUMNS):**
   - Thuộc tính (B2) → Cột (B3).

3. **Xác định khóa chính (PRIMARY KEY):**
   - Từ khóa (B2) → Khóa chính (B3).
   - Mỗi bảng có **tối đa 1 khóa chính** (hoặc không có).

4. **Xác định khóa ngoại (FOREIGN KEY):**
   - Dựa vào mối quan hệ (B2):
     - **1-1:** Cách tạo khóa ngoại.
     - **1-n:** Cách tạo khóa ngoại (hoặc n-1).
     - **n-n:** Cách tạo khóa ngoại.

     
