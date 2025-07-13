
# Crytography

## 🧩 Challenge: EVAN RSA CAN BE BROKE???

### 📝 Description

Dịch vụ này cung cấp cho bạn một lá cờ được mã hóa. Bạn có thể giải mã nó chỉ với N&e không?

> Link: https://play.picoctf.org/practice/challenge/470?category=2&page=1

## 🧠 Chiến lược giải
- tìm hiểu về thuật toán mã hóa **RSA**

### 🛠️ Cách giải

1. kết nối với server qua câu lệnh sau:

```
nc verbal-sleep.picoctf.net 55822
```

2. Sau khi kết nối bạn nhận lại được dữ liệu sau

<img width="938" height="102" alt="image" src="https://github.com/user-attachments/assets/4baf233d-8170-43e1-8995-5d734572ce67" />

- `N` : modules trong RSA
- `e = 65337` : public exponent
- `cyphertext` : bản mã hóa của flag
-> Giải mã `cyphertext` khi chỉ biết `N` và `e`

3. Dùng trang web sau để giải mã `RSA`

> link: https://www.dcode.fr/rsa-cipher
> web này chỉ giải được `RSA` yếu.

-> ta nhập `N`, `e`, và `cyphertext` để lấy `flag`

### 🏁 Flag
```
picoCTF{tw0_1$_pr!m3f995d086}
```

---

## 📚 Tổng Kết
- `RSA` là một thuật toán mã hóa công khai phổ biến hiện nay, dùng trong: gửi tin nhắn mã hóa, chữ ký số, HTTPS, SSH,...
