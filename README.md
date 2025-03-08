Dưới đây là toàn bộ nội dung bằng Markdown để bạn có thể dễ dàng copy:

# 📘 Hướng Dẫn Lệnh Linux (Ubuntu)

<div align="center">
  
  ![Linux Logo](assets/12.png)

  **Tài liệu tổng hợp các lệnh cơ bản trong Ubuntu Linux**
  
</div>

## 📋 Mục Lục

- [🚀 Bắt Đầu Với Terminal](#-bắt-đầu-với-terminal)
- [📁 Thao Tác Với Thư Mục](#-thao-tác-với-thư-mục)
- [📄 Thao Tác Với Tệp Tin](#-thao-tác-với-tệp-tin)
- [⚙️ Lệnh Hệ Thống](#️-lệnh-hệ-thống)
- [🔗 Liên Kết Và Lối Tắt](#-liên-kết-và-lối-tắt)
- [📝 Thao Tác Với Nội Dung File](#-thao-tác-với-nội-dung-file)
- [🔍 Tìm Kiếm Và Lọc](#-tìm-kiếm-và-lọc)
- [↪️ Điều Hướng Đầu Vào Và Đầu Ra](#️-điều-hướng-đầu-vào-và-đầu-ra)
- [⏯️ Quản Lý Tiến Trình](#️-quản-lý-tiến-trình)
- [🛠️ Tùy Biến](#️-tùy-biến)
- [💻 Lập Trình Trên Linux](#-lập-trình-trên-linux)

---

## 🚀 Bắt Đầu Với Terminal

<kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>T</kbd> - Mở terminal nhanh chóng

*Hoặc tìm kiếm "Terminal" trong menu Ubuntu*

---

## 📁 Thao Tác Với Thư Mục

### Tạo thư mục mới

```bash
mkdir <tên-thư-mục>                # Tạo một thư mục
mkdir -p <thư-mục1>/<thư-mục2>     # Tạo cấu trúc thư mục lồng nhau
```

### Di chuyển giữa các thư mục

| Lệnh | Mô tả |
|------|-------|
| `cd <tên-thư-mục>` | Di chuyển đến thư mục cụ thể |
| `cd ~` | Di chuyển về thư mục home |
| `cd ..` | Di chuyển lên thư mục cha |
| `cd -` | Di chuyển về thư mục trước đó |

### Xóa thư mục

```bash
rmdir <tên-thư-mục>     # Xóa thư mục trống
rm -r <tên-thư-mục>     # Xóa thư mục và nội dung bên trong
rm -rf <tên-thư-mục>    # Xóa bắt buộc, không cần xác nhận
```

> ⚠️ **Cảnh báo**: Hãy cẩn thận với lệnh `rm -rf` vì nó xóa không khôi phục được!

---

## 📄 Thao Tác Với Tệp Tin

### Tạo tệp tin mới

```bash
touch <tên-file>.<đuôi-file>   # Tạo file trống
nano <tên-file>.<đuôi-file>    # Tạo và mở file bằng trình soạn thảo nano
```

### Sao chép tệp tin

```bash
cp <nguồn> <đích>                  # Sao chép file
cp -r <thư-mục-nguồn> <thư-mục-đích>    # Sao chép thư mục và nội dung
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

---

## ⚙️ Lệnh Hệ Thống

### Xem đường dẫn hiện tại

```bash
pwd     # Print Working Directory
```

### Liệt kê nội dung thư mục

| Lệnh | Mô tả |
|------|-------|
| `ls` | Liệt kê cơ bản |
| `ls -l` | Liệt kê chi tiết (quyền, kích thước, thời gian) |
| `ls -a` | Hiện cả file ẩn |
| `ls -lh` | Liệt kê chi tiết với kích thước đọc được (KB, MB) |

---

## 🔗 Liên Kết Và Lối Tắt

### Tạo liên kết mềm (symbolic link)

```bash
ln -s <đường-dẫn-đích> <tên-liên-kết>
```

> 💡 **Mẹo**: Liên kết mềm hoạt động giống như shortcut trong Windows

---

## 📝 Thao Tác Với Nội Dung File

### Đọc nội dung file

```bash
cat <tên-file>         # Hiển thị toàn bộ nội dung
less <tên-file>        # Xem nội dung theo trang (ấn q để thoát)
head <tên-file>        # Xem 10 dòng đầu tiên
tail <tên-file>        # Xem 10 dòng cuối cùng
```

### Đếm số từ, câu

```bash
wc <tên-file>          # Trả về số dòng, số từ, số byte
```

### So sánh kí tự

```bash
diff <tên-file-1> <tên-file-2>
```

| Kết quả | Ý nghĩa |
|---------|---------|
| `>` | File 1 không có dòng đó nhưng file 2 có |
| `<` | File 1 có dòng đó nhưng file 2 không |

### Tìm kiếm văn bản

```bash
grep "<nội-dung-cần-tìm>" <tên-file>   # Tìm chuỗi trong file
grep -i "<chuỗi>" <tên-file>           # Tìm không phân biệt hoa thường
grep -r "<chuỗi>" <thư-mục>            # Tìm đệ quy trong thư mục
```

### Sắp xếp văn bản

```bash
sort <tên-file>              # Sắp xếp theo bảng chữ cái
sort -n <tên-file>           # Sắp xếp theo số
sort -r <tên-file>           # Sắp xếp ngược lại
```

### Lệnh uniq

```bash
uniq <tên-file>              # Loại bỏ các dòng liền kề giống nhau
uniq -c <tên-file>           # Hiển thị số lần xuất hiện của mỗi dòng
uniq -d <tên-file>           # Chỉ hiển thị các dòng lặp lại
uniq -u <tên-file>           # Chỉ hiển thị các dòng không lặp lại
```

---

## 🔍 Tìm Kiếm Và Lọc

### Lệnh tìm kiếm trong thư mục

```bash
find <đường-dẫn> -name "<tên-file>"    # Tìm file theo tên
find . -type f                         # Tìm tất cả các file
find . -type d                         # Tìm tất cả các thư mục
find . -size +10M                      # Tìm file lớn hơn 10MB
```

---

## ↪️ Điều Hướng Đầu Vào Và Đầu Ra

### Điều chỉnh đầu ra

```bash
ls -l > myfiles.txt           # Ghi đè kết quả vào file
ls -l >> myfiles.txt          # Nối thêm kết quả vào file
```

### Điều chỉnh đầu vào

```bash
java Guess < input.txt        # Lấy input từ file
```

### Kết hợp câu lệnh (Pipes)

```bash
sort names.txt | uniq         # Đầu ra của lệnh này là đầu vào của lệnh kia
ls -l | grep "txt"            # Tìm các file .txt trong danh sách
```

### Trình tự câu lệnh

| Cú pháp | Mô tả |
|---------|-------|
| `sort abc.txt ; cat` | Thực hiện tuần tự không phụ thuộc |
| `sort abc.txt && cat` | Lệnh 2 chỉ chạy nếu lệnh 1 thành công |
| `sort abc.txt  cat` | Lệnh 2 chỉ chạy nếu lệnh 1 thất bại |

---

## ⏯️ Quản Lý Tiến Trình

### Xem ứng dụng và tiến trình đang chạy

```bash
top                     # Hiển thị các tiến trình đang chạy (giống Task Manager)
htop                    # Phiên bản đồ họa của top (cần cài đặt)
ps aux                  # Liệt kê các tiến trình
```

### Dừng tiến trình 

```bash
kill <PID>              # Dừng tiến trình theo ID
killall <tên-tiến-trình>  # Dừng tất cả tiến trình có tên cụ thể
```

### Tạm dừng tiến trình đang chạy

<kbd>Ctrl</kbd> + <kbd>Z</kbd> - Tạm dừng tiến trình hiện tại

---

## 🛠️ Tùy Biến

### Gán lệnh

```bash
alias q='exit'                  # Tạo lệnh rút gọn
alias ll='ls -la'               # Tạo lệnh tùy chỉnh
```

> 💡 **Mẹo**: Thêm các alias vào file `~/.bashrc` để lưu trữ vĩnh viễn

---

## 💻 Lập Trình Trên Linux

### Lập trình Java

#### Cài đặt JDK

```bash
sudo apt install default-jre default-jdk
java --version                  # Kiểm tra phiên bản
```

#### Tạo và biên dịch chương trình

```bash
# Tạo file và viết code
gedit Main.java

# Biên dịch
javac Main.java

# Chạy chương trình
java Main
```

#### Code mẫu Java

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```

### Lập trình C/C++

#### Cài đặt trình biên dịch

```bash
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install build-essential
```

#### Kiểm tra cài đặt

```bash
gcc -v
make -v
```

#### C++: Tạo và biên dịch

```bash
# Tạo file
gedit main.cpp

# Biên dịch
g++ main.cpp -o program

# Chạy
./program
```

#### C: Tạo và biên dịch

```bash
# Tạo file
gedit main.c

# Biên dịch
gcc main.c -o program

# Chạy
./program
```

#### Code mẫu C++

```cpp
#include <iostream>

int main() {
    std::cout << "Hello World";
    return 0;
}
```