
# General Skills

## 🧩 Challenge: Collbaretive Development

### 📝 Description
một nhóm đã code một chức năng mới cho chương trình print flag. Hãy tìm hiểu họ làm việc như thế nào?

> Link: https://play.picoctf.org/practice/challenge/410?category=5&page=1

## 🧠 Chiến lược giải
- kiểm tra các nhánh mà họ đã làm việc với chức năng trên để tìm ra flag

### 🛠️ Cách giải

1. Tải file chanllenge.zip
2. Dùng lệnh giải nén file.

```
unzip challenge.zip
```

3. vì học đã phát triển một chức mới nên ta kiểm tra các nhánh 

```
git branch
```
![image](https://github.com/user-attachments/assets/62ccea76-c4c1-46b2-9b9e-d12bbe21affa)

-> liệt kê các nhánh và nhánh ta đang ở

4. chuyển nhánh và kiểm tra từng nhánh 
```
git checkout feature/part-1
```
-> chuyển sang nhánh feature/part-1

5. kiểm tra các file trong nhánh và tìm flag
```
ls
cat flag.py
```

### 🏁 Flag
-> flag nằm ở 3 file flag.py của 3 nhánh
```
picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_7ae8dd33}
```

---

## 📚 Tổng Kết
- làm quen với **git branch** để làm việc nhóm trên githup
