# Agenda
- Playwright là gì?
- Tại sao chọn Playwright Typescript

# Playwright là gì
- Là 1 **framework**
- Tiền thân là Puppeteer, được Microsoft tài trợ và phát triển lên
- https://playwright.dev/
- Ra đời 31/01/2020
- Version mới nhất v1.50.1

## Ưu điểm
- Cross browser - chrome, firefox, safari, edge
- Cross platform - window, linux, macos
- Auto-wait
- Web-first assertion
- Tracing
- Code-gen

# Tại sao chọn Playwright
- **Cú pháp đơn giản**, hiện đại
- **Dễ học, dễ tiếp cận**
- Giảm rào cản tiếp cận

# Cài đặt tools
## NVM
- NVM = Node Version Manager = Quản lý các phiên bản NodeJs
- NodeJs = Công cụ để chạy code
- 2 options:
  - Cài đặt trực tiếp NodeJs vào máy
  - Cài đặt thông qua NVM
- Chọn thông qua NVM vì
  - Dễ chuyển đổi nhiều phiên bản NodeJs

## Cài đặt cấu hình GIT
- Config username: `git config --global user.name "Vu"`
- Config email: `git config --global user.email dominhvu278@gmail.com`
- Config branch default: `git config --global init.defaultBranch main`

## Kết nối với Github
- SSH key
- Cặp khoá (2 cái)
  - `id_rsa` và `id_rsa.pub`
  - `id_rsa`: Cần giữ bí mật
  - `id_rsa.pub`: Có thể gửi cho người khác
- Giúp xác thực đăng nhập trở nên dễ dàng hơn
- Lưu ở `~/.ssh`
  - ~ đại diện cho thư mục home

## Tạo ssh key & connect git
- SSH key
- Tạo SSH key
  - Lưu ý, nếu file đã tồn tại, cần kiểm tra kỹ trước khi ghi đè
  - Câu lệnh: `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`
- Thêm vào github
  - Lấy nội dung ssh key: `cat ~/.ssh/id_rsa.pub`
  - Truy cập vào github.com/settings/ssh/new

# Cài đặt PL
- Tạo thư mục pw-course
- Chạy lệnh:
  - npm init
  - playwright@latest
- Đi tới file: `example.spec.ts`
- Click run test
