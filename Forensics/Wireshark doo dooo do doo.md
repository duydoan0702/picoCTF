
# Forensics

## 🧩 Challenge: Wireshark doo dooo do doo

## 📝 Description
Bạn có thể tìm được flag ?

> Link: https://play.picoctf.org/practice/challenge/115category=4&page=1

## 🧠 Chiến lược giải
- Tìm thử flag ở dạng plantext nếu không có chúng ta tìm các gói **http** và theo dõi **stream** của chúng.

## 🔧 Công cụ 
### 1. **wireshark**
- Là công cụ **phân tích lưu lượng mạng(network traffic analyzer)** . Nó cho phép bạn:
    + Ghi lại **(capture)** các gói tin trên mạng
    + Xem chi tiết từng gói tin
    + Phân tích giao tiếp giữa client và server
    + Tìm lỗi hoặc flag trong file `.pcap`, `pcapng`
- Các câu lệnh hay dùng:

| **Cú pháp**                               | **Mô tả**                                                  |
|-------------------------------------------|-------------------------------------------------------------|
| `ip.addr == 192.168.1.1`                  | Gói tin có IP nguồn hoặc đích là `192.168.1.1`              |
| `http`                                    | Lọc tất cả gói HTTP                                         |
| `tcp.port == 80`                          | Gói tin có TCP port 80                                      |
| `frame contains "picoCTF"`               | Gói nào chứa chuỗi `"picoCTF"`                              |
| `tcp.payload`                             | Truy cập payload TCP                                        |
| `http.request.method == "GET"`           | Các gói HTTP sử dụng phương thức GET                        |

> 📌 Gợi ý: Bạn có thể kết hợp nhiều điều kiện với `&&`, `||`, và `!` để tạo bộ lọc phức tạp hơn.

## 🛠️ Cách giải

### 1. Tìm flag ở dạng rõ ( plantext )

```
tcp.payload contains "picoCTF"
```
- filter vào thanh Display filter
### 2.Xem tổng quan lưu lượng

```
Statistics -> Protocal Hierarchy
```
- Xem giao thức nào chiếm đa số để tập trung vào phân tích đúng hướng

### 3. Lọc HTTP và theo dõi từng luồng (TCP stream)

```
http
```
- filter vào thanh Display Filter, sau đó chọn gói đầu tiên chọn `Follow` -> `TCP stream`

### 4. Tìm flag trong TCP Stream

```
cvpbPGS{c33xno00_1_f33_h_qrnqorrs}
```
- bạn sẽ tìm thấy dòng sau ở tcp stream số 5

### 5.Ta thấy flag ở dụng `ROT13`
> link: https://rot13.com/

- sử dụng web sau để giải mã ROT13


---

## 🏁 Flag

```
picoCTF{p33kab00_1_s33_u_deadbeef}

```

