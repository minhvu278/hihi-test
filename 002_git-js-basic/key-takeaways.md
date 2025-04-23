# Agenda
- Version control system
- Git
- Js basic

# Version control System
- VCS (Version Control System): Hệ thống quản lý các phiên bản - Giúp bạn lưu lại các phiên bản khác nhau, quay lại bản cũ nếu cần hoặc xem ai đã sửa gì
  - Google Docs sử dụng Version Control System để dễ quản lý các version
  - **Local**: Lưu ở máy cá nhân - Hiện nay ít dùng
  - **Centralize**: Lưu ở 1 server trung tâm chứa code - Ví dụ SVN
  - **Distributed**: Lưu ở nhiều máy khác nhau - Mỗi người có 1 bản sao toàn bộ dự án (Git - phổ biến nhất hiện nay)

# Git
- Được viết bởi Linus Torvalds, cha đẻ của Linux
- git là từ viết sai chính tả có chủ đích của get, lí do là get đã được sử dụng rồi
- Dùng git do nhu cầu quản lý phiên bản & làm việc giữa nhiều người với nhau

## So sánh git với các VCS khác
- Tính năng
  - Dễ dùng, có nhiều tính năng vượt trội: branching, tốc độ xử lý nhanh
- Chi phí: Free
- Phổ biến: Nhiều công ty sử dụng

## Git & github
| Git | Github|
|-----|-------|
|Là 1 phần mềm | Là 1 dịch vụ web|
| Cài trên máy của bạn | Host trên web|
| Là 1 commandline tool | Là công cụ có giao diện|
| Là 1 công cụ quản lý phiên bản | Là nơi upload git repository lên|
| Có các tính năng của Version Control System | Có các tính năng của VCS và 1 số tính năng khác|

## Git - three states
- **Working Directory**: Các file mới hoặc có thay đổi
  - Giống như bản nháp trên máy tính cá nhân, có thể thêm sửa xoá
  - Nhưng thay đổi này chưa được Git quản lý chính thức cho đến khi bạn đưa chúng sang bước tiếp theo
- **Staging Area**: Các file đưa vào vùng chuẩn bị commit (tạo ra các phiên bản)
  - Là bước trung gian, nơi chọn những thay đổi của Working để chuẩn bị lưu vào lịch sử của Git
  - Giống như 1 giỏ hàng - bạn chỉ đưa vào những thứ mà bạn muốn "Thanh toán" (commit)
- **Repository**: Các commit (phiên bản)
  - Nơi git lưu trữ toàn bộ thay đổi của dự án (các commit)
  - Khi commit từ Staging Area, những thay đổi đó sẽ được ghi lại vĩnh viễn trong Repository.

### Ví dụ
- Chúng ta tạo ra 1 file là `test.txt`
- Sau khi chúng ta gõ lệnh git init -> file sẽ được chuyển vào vùng Working Directory
- Sau khi chúng ta gõ `git add test.txt` -> File sẽ được thêm vào vùng Staging Area
- Và sau khi gõ `git commit -m"feat: add file test"` -> File sẽ được chuyển vào vùng repository
- Ở local chúng ta tạo thêm file & sau đó lặp lại các bước trên. Đến khi đến bước commit nó sẽ tạo thêm 1 phiên bản nữa (Bây giờ đang có 2)
- Mỗi lần commit là 1 lần tạo ra 1 version mới 

# Git key takeaways
- Câu lệnh thường dùng để khởi tạo thư mục quản lý bởi git `git init`
- Sau khi cài đặt xong, cần cấu hình git
  - Cho 1 repo: git config user.name "<name>"
  - Cho 1 repo: git config user.email "<email>"

# JS basic
- Javascript - ăn theo cái tên hot Java
- Là 1 ngôn ngữ lập trình
- Ra đời năm 1995 bởi Brendan Eich
- Giúp browser hoạt động được
- Top language
- Bình thường Js chạy được do browser enginer support
- Để chạy được trên máy tính, không cần trình duyệt, cần nodeJs
- Runtime

## Js systax
- 