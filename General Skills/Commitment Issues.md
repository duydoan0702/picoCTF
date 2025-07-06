
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

3. kiểm tra các commit 

```
git log
```
-> liệt kê các commit
```
cd drop-in
```
-> chuyển tới thư mục vừa giải nén ra

4. kiểm tra các commit tìm file mà họ đã lỡ xóa nhưng git vẫn lưu
```
git checkout ...
```
-> kiểm tra và tìm ra flag

### 🏁 Flag
-> flag nằm ở file message.txt mà người dùng đã lỡ xóa
```
picoCTF{s@n1t1z3_c785c319}
```

---

## 📚 Tổng Kết
- làm quen với git để xem lại lịch sử commit
- tìm lại các thông tin đã bị thay đổi hoặc bị xóa
