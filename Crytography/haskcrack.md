
# Crytography

## 🧩 Challenge: hashcrack

### 📝 Description

Một công ty đã lưu một thông điệp bí mật trên máy chủ và thông điệp này dã bị xâm phạm do quản trị viên sử dụng mật khẩu băm yếu. Bạn có thể truy cập thông điệp lưu trên máy chủ không ?

> Link: https://play.picoctf.org/practice/challenge/475?category=2&page=1

## 🧠 Chiến lược giải

- tìm hiểu về hash ?
- tìm hiều về md5? sha256? sha1?

### 🛠️ Cách giải

1. kết nối với server qua câu lệnh sau:

```
nc verbal-sleep.picoctf.net 57192
```

2. Sử dụng trang web sau để kiểm tra `type` và `result` của `hash`

> Link: https://crackstation.net/

| **Hash** | **Type** | **Resule** |
|:--------:|:---------:|:---------:|
|482c811da5d5b4bc6d497ffa98491e38| md5 | password123 |

-> `md5` là một thuật toán băm mã hóa 1 chiều, nó nhận vào một chuỗi dự liệu bất kì và tạo ra một chuỗi hash cố định là **128bit ( 32 ký tự hex )**






   

### 🏁 Flag
```
picoCTF{t1m3m@ch1n3_b476ca06}
```

---

## 📚 Tổng Kết

| **Nội dung**            | **Giải thích**                                                                                   |
|:------------------------|:------------------------------------------------------------------------------------------------|
| **Hash là gì?**           | Là giá trị mã hóa một chiều đại diện cho dữ liệu. Chỉ cần thay đổi một chút dữ liệu, hash sẽ khác hoàn toàn. |
| **Ứng dụng**              | Kiểm tra tính toàn vẹn dữ liệu, lưu mật khẩu an toàn.                                           |
| **Tính chất của hash**    | - Không thể khôi phục dữ liệu gốc từ hash. <br> - Rất nhạy với thay đổi nhỏ nhất của dữ liệu.     |
| **Thuật toán phổ biến**   | SHA-2 (ví dụ: SHA-256)                                                                          |
| **Tấn công hash**         | - Dùng bảng tra cứu (lookup table) hoặc từ điển mật khẩu (dictionary attack). <br> - Giải pháp: đặt mật khẩu ngẫu nhiên, phức tạp. |
| **Challenge thực hành**   | Dò tìm mật khẩu dựa trên hash SHA256 và danh sách `rockyou.txt` bằng Python.                     |


