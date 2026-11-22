# Portfolio CV - Đỗ Trí Đạt

Trang portfolio cá nhân giới thiệu thông tin, kỹ năng, hình ảnh và một số nội dung dự án của Đỗ Trí Đạt. Giao diện được xây dựng theo hướng tối giản, responsive và có thể chạy trực tiếp trên trình duyệt hoặc qua Docker.

## Chức năng

- Giới thiệu cá nhân và vai trò Frontend Developer.
- Hiển thị các kỹ năng.
- Trình bày các thẻ dự án kèm hình ảnh và mô tả.
- Cung cấp thông tin liên hệ qua email và GitHub.
- Có khung nhập ý kiến phản hồi với hiệu ứng hover/focus.

> Khung phản hồi hiện chỉ là giao diện: nút “Gửi ý kiến” chưa gửi hoặc lưu dữ liệu.

## Công nghệ sử dụng

- HTML5.
- CSS3: Flexbox, CSS Grid, media queries, custom properties và hiệu ứng hover/focus.
- Nginx (tùy chọn): phục vụ trang tĩnh khi chạy bằng Docker.

Dự án không sử dụng framework, thư viện JavaScript, trình quản lý gói hoặc bước build.

## Yêu cầu môi trường

### Chạy trực tiếp

- Trình duyệt web hiện đại (Chrome, Edge, Firefox hoặc Safari).
- Không cần cài Node.js hay công cụ build.

### Chạy bằng Docker

- Docker Engine hoặc Docker Desktop đang hoạt động.
- Kết nối Internet ở lần đầu để tải image `nginx:alpine`.

## Cài đặt

### Windows (PowerShell)

```powershell
git clone https://github.com/dotridat2005-bit/My-CV.git
Set-Location My-CV
```

### macOS

```bash
git clone https://github.com/dotridat2005-bit/My-CV.git
cd My-CV
```

### Linux

```bash
git clone https://github.com/dotridat2005-bit/My-CV.git
cd My-CV
```

Nếu không dùng Git, tải hoặc giải nén mã nguồn vào một thư mục trên máy tính.

## Cấu hình

Dự án không có file `.env` hoặc cấu hình máy chủ bắt buộc.

- **Nội dung trang:** sửa các phần tương ứng trong `index.html`.
- **Màu sắc, bố cục và breakpoint:** chỉnh các biến trong `:root` và các quy tắc trong `assets/css/styles.css`.
- **Hình ảnh:** đặt ảnh trong `assets/img/` và cập nhật đường dẫn `src` trong `index.html`.
- **Thông tin liên hệ:** cập nhật email và URL GitHub trong phần Liên hệ của `index.html`. Kiểm tra `href` để bảo đảm liên kết trỏ đúng địa chỉ.

## Chạy thử

### Windows

Sau khi clone, có thể mở `index.html` bằng cách nhấp đúp trong File Explorer hoặc chạy:

```powershell
Start-Process .\index.html
```

### macOS

```bash
open index.html
```

### Linux

```bash
xdg-open index.html
```

Các lệnh trên mở trang từ file cục bộ. Để kiểm tra qua HTTP hoặc Docker, xem mục bên dưới.

## Chạy bằng Docker

Chạy các lệnh từ thư mục gốc của dự án, nơi có `index.html`.

### Windows (PowerShell, Docker Desktop)

```powershell
docker run -d --name my-cv -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

### macOS và Linux

```bash
docker run -d --name my-cv -p 8080:80 -v "$PWD:/usr/share/nginx/html:ro" nginx:alpine
```

Mở [http://localhost:8080](http://localhost:8080) để xem trang. Nếu cổng `8080` đang được sử dụng, thay `8080` ở phía trái của `-p` bằng một cổng khác, ví dụ `8081:80`.

Dừng và xóa container:

```bash
docker stop my-cv
docker rm my-cv
```

Trong PowerShell, chạy hai lệnh trên riêng biệt hoặc ngăn cách bằng dấu chấm phẩy (`;`).

## Kiểm tra sau khi chạy

- Xác nhận trang, CSS và hình ảnh tải bình thường.
- Thử các liên kết điều hướng nội bộ.
- Nhập thử nội dung vào khung phản hồi. Nút gửi chưa có chức năng gửi dữ liệu.
- Kiểm tra bố cục ở kích thước màn hình desktop và mobile.

Hiện dự án chưa có bộ kiểm thử tự động hoặc lệnh test riêng.

## Cấu trúc thư mục

```text
.
├── index.html
├── README.md
├── assets/
│   ├── css/
│   │   └── styles.css
│   └── img/
└── docs/
    ├── AI_LOG.md
    ├── RELEASENOTE.md
    └── test_report.md
```

## Thông tin liên hệ

- **Tác giả:** Đỗ Trí Đạt
- **Email:** [dotridat@gmail.com](mailto:dotridat@gmail.com)
- **GitHub:** [dotridat2005-bit](https://github.com/dotridat2005-bit)
- **Repository:** [dotridat2005-bit/My-CV](https://github.com/dotridat2005-bit/My-CV)
