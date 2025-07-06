
# General Skills

## 🧩 Challenge: Commmitment Issues

### 📝 Description
tôi vô tình viết flag may là tôi đã xóa nó.

> Link: https://play.picoctf.org/practice/challenge/411?category=5&page=1

## 🧠 Chiến lược giải
- kiểm tra các thay đổi trong lịch sử commit để tìm flag

### 🛠️ Cách giải

1. Tải file chanllenge.zip
2. Dùng lệnh giải nén file.

```
unzip challenge.zip
```

3. sau đó dùng lệnh để xem các file đã giải nén

```
ls
```
-> liệt kê các file đã giải nén
```
cd drop-in
```
-> chuyển tới thư mục vừa giải nén ra

4. dùng lệnh để xem ai là người commit lên git làm ngừng code
```
git log message.py
```
-> xem lịch sử commit đối với file message.py

### 🏁 Flag
-> flag nằm ở author 
```
picoCTF{@ak_th3_1nt3rn_b64c4705}
```

---

## 📚 Tổng Kết
- làm quen với **git log** câu lệnh để kiểm tra lịch sử commit
