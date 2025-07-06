
# General Skills

## 🧩 Challenge: Binary Search

### 📝 Description
use algorithm binary search to quickly find the flag ? you have 1000 possibilities and only 10 guesses.

> Link: https://play.picoctf.org/practice/challenge/442?category=5&page=1  

### 🛠️ Cách giải

1. Tải file chanllenge.zip
2. Dùng lệnh giải nén file hoặc kết nối trực tiếp máy chủ qua launch instance để chạy chương trình :

```
unzip challenge.zip
```

3. sử dụng thuật toán binary search để tìm flag :

```
int binarySearch(int arr[], int size, int target){
    int left = 0;
    int right = size-1;
    while( left <= right){
        // Tính chỉ số giữa
        int mid = (right + left) /2;
        if(arr[mid] == target){
            return mid;
        }
        else if(arr[mid] < target){
            // Tìm kiếm bên phải
            left = mid +1;
        }else{
            // Tìm kiếm bên trái
            right = mid - 1;
        }
    }
    return -1; // Trả về -1 nếu không tìm thấy
}
```

### 🏁 Flag

```
picoCTF{g00d_gu355_6dcfb67c}
```

---

## 📚 Tổng Kết

- **Binary Search** là thuật toán tìm kiếm trên mảng **đã sắp xếp**.
- Binary Search chia mảng làm đôi sau mỗi lần tìm kiếm
- Độ phức tạp thuật toán : **O(log n)**
