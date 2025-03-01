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
