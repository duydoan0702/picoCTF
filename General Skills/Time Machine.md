
# General Skills

## 🧩 Challenge: FANTASY CTF

### 📝 Description
tôi vô tình viết flag may là tôi đã xóa nó.

> Link: https://play.picoctf.org/practice/challenge/471?category=5&page=1

## 🧠 Chiến lược giải
- Dùng lệnh `nc` (netcat) để kết nối đến máy chủ được chỉ định.
- Làm theo chỉ dẫn trong game text-based để giải đố, điều hướng và tìm flag.

### 🛠️ Cách giải

1. chạy lệnh sau để kết nối với chương trình:

```
nc verbal-sleep.picoctf.net 57327
```
-> `nc <host> <port>`

-> ctrl + C để thoát

2. làm theo hướng dẫn để tìm flag
   

### 🏁 Flag
```
picoCTF{m1113n1um_3d1710n_5e40d7b5}
```

---

## 📚 Tổng Kết
- netcat(nc) là công cụ phổ biến trong ctf để giao tiếp với chương trình từ xa thông qua cổng mạng.
- làm quen với terminal
