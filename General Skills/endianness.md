
# General Skills

## 🧩 Challenge: endianness

### 📝 Description
bạn có biết về little và big endian ?

> Link: https://play.picoctf.org/practice/challenge/414?category=5&page=1

## 🧠 Chiến lược giải
- tìm hiểu về little và big endian để giải.

### 🛠️ Cách giải

1. kết nối với server qua câu lệnh sau:

```
nc titan.picoctf.net 60831
```
-> dùng titan kết nối tới server
2. chuyển chuỗi dữ liệu thành
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
- Endian mô tả thứ tự sắp xếp các byte trong một giá trị nhiều byte (thường là 2, 4, 8 byte).
