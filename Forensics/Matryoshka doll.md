
# Forensics

## 🧩 Challenge: Matryoshka doll
- Búp bê Matryoshka là một bộ búp bê bằng gỗ có kích thước giảm dần được đặt lồng vào nhau. Vậy búp bê cuối cùng là gì?

## 📝 Description

> Link: https://play.picoctf.org/practice/challenge/129?category=4&page=1&search=doll

## 🧠 Chiến lược giải
- kiểm tra các file ảnh có chứa dữ liệu ẩn không và giải nén các lớp của file ảnh đề tìm flag

## 🔧 Công cụ 
1, **binwalk**
- kiểm tra ảnh có chứa file zip, ảnh PNG khác, hoặc nội dung khác không.
- câu lệnh:

```
binwalk dolls.jpg
```



## 🛠️ Cách giải

1. dùng câu lệnh `binwalk` để kiểm tra dữ liệu ẩn của file

```
binwalk dolls.jpg
```

2. sử dụng `binwalk` để giải nén

```
binwalk -e dolls.jpg
```
- `-e` để giải nén các file ẩn tìm được

3. giải nén làn lược các file ảnh cho đến khi tìm được `flag.txt`
---

## 🏁 Flag

```
picoCTF{4cf7ac000c3fb0fa96fb92722ffb2a32}

```

---

## 📚 Tổng Kết
-  một file ảnh có thể chứa nhiều lớp dữ liệu trong đó, ta có thể dùng công cụ như `binwalk`, `string`, `exiftool` để tìm dữ liệu ẩn trong đó.
