# Tài liệu tổng hợp lệnh trong Linux (Ubuntu)

## Mục lục
1. [Cách mở terminal trong Ubuntu](#cách-mở-terminal-trong-ubuntu)
2. [Tạo thư mục](#tạo-thư-mục)
3. [Di chuyển thư mục](#di-chuyển-thư-mục)
4. [Tạo file mới](#tạo-file-mới)
5. [Các lệnh khác](#các-lệnh-khác)
    - [In đường dẫn hiện tại](#in-đường-dẫn-hiện-tại)
    - [Liệt kê các file](#liệt-kê-các-file)
    - [Xóa thư mục](#xóa-thư-mục)
    - [Sao chép file](#sao-chép-file)
    - [Di chuyển file](#di-chuyển-file)
    - [Xóa file](#xóa-file)

## Cách mở terminal trong Ubuntu
- Cách 1: Ở desktop chọn icon Ubuntu và sau đó chọn Terminal.
- Cách 2: Sử dụng tổ hợp phím `Ctrl + Alt + T`.

## Tạo thư mục
```bash
mkdir <tên-thư-mục>
```
Ví dụ:
```bash
mkdir Java
```

## Di chuyển thư mục
- Di chuyển đến thư mục:
```bash
cd <tên-thư-mục>
```
- Di chuyển về thư mục gốc (root):
```bash
cd ~
```

## Tạo file mới
```bash
touch <tên-file>.<đuôi-file>
```
Ví dụ:
```bash
touch main.py
```

## Các lệnh khác

### In đường dẫn hiện tại
```bash
pwd
```

### Liệt kê các file trong thư mục hiện tại
```bash
ls
```

### Xóa thư mục (thư mục phải trống)
```bash
rmdir <tên-thư-mục>
```

### Sao chép file
- Nếu muốn file chung thư mục:
```bash
cp <tên-file-muốn-copy> <tên-file-mới>.<đuôi-file>
```
- Nếu muốn copy qua thư mục khác:
```bash
cp <tên-file-muốn-copy> <đường-dẫn-tới-thư-mục-khác/tên-file-mới>.<đuôi-file>
```

### Di chuyển file
- Nếu muốn đổi tên file:
```bash
mv <tên-file-muốn-di-chuyển> <tên-file-mới>.<đuôi-file>
```
- Nếu muốn di chuyển qua thư mục khác:
```bash
mv <tên-file-muốn-di-chuyển> <đường-dẫn-tới-thư-mục-khác/tên-file-mới>.<đuôi-file>
```

### Xóa file
- Xóa không cần xác nhận:
```bash
rm <tên-file>
```
- Xóa yêu cầu xác nhận:
```bash
rm -ri <tên-file>
```
