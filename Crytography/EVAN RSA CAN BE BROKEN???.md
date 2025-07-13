
# Crytography

## 🧩 Challenge: EVAN RSA CAN BE BROKE???

### 📝 Description

Dịch vụ này cung cấp cho bạn một lá cờ được mã hóa. Bạn có thể giải mã nó chỉ với N&e không?

> Link: https://play.picoctf.org/practice/challenge/470?category=2&page=1

## 🧠 Chiến lược giải

- tìm hiểu về hash ?
- tìm hiều về md5? sha256? sha1?

### 🛠️ Cách giải

1. kết nối với server qua câu lệnh sau:

```
nc verbal-sleep.picoctf.net 57192
```

2. Sử dụng trang web sau để kiểm tra `type` và `result` của `hash` sẽ lấy được flag

> Link: https://crackstation.net/

| **Hash** | **Type** | **Resule** |
|:--------:|:---------:|:---------:|
|482c811da5d5b4bc6d497ffa98491e38| md5 | password123 |

-> `md5` là một thuật toán băm mã hóa 1 chiều, nó nhận vào một chuỗi dự liệu bất kì và tạo ra một chuỗi hash cố định là **128bit ( 32 ký tự hex )**

| **Hash** | **Type** | **Resule** |
|:--------:|:---------:|:---------:|
|b7a875fc1ea228b9061041b7cec4bd3c52ab3ce3| sha1 | letmein |

-> `SHA-1` là một thuật toán băm mã hóa 1 chiều, nó nhận vào một chuỗi bất kì và xuất ra một chuỗi hash có độ dài cố dịnh là **160 bit (40 ký tự hex)**

| **Hash** | **Type** | **Resule** |
|:--------:|:---------:|:---------:|
|916e8c4f79b25028c9e467f1eb8eee6d6bbdff965f9928310ad30a8d88697745| sha256 | qwerty098 |

-> `SHA-256` là một thuật toán băm mã hóa 1 chiều thuộc họ `SHA-2` nhận vào một chuỗi ký tự bất kì và xuất ra chuỗi hash cố định với độ dài **256 bit (64 ký tự hex)**



### 🏁 Flag
```
picoCTF{UseStr0nG_h@shEs_&PaSswDs!_29028be8}
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
