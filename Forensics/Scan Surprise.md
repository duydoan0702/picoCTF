
# Forensics

## 🧩 Challenge: Scan Surprise

## 📝 Description
Tôi chán việc phát cờ dưới dạng chữ rồi.Sẽ tuyệt hơn nếu chúng được thể hiện bằng hình ảnh chứ ?


> Link: https://play.picoctf.org/practice/challenge/444?category=4&page=1

## 🧠 Chiến lược giải

- giải nén và tìm file .png sau đó tìm công cụ để giải mã QR đó.

## 🛠️ Cách giải

1. tìm file `flag.png`

2. sử dụng công cụ `zbariimg` để tìm flag

```
zbarimg flag.img
```

---

## 🏁 Flag

```
picoCTF{p33k_@_b00_19eccd10}

```

---

## 📚 Tổng Kết
- `Zbarimg` là một tiện ích dòng lệnh của thư viện `Zbar barcode Reader` dùng để quét và giải mã mã vạch, QR code và một số định khác từ file ảnh.
- Cú pháp cơ bản `zbarimg [tìu chọn] <file ảnh>`

