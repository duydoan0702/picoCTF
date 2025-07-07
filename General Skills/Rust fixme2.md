# General Skills

## 🧩 Challenge: Rust: fixme2

### 📝 Description
Một chương trình Rust nhỏ bị lỗi, bạn cần sửa nó để in ra flag.

> Link: https://play.picoctf.org/practice/challenge/462?category=5&page=1

---

## 🧠 Chiến lược giải
- Đọc hiểu mã nguồn Rust
- Nhận diện lỗi cú pháp hoặc logic
- Chạy chương trình để lấy flag

---

## 🛠️ Cách giải

1. **Tải và giải nén tệp bài:**
```
unzip challenge.zip
```
2. Mở file `main.rs` và sửa lỗi.
   
![image](https://github.com/user-attachments/assets/dc58a442-3e6c-4e80-abe8-4cb52305cb3c)

-> khai báo `mut` cho biến cần thay đổi

-> truyền tham chiều `&mut` và biến tham chiếu muốn thay dổi giá trị

3. run code bằng câu lệnh `cargo run` và thấy flag

## 🏁 Flag
```
picoCTF{4r3_y0u_h4v1n5_fun_y31?}
```

## 📚 Tổng Kết
-> `Ownership` quyền sở hữu trong `Rust` : mỗi giá trị chỉ có 1 chủ sở hữu
-> `References` thâm chiếu : thay vì chuyển đổi chủ sở hữu ta tham chiếu `&`
    - tham chiếu không thể thay đổi giá trị nên ta dùng `&mut`
