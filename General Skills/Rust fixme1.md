# General Skills

## 🧩 Challenge: Rust: fixme1

### 📝 Description
Một chương trình Rust nhỏ bị lỗi, bạn cần sửa nó để in ra flag.

> Link: https://play.picoctf.org/practice/challenge/461?category=5&page=1

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
   
![image](https://github.com/user-attachments/assets/d605c267-a4ad-4c54-8a8b-359c640c4725)

-> trong `Rust` khi trả về giá trị của một hàm không dùng `ret` mà dùng `return;`
-> kết thúc câu lệnh bằng `;`
-> truyền biến vào println thêm `{}` và truyền biến sau dấu `,`

3. run code bằng câu lệnh `cargo run` và thấy flag

## 🏁 Flag
```
picoCTF{4r3_y0u_4_ru$t4c30n_n0w?}
```

## 📚 Tổng Kết
-> Làm quen với cú pháp cơ bản của Rust:

   - Dấu ; để kết thúc lệnh

   - return thay vì ret

   - Cách truyền biến vào println!






