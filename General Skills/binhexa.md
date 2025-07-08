
# General Skills

## 🧩 Challenge: binhexa

### 📝 Description

bạn có thể thực hiện các phép toán cơ bản với phép toán nhị phân ?

> Link: https://play.picoctf.org/practice/challenge/414?category=5&page=1

## 🧠 Chiến lược giải

- tìm hiểu về các phép toán nhị phân cơ bản như : `*`, `|`, `+`, `<<`, `>>`.

### 🛠️ Cách giải

**1. kết nối với server qua câu lệnh sau:**

```
nc titan.picoctf.net 49191
```

-> nhận được 2 dữ liệu sau : number1 `00010111`, number2 `00001001`

**2. thực hiện phép dịch phải ( right shift `>>`) đối với number 2 `1 bit`**
   
```
- Khi dịch phải 1 bit:

  + Mỗi bit trượt sang phải 1 vị trí.

  + Bit bên trái nhất (bit cao nhất) sẽ được thêm 0.

  + Bit bên phải nhất (bit thấp nhất) bị loại bỏ.
```

-> kết quả : `00000100`

**3. thực hiện phép `OR` nhị phân (`|`)**
   
![image](https://github.com/user-attachments/assets/4bb72430-5399-4ad8-b113-0bdb26574ec4)

-> kết quả : `00011111`

**4. thực hiện phép `AND` nhị phân (`&`)**

![image](https://github.com/user-attachments/assets/7ef13522-4cb2-4bce-9668-d253ee56ac6a)

  -> kết quả : `00000001`

**5. thực hiện phép nhân nhị phân (`*`)**


  - number 1 : `00010111` -> thập phân : 1+2+4+16 = `23`
  - number 2 : `0000100`1 -> thập phân : 1 + 8 = `9`
    - lấy 23 * 9 = 207, chuyển `207` về nhị phân

![image](https://github.com/user-attachments/assets/5392e0ba-5ed0-4413-b192-9df31b47b037)


-> kết quả : `11001111`

**6. thực hiện phép cộng nhị phân (`+`)**

  - tương tự như nhân ta lấy 23 + 9 = `32`

  - sau đó chuyển `32` thành nhị phân :
  
  ![image](https://github.com/user-attachments/assets/f9314563-fa44-489e-af8b-9947ad5c4242)

-> kết quả : `00100000`

**7. thực hiện phép dịch trái ( left shift `>>`) đối với number 1 `1 bit`**
   
```
- Khi dịch phải 1 bit:

  + Mỗi bit trượt sang trái 1 vị trí.

  + Bit bên phải nhất (bit cao nhất) sẽ được thêm 0.

  + Bit bên trái nhất (bit thấp nhất) bị loại bỏ.
```

  -> kết quả : `00101110`

**8. chuyển kết quả cuối cùng `00101110` sang hệ 16 hexadecimal**

  - `001011101` chuyển sang thập phân : `46`
  
  - chuyển 46 sang hệ 16 bằng cách chia cho `16`
    
  ![image](https://github.com/user-attachments/assets/228451fd-10cf-4f06-b807-c5f0e9d39577)
  
    -> kết quả : `2E`

  
   

### 🏁 Flag
```
picoCTF{b1tw^3se_0p3eR@tI0n_su33essFul_6ab1ad84}
```

---

## 📚 Tổng Kết
- học được các phép toán nhị phân cơ bản và cách chuyển đổi giữa các hệ số
  
  
  ![image](https://github.com/user-attachments/assets/030e87cd-49cf-46dd-b9ec-3c4064df78e0)

