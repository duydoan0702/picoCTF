
# Forensics

## 🧩 Challenge: Glory of the Garden
- file ảnh này chứa nhiều điều hơn bạn nghĩ.

## 📝 Description

> Link: https://play.picoctf.org/practice/challenge/44?category=4&page=1

## 🧠 Chiến lược giải
- kiểm tra dữ liệu
- kiểm tra **Embebded String** ( là một chuỗi văn bản nhúng trực tiếp vào file nhị phân như ảnh, audio, video, PDF, ...)

## 🔧 Công cụ 
1, **exiftool**
- giúp đọc, ghi và chỉnh sửa metadata( siêu dữ liệu) của **ảnh(.jpg, .png,..) , video, PDF, audio,..**
- Phân tích **Exif, IPTC, XMP, JFIF, MakerNotes,...**
-> sử dụng câu lệnh sau đề cài đặt:
```
sudo apt install exiftool
```
2. **strings**
- là công cụ dùng để kiểm tra tất cả các chuỗi ASCII hoặc Unicode có thể đọc được trong file ảnh
- câu lệnh:
```
strings filename
```

3.**binwalk**
-  kiểm tra ảnh có chứa file zip, ảnh PNG khác, hoặc nội dung nhúng khác không.
-  câu lênh:
```
binwalk garden.jpg
```

## 🛠️ Cách giải

1. Sử dụng câu lệnh để kiểm tra dữ liệu của ảnh

```
exiftool garden.jpg
```
- ta thấy không có flag trong dữ liệu của ảnh

2. Sử dụng `strings` kiểm tra text ẩn

```
strings garden.jpg
```
- ta tìm được `flag` ở cuối text
---

## 🏁 Flag

```
picoCTF{more_than_m33ts_the_3y3eBdBd2cc}

```

---

## 📚 Tổng Kết
- ta được cách sử dụng các công cụ như: `exiftool`, `strings`, `binwalk` để kiểm tra thông tin giấu trong ảnh. 
