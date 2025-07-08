# General Skills

## 🧩 Challenge: Super SSH

### 📝 Description
Một chương trình làm quen với kết SSH.

> Link: https://play.picoctf.org/practice/challenge/424?category=5&page=1

---

## 🧠 Chiến lược giải
- tìm hiểu cách kết nối ssh và làm theo yêu cầu đề.

---

## 🛠️ Cách giải

1. ghi lệnh sau để kết nối và tìm flag
```
ssh ctf-player@titan.picoctf.net -p 53668
```
-> câu lệnh tổng quát `ssh username@hostname` `-p` để chỉnh định port


## 🏁 Flag
```
picoCTF{s3cur3_c0nn3ct10n_8969f7d3}
```

## 📚 Tổng Kết
-> SSH là một giao thức mã hóa cho phép bạn kết nối an toàn tơi một máy tính từ xá, để quản trị hệ thống hoặc thực hiện các tác vụ từ dòng lệnh.
