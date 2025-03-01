# Tài liệu tổng hợp lệnh trong linux (Ubuntu)

# Cách mở terminal trong Ubuntu  
C1 : Ở desktop chọn icon Ubuntu và sau đó chọn Terminal  
C2 : Ctrl + Alt + T


## Tạo 1 folder mới
```bash
mkdir <tên folder>
```  
Ví dụ  
```bash
mkdir Java
```
## Di chuyển đến thư mục nào đó
```bash
cd <tên folder>
```
## Di chuyển về lại thư mục gốc (root)
```bash
cd ~
```
## Tạo 1 file mới
```bash
touch <tên file>.<đuôi file>
```  
Ví dụ  
```bash
touch main.py
```
## In đường dẫn hiện tại
```bash
pwd
```
## Liệt kê các file có trong đường dẫn
```bash
ls
```
## Xóa thư mục (thư mục phải trống)
```bash
rmdir <tên folder>
```
## Sao chép file 
##### Nếu muốn file chung folder
```bash
cp <tên file muốn copy> <tên file mới>.<đuôi file>
```
##### hoặc nếu muốn copy qua folder khác
```bash
cp <tên file muốn copy> <đường dẫn tới folder khác/tên file mới>.<đuôi file>
```

## Di chuyển file 
##### Nếu muốn đổi tên file
```bash
mv <tên file muốn di chuyển> <tên file mới>.<đuôi file>
```
##### hoặc nếu muốn di chuyển qua folder khác
```bash
cp <tên file muốn di chuyển> <đường dẫn tới folder khác/tên file mới>.<đuôi file>
```

## Xóa file
##### Như này thì sẽ không yêu cầu xác nhận
```bash
rm <tên file>
```
##### nếu muốn xác nhận trước khi xóa
```bash
rm -ri <tên file>
```
