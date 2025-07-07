# General Skills

## 🧩 Challenge: Rust: fixme3

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
   

![image](https://github.com/user-attachments/assets/a84c928b-09dd-4bff-b6e2-72f6d5aa9279)

-> dùng hàm unsafe bằng có bỏ comment dòng lệnh đó

3. run code bằng câu lệnh `cargo run` và thấy flag

## 🏁 Flag
```
picoCTF{n0w_y0uv3_f1x3d_1h3m_411}
```

## 📚 Tổng Kết
-> nếu không muốn theo các nguyên tắc của `Rust fixme2` ta dùng hàm `unsafe`
