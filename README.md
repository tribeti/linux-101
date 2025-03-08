# Tài liệu tổng hợp lệnh trong Linux (Ubuntu)

## Mục lục
1. [Bắt đầu với Terminal](#bắt-đầu-với-terminal)
2. [Thao tác với thư mục](#thao-tác-với-thư-mục)
    - [Tạo thư mục mới](#tạo-thư-mục-mới)
    - [Di chuyển giữa các thư mục](#di-chuyển-giữa-các-thư-mục)
    - [Xóa thư mục](#xóa-thư-mục)
3. [Thao tác với tệp tin](#thao-tác-với-tệp-tin)
    - [Tạo tệp tin mới](#tạo-tệp-tin-mới)
    - [Sao chép tệp tin](#sao-chép-tệp-tin)
    - [Di chuyển và đổi tên tệp tin](#di-chuyển-và-đổi-tên-tệp-tin)
    - [Xóa tệp tin](#xóa-tệp-tin)
4. [Lệnh hệ thống](#lệnh-hệ-thống)
    - [Xem đường dẫn hiện tại](#xem-đường-dẫn-hiện-tại)
    - [Liệt kê nội dung thư mục](#liệt-kê-nội-dung-thư-mục)
5. [Liên kết và lối tắt](#liên-kết-và-lối-tắt)
    - [Tạo liên kết mềm](#tạo-liên-kết-mềm)
6. [Thao tác với nội dung file](#thao-tác-với-nội-dung-file)
    - [Đọc nội dung file](#đọc-nội-dung-file)
    - [Đếm số từ, câu](#đếm-số-từ-câu)
    - [So sánh kí tự](#so-sánh-kí-tự)
    - [Tìm kiếm văn bản](#tìm-kiếm-văn-bản)
    - [Sắp xếp văn bản](#sắp-xếp-văn-bản)
    - [Lệnh uniq](#lệnh-uniq)
7. [Tìm kiếm và lọc](#tìm-kiếm-và-lọc)
    - [Lệnh tìm kiếm trong thư mục](#lệnh-tìm-kiếm-trong-thư-mục)
8. [Điều hướng đầu vào và đầu ra](#điều-hướng-đầu-vào-và-đầu-ra)
    - [Điều chỉnh đầu ra](#điều-chỉnh-đầu-ra)
    - [Điều chỉnh đầu vào](#điều-chỉnh-đầu-vào)
    - [Kết hợp câu lệnh](#kết-hợp-câu-lệnh)
    - [Trình tự câu lệnh](#trình-tự-câu-lệnh)
9. [Quản lý tiến trình](#quản-lý-tiến-trình)
    - [Xem ứng dụng và tiến trình đang chạy](#xem-ứng-dụng-và-tiến-trình-đang-chạy)
    - [Dừng tiến trình](#dừng-tiến-trình)
    - [Tạm dừng tiến trình đang chạy](#tạm-dừng-tiến-trình-đang-chạy)
10. [Tùy biến](#tùy-biến)
    - [Gán lệnh](#gán-lệnh)

## Bắt đầu với Terminal
- Cách 1: Ở desktop chọn icon Ubuntu và sau đó chọn Terminal
- Cách 2: Sử dụng tổ hợp phím `Ctrl + Alt + T`

## Thao tác với thư mục

### Tạo thư mục mới
```bash
mkdir <tên-thư-mục>
```

### Di chuyển giữa các thư mục
```bash
cd <tên-thư-mục>    # Di chuyển đến thư mục cụ thể
cd ~                # Di chuyển về thư mục home
cd ..              # Di chuyển lên thư mục cha
cd -               # Di chuyển về thư mục trước đó
```

### Xóa thư mục
```bash
rmdir <tên-thư-mục>     # Xóa thư mục trống
rm -r <tên-thư-mục>     # Xóa thư mục và nội dung bên trong
rm -rf <tên-thư-mục>    # Xóa bắt buộc, không cần xác nhận
```

## Thao tác với tệp tin

### Tạo tệp tin mới
```bash
touch <tên-file>.<đuôi-file>
```

### Sao chép tệp tin
```bash
cp <nguồn> <đích>
cp <tệp-tin> <thư-mục-đích>
cp -r <thư-mục-nguồn> <thư-mục-đích>    # Sao chép thư mục
```

### Di chuyển và đổi tên tệp tin
```bash
mv <tên-cũ> <tên-mới>               # Đổi tên
mv <tệp-tin> <thư-mục-đích>        # Di chuyển
```

### Xóa tệp tin
```bash
rm <tên-file>          # Xóa không xác nhận
rm -i <tên-file>       # Xóa có xác nhận
```

## Lệnh hệ thống

### Xem đường dẫn hiện tại
```bash
pwd
```

### Liệt kê nội dung thư mục
```bash
ls              # Liệt kê cơ bản
ls -l           # Liệt kê chi tiết
ls -a           # Hiện cả file ẩn
```

## Liên kết và lối tắt

### Tạo liên kết mềm
```bash
ln -s <đường-dẫn-đích> <tên-liên-kết>
```

## Thao tác với nội dung file

### Đọc nội dung file
```bash
cat <tên file>
```

### Đếm số từ, câu
```bash
wc <tên file>
```
trả về số dòng, số từ, số byte

### So sánh kí tự
```bash
diff <tên file 1> <tên file 2>
```
trả về > nghĩa là file 1 không có dòng đó nhưng file 2 có
trả về < nghĩa là file 1 có dòng đó nhưng file 2 không

### Tìm kiếm văn bản
```bash
grep <nội dung cần tìm> <tên file muốn tìm>
```

### Sắp xếp văn bản
```bash
sort <tên file>
```

### Lệnh uniq
```bash
uniq <tên file>              # Loại bỏ các dòng liền kề giống nhau
uniq -c <tên file>          # Hiển thị số lần xuất hiện của mỗi dòng
uniq -d <tên file>          # Chỉ hiển thị các dòng lặp lại
uniq -u <tên file>          # Chỉ hiển thị các dòng không lặp lại
```

## Tìm kiếm và lọc

### Lệnh tìm kiếm trong thư mục
```bash
find <đường dẫn> -name "<tên file>"    # Tìm file theo tên
find . -type f                         # Tìm tất cả các file
find . -type d                         # Tìm tất cả các thư mục
```

## Điều hướng đầu vào và đầu ra

### Điều chỉnh đầu ra
```bash
ls -l > myfiles.txt
```
Giải thích : 
- ls - l : in danh sách các nội dung có trong đường dẫn hiện tại  
- '>' myfiles.txt : chuyển kết quả đó và viết vào file txt

### Điều chỉnh đầu vào
```bash
java Guess < input.txt
```
Giải thích :
- java Guess : chạy code java  
- < input.txt : code viết trong file txt sẽ biên dịch

### Kết hợp câu lệnh
```bash
sort names.txt | uniq
```

### Trình tự câu lệnh
```bash
sort abc.txt ; cat
```

```bash
sort abc.txt && cat
```

Giải thích : dấu ; không yêu cầu lệnh trước thực hiện thành công. Trong khi && bắt buộc lệnh 1 phải chạy thành công rồi mới chạy lệnh 2

## Quản lý tiến trình

### Xem ứng dụng và tiến trình đang chạy (giống Task Manager)
```bash
top
```

### Dừng tiến trình 
```bash
kill <pipid>
```

### Tạm dừng tiến trình đang chạy
Ctrl + Z

## Tùy biến

### Gán lệnh
```bash
allias q=exit
```


### Hướng dẫn lập trình trong linux
### Với java
### B1 : Tải trình biên dịch
```bash
sudo apt install default-jre
```

Sau tải xong có thể kiểm tra bằng 
```bash
java --version
```

### B2 : tạo file và viết code
```bash
gedit Main.java
```

Code mẫu

```java
public class Main {
    public static void main (String[] args) {
        System.out.println("Hello World");
    }
}
```
### B3 : Chạy code
```bash
javac Main.java
java Main.java
```

### Với C và C++
### B1 : Tải trình biên dịch
```bash
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install build-essential
```

Sau tải xong có thể kiểm tra bằng 
```bash
gcc -v
make -v
```
Nếu hiển thị phiên bản nghĩa là cài đặt thành công
### B2 : tạo file và viết code
```bash
gedit main.cpp
```
code mẫu
```cpp
#include <iostream>

int main () {
    std::cout << "Hello World";
}
```
### B3 : Chạy code
```bash
g++ main.cpp -o <tên file kết quả>
./<tên file>
```
Với C thì tạo file có đuôi .c và chạy code như sau
```bash
gcc main.c -o <tên file kết quả>
./<tên file>
```