
# General Skills

## 🧩 Challenge: endianness

### 📝 Description
bạn có biết về little và big endian ?

> Link: https://play.picoctf.org/practice/challenge/414?category=5&page=1

## 🧠 Chiến lược giải
- tìm hiểu về **little edian** và **big endian** để giải.
- biến chuỗi kí tự thành mã dạng hex, sau đó sắp xếp lại theo đúng quy tắc của edian.

### 🛠️ Cách giải

1. kết nối với server qua câu lệnh sau:

```
nc titan.picoctf.net 60831
```

2. chuyển chuỗi dữ liệu được cung cấp
```
brbgk
```
-> mã hex : ` 62 72 62 72 eb `, dựa theo bảng ascii : https://vi.wikipedia.org/wiki/ASCII

3. chuyển đổi và nhận flag:
   -> **little edian** : `6b67627262`
   
   -> **big edian** : `626762676b`

### 🏁 Flag
```
picoCTF{t1m3m@ch1n3_b476ca06}
```

---

## 📚 Tổng Kết
- **Endian** là khái niệm mô mả thứ tự sắp xếp byte trong bộ nhớ.
    - **little edian** : byte quan trọng nhất đứng sau, lưu theo thứ tự byte từ nhỏ đến lớn
    - **big edian** : byte quan trọng nhất đứng trước , thứ tự ngược lại từ lớn đến nhỏ.
- nếu cần hiểu rõ hơn truy cập link sau : https://levelup.gitconnected.com/little-endian-and-big-endian-74ab6441b2a7


