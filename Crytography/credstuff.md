
# Forensics

## 🧩 Challenge: credstuff
- file ảnh này chứa nhiều điều hơn bạn nghĩ.

## 📝 Description
Chúng tôi phát hiện rò rỉ thông tin đăng nhập trên web chợ đen. Bạn có thể tìm thấy mật khẩu của người dùng cultiris và giải mã thành công không ?

> Link: https://play.picoctf.org/practice/challenge/261?category=2&page=1

## 🧠 Chiến lược giải
- tìm **password** của người dùng **cultiris**

## 🔧 Công cụ 
1. **grep**
- Tìm dòng chứa từ khóa trong file hoặc thư mục
- câu lệnh:

```
grep "chuỗi" file.txt
```
- `-n` hiện cả số dòng

2.**sed**
- Xử lý dòng văn bản: in, thay thế, xóa, chỉnh sửa, lọc dòng.
- câu lệnh:

```
sed -n 10p file.txt
```
- in ra dòng số 10


## 🛠️ Cách giải

1. Giải nén thư mục đã cho

```
tar -xf leak.tar
```

2. Tìm người dùng `cultiris` đang ở dòng số bao nhiêu
```
grep -n cultiris usernames.txt
```

3. Sau khi tìm được vị trí người dùng, ta tìm **password** tương ứng.

```
sed -n 378 passowrds.txt
```
- ta nhập được passowrd như sau : `cvpbPGS{P7e1S_54I35_71Z3}`

4. Ta thấy password được mã hóa `ROT13`
>link: https://rot13.com/
- ta sử dụng trang web sau để mã hóa.
---

## 🏁 Flag

```
picoCTF{C7r1F_54V35_71M3}

```

---

