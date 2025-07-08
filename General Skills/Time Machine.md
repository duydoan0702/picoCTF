
# General Skills

## 🧩 Challenge: Time Machine

### 📝 Description
lần cuối tôi làm việc gì ? tôi nhớ đã note lại để giúp tôi nhớ lại

> Link: https://play.picoctf.org/practice/challenge/425?category=5&page=1

## 🧠 Chiến lược giải
- kiểm tra lịch sử commit để tìm note.

### 🛠️ Cách giải

1. tải file về rồi giải nén bằng lệnh sau:

```
unzip challenge.zip
```

2. kiểm tra lịch sử commit và tìm flag:
```
git log
```
-> hiện commit history 

### 🏁 Flag
```
picoCTF{t1m3m@ch1n3_b476ca06}
```

---

## 📚 Tổng Kết
- lịch sử commit có thể lưu lại quá trình làm việc và có thể tìm lại các file bị xóa các thay đổi trong quá trình làm việc.
