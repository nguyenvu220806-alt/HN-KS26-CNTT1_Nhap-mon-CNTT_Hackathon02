# BÀI LÀM – HACKATHON 02

- **Mã đề:** 06
- **Họ tên:** Nguyễn Hồng Vũ 
- **Lớp:** CNTT1
- **Link repository:** https://github.com/nguyenvu220806-alt/HN-KS26-CNTT1_Nhap-mon-CNTT_Hackathon02/upload
- **Hệ điều hành (Windows/macOS):** Windows

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```shell
1. pwd
2. ls -force
3. mv yeu_cau_khach_hang.txt docs
4. mkdir backup
5. cp .\data\don_in_thang6.xlsx .\backup\
6. rm .\temp_606.tmp
7. cd logs
8. ls
9. cd ..
10. get-childitem -Recurse -Force

```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
 Directory: C:\Users\GIGA\Downloads\starter-kit (1)\starter-kit\xuong-in
    -website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        2026/11/11      7:52                backup
d-----        2026/11/11      7:42                data
d-----        2026/11/11      7:50                docs
d-----        2026/11/11      7:36                evidence
d-----        2026/11/11      7:42                logs
d-----        2026/11/11      7:32                web
------        2026/11/03      7:07             76 .env
-a----        2026/11/11      7:55           2621 bai_lam.md


    Directory: C:\Users\GIGA\Downloads\starter-kit (1)\starter-kit\xuong-in
    -website\backup


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        2026/11/03      7:07           6137 don_in_thang6.xlsx


    Directory: C:\Users\GIGA\Downloads\starter-kit (1)\starter-kit\xuong-in
    -website\data


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        2026/11/03      7:07           6137 don_in_thang6.xlsx


    Directory: C:\Users\GIGA\Downloads\starter-kit (1)\starter-kit\xuong-in
    -website\docs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        2026/11/03      7:07            153 yeu_cau_khach_hang.txt


    Directory: C:\Users\GIGA\Downloads\starter-kit (1)\starter-kit\xuong-in
    -website\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        2026/11/03      7:07            981 order.log


    Directory: C:\Users\GIGA\Downloads\starter-kit (1)\starter-kit\xuong-in
    -website\web


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        2026/11/11      7:32                images
------        2026/11/03      7:07            594 app.js
------        2026/11/03      7:07            516 index.html
------        2026/11/03      7:07            460 style.css


    Directory: C:\Users\GIGA\Downloads\starter-kit (1)\starter-kit\xuong-in
    -website\web\images


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
------        2026/11/03      7:07           3092 logo-printnow.png


PS C:\Users\GIGA\Downloads\starter-kit (1)\starter-kit\xuong-in-website>


```

## 4.3. Lọc log truy cập website

### a) Lệnh lọc các dòng status=500

```shell
Get-Content "logs/order.log" | sls "status=500"
Get-Content "logs/order.log" | sls "status=500" >> logs/loi_500.txt

```

### 2 dòng đầu tiên trong logs/loi_500.txt

```text
2026-06-28 08:15:01 POST /api/thanh-toan status=500
2026-06-28 08:34:07 POST /api/tai-file status=500


```

### b) Lệnh đếm số dòng status=404 và kết quả

```shell
Get-Content "logs/order.log" | sls "status=404" | measure-object


```

```text
4

```

## 4.4. Chạy script tong_hop (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell
 Set -ExcutionPolicy -Scope Process -xecutionPolicy Bypass .\tong_hop.ps1


```

### Nội dung file logs/tong_hop.txt

```text
Dang tao bao cao..
Hoan thanh! 
```

## 4.5. README.md và bảo vệ thông tin bí mật

> README.md, .gitignore và .env.example được chấm trực tiếp trên file ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [x] README.md: Heading 1, mô tả có **in đậm** và *in nghiêng*, bảng, code block, task list, blockquote
- [x] .gitignore có dòng `.env` (tên file đúng, không có đuôi .txt)
- [ ] .env.example có đủ tên biến, giá trị để trống (tên file đúng, không có đuôi .txt)

## 4.6. Kiểm tra trang web bằng DevTools (F12) và báo cáo lỗi

### Bảng lỗi

| STT | Tab DevTools phát hiện lỗi | Tên file hoặc thông báo lỗi | Cách khắc phục |
| --- | --- | --- | --- |
| 1 |lỗi không logo   |  | F12  |
| 2 | lỗi không hiện bảng   |  |  |

> Ảnh chụp màn hình lưu trong thư mục `evidence/` (network.png, console.png).

### Báo cáo lỗi gửi trưởng nhóm

- **Context:** 
- **Expected:** 
- **Actual:** 
- **Log:** 

### Câu tìm kiếm Google

```text
(Ghi câu tìm kiếm vào đây – xoá dòng này)

```

## 4.7. Excel

> Phần Excel được chấm trực tiếp trên file `data/don_in_thang_6.xlsx`, không cần ghi vào đây.
