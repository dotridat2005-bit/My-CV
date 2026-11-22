# BÁO CÁO KIỂM THỬ SẢN PHẨM

## 1. Thông tin chung

| Thông tin | Chi tiết |
|---|---|
| Tên dự án | Portfolio CV cá nhân - Đỗ Trí Đạt |
| Phiên bản | v1.0 (theo `docs/RELEASENOTE.md`) |
| Ngày kiểm thử | 23/11/2026 |
| Người thực hiện | [Bổ sung họ tên người kiểm thử] |
| Người đánh giá | [Bổ sung họ tên người đánh giá] |
| Phạm vi | Kiểm tra giao diện, nội dung, tương tác cơ bản và hồ sơ bàn giao |
| Môi trường đã kiểm tra | Mở `index.html` trực tiếp bằng trình duyệt tích hợp |
| Quy ước trạng thái | **Đạt**: có kết quả kiểm tra phù hợp; **Chưa đạt**: có lỗi hoặc thiếu yêu cầu; **Cần cải thiện**: chưa đủ kiểm thử/minh chứng hoặc còn rủi ro cần xử lý |

> Báo cáo ghi nhận kết quả kiểm tra thủ công hiện có. Các hạng mục chưa được thực thi không được xem là đã đạt.

## 2. Bảng tổng quan trạng thái

| # | Nhóm tiêu chí | Trạng thái | Tóm tắt |
|---|---|---|---|
| 1 | Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng | Cần cải thiện | Các phần chính hiển thị; ô phản hồi nhận được nội dung nhập. Liên kết dự án còn là placeholder và nút gửi chưa xử lý dữ liệu. |
| 2 | Giao diện, trải nghiệm người dùng và khả năng tương thích | Cần cải thiện | Trang và khung phản hồi hiển thị trong trình duyệt đã kiểm tra; chưa có kết quả trên nhiều kích thước màn hình/trình duyệt. |
| 3 | Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản | Cần cải thiện | Trang tĩnh mở được; chưa đo hiệu năng hoặc kiểm tra lỗi trên nhiều môi trường. |
| 4 | Bảo mật, quản lý cấu hình và dữ liệu | Cần cải thiện | Không thấy luồng xử lý dữ liệu phía máy chủ trong phạm vi kiểm tra; chưa thực hiện rà soát bảo mật chuyên sâu. |
| 5 | Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao | Đạt | Có cấu trúc HTML/CSS tách biệt, README và ghi chú phát hành; chưa chạy công cụ phân tích mã tự động. |
| 6 | Khả năng triển khai, kiểm thử và cung cấp minh chứng | Cần cải thiện | Có kiểm tra thủ công trên file cục bộ; chưa triển khai lên môi trường đích, chưa có bộ kiểm thử tự động hoặc gói minh chứng bàn giao. |

## 3. Nội dung kiểm thử chi tiết

### 3.1. Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng

| Hạng mục kiểm tra | Trạng thái | Ghi chú / Minh chứng |
|---|---|---|
| Hiển thị các phần giới thiệu, kỹ năng, dự án và liên hệ | Đạt | Mở `index.html` trong trình duyệt; các phần chính được hiển thị trong trang. |
| Điều hướng nội bộ đến các mục trên trang | Đạt | Các mục menu liên kết đến `#about`, `#skills`, `#projects` và `#contact`, tương ứng với các section trong HTML. |
| Nhập nội dung vào khung ý kiến phản hồi | Đạt | Đã nhập thử nội dung vào trường “Ý kiến của bạn”; nội dung được hiển thị trong ô nhập. |
| Nút “Gửi ý kiến” xử lý hoặc lưu phản hồi | Cần cải thiện | Nút hiện chỉ phục vụ giao diện (`type="button"`); chưa có xử lý, gửi hoặc lưu dữ liệu. Đây là giới hạn đã biết của phiên bản giao diện tĩnh. |
| Liên kết “Xem chi tiết” của dự án và GitHub | Chưa đạt | Các liên kết hiện dùng `href="#"`; chưa dẫn tới trang đích thực tế. |

### 3.2. Giao diện, trải nghiệm người dùng và khả năng tương thích

| Hạng mục kiểm tra | Trạng thái | Ghi chú / Minh chứng |
|---|---|---|
| Bố cục và nội dung trang trên trình duyệt đã kiểm tra | Đạt | Trang mở được; tiêu đề, các phần nội dung và footer hiển thị trong trình duyệt tích hợp. |
| Trạng thái nhập liệu và nút phản hồi | Đạt | Trường nhập và nút hiển thị; đã xác nhận trường nhập nhận được nội dung thử nghiệm. |
| Hiệu ứng hover/focus và thao tác bằng bàn phím | Cần cải thiện | CSS có khai báo hover/focus và `:focus-visible`; chưa kiểm tra thủ công toàn bộ thành phần bằng chuột, bàn phím và thiết bị hỗ trợ. |
| Bố cục trên mobile, tablet và desktop | Cần cải thiện | CSS có breakpoint 768px và 1280px; chưa chụp/kiểm tra thực tế tại các viewport này. |
| Tương thích trên nhiều trình duyệt | Cần cải thiện | Mới kiểm tra bằng trình duyệt tích hợp; chưa có kết quả trên các trình duyệt và phiên bản khác. |

### 3.3. Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản

| Hạng mục kiểm tra | Trạng thái | Ghi chú / Minh chứng |
|---|---|---|
| Mở trang từ file HTML cục bộ | Đạt | `index.html` tải và hiển thị trong trình duyệt tích hợp. |
| Tải CSS và hình ảnh trang | Cần cải thiện | Giao diện được hiển thị; chưa kiểm tra độc lập tất cả tài nguyên hoặc xác nhận lỗi tải trong Network/Console. |
| Xử lý lỗi khi thiếu tài nguyên hoặc dữ liệu không hợp lệ | Cần cải thiện | Chưa thực hiện các tình huống lỗi; trang hiện là nội dung tĩnh, không có luồng nghiệp vụ xử lý dữ liệu. |
| Hiệu năng tải trang | Cần cải thiện | Chưa đo thời gian tải, kích thước tài nguyên, chỉ số hiệu năng hoặc hiệu năng trên mạng chậm/thiết bị cấu hình thấp. |

### 3.4. Bảo mật, quản lý cấu hình và dữ liệu

| Hạng mục kiểm tra | Trạng thái | Ghi chú / Minh chứng |
|---|---|---|
| Luồng thu thập và lưu trữ dữ liệu phản hồi | Cần cải thiện | Nút gửi chưa gửi dữ liệu; không xác nhận được quy trình lưu trữ vì chưa có backend. Cần kiểm thử lại nếu bổ sung chức năng gửi. |
| Thông tin nhạy cảm hoặc cấu hình bí mật trong mã nguồn | Cần cải thiện | Chưa thực hiện quét secret hoặc rà soát bảo mật toàn repository. |
| Kiểm tra dữ liệu đầu vào | Cần cải thiện | Trường phản hồi có `required`, nhưng chưa có xử lý/kiểm tra phía ứng dụng; thuộc tính này không thay thế validation phía máy chủ nếu triển khai gửi dữ liệu. |
| HTTPS, quyền truy cập và cấu hình môi trường triển khai | Cần cải thiện | Chưa có môi trường triển khai hoặc cấu hình máy chủ để kiểm tra. |

### 3.5. Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao

| Hạng mục kiểm tra | Trạng thái | Ghi chú / Minh chứng |
|---|---|---|
| Phân tách cấu trúc nội dung và kiểu trình bày | Đạt | Nội dung nằm trong `index.html`; CSS nằm riêng tại `assets/css/styles.css`. |
| Cấu trúc thư mục chính | Đạt | Có thư mục `assets/css`, `assets/img` và `docs`; các hình ảnh được lưu riêng trong `assets/img`. |
| Tài liệu giới thiệu và hướng dẫn mở dự án | Đạt | `README.md` mô tả công nghệ, cấu trúc thư mục và cách mở trang cục bộ. |
| Ghi chú phiên bản | Đạt | Có `docs/RELEASENOTE.md` ghi nhận phiên bản v1.0 và các giới hạn đã biết. |
| Kiểm tra tự động chất lượng mã | Cần cải thiện | Chưa chạy validator HTML, linter CSS, kiểm tra accessibility hoặc pipeline CI. |

### 3.6. Khả năng triển khai, kiểm thử và cung cấp minh chứng

| Hạng mục kiểm tra | Trạng thái | Ghi chú / Minh chứng |
|---|---|---|
| Kiểm tra thủ công chức năng giao diện cơ bản | Đạt | Đã mở trang cục bộ, xác nhận nội dung trang, ô phản hồi và nút hiển thị; đã nhập thử vào ô phản hồi. |
| Kiểm tra định dạng thay đổi | Đạt | `git diff --check` không báo lỗi whitespace trong lần kiểm tra đã thực hiện. |
| Bộ kiểm thử hồi quy/tự động | Cần cải thiện | Chưa có hoặc chưa chạy bộ test tự động; cần bổ sung nếu dự án tiếp tục phát triển. |
| Triển khai lên môi trường bàn giao | Cần cải thiện | Chưa kiểm tra trên hosting hoặc URL triển khai thực tế. |
| Minh chứng kiểm thử có thể bàn giao | Cần cải thiện | Báo cáo này ghi lại kết quả; chưa đính kèm ảnh chụp, log trình duyệt hay kết quả kiểm thử đa thiết bị. |

## 4. Đánh giá tổng kết và đề xuất

### Nhận định chung

Portfolio có thể mở dưới dạng trang tĩnh và các nội dung chính hiển thị trong môi trường đã kiểm tra. Khung phản hồi đáp ứng mục tiêu giao diện: người dùng có thể bấm vào để nhập nội dung. Tuy nhiên, nút gửi hiện chưa thực hiện gửi/lưu dữ liệu; một số liên kết còn là placeholder. Khả năng tương thích đa thiết bị, hiệu năng, bảo mật chuyên sâu và triển khai thực tế chưa được xác minh.

**Mức độ sẵn sàng bàn giao: Cần cải thiện trước khi bàn giao chính thức.** Có thể bàn giao như bản giao diện tĩnh/demo nếu phạm vi bàn giao nêu rõ rằng biểu mẫu phản hồi chưa có backend và các liên kết placeholder chưa hoàn thiện.

### Vấn đề cần xử lý hoặc xác nhận

1. Thay các liên kết `href="#"` bằng URL đích hợp lệ hoặc bỏ liên kết nếu chưa có trang tương ứng.
2. Xác nhận với bên nhận sản phẩm rằng khung phản hồi chỉ cần giao diện; nếu cần gửi thật, triển khai và kiểm thử API/backend, validation, trạng thái thành công/thất bại và chính sách dữ liệu.
3. Kiểm tra giao diện tại các viewport mobile, tablet, desktop và trên các trình duyệt mục tiêu.
4. Kiểm tra lỗi tải tài nguyên, lỗi trong Console và các trạng thái sử dụng bằng bàn phím.
5. Chạy validator/linter và kiểm tra accessibility; lưu kết quả hoặc ảnh chụp làm minh chứng bàn giao.
6. Nếu triển khai công khai, xác nhận HTTPS, cấu hình hosting và việc không đưa dữ liệu nhạy cảm vào repository.

### Kết luận phê duyệt

- [ ] Đạt yêu cầu bàn giao chính thức.
- [ ] Chấp nhận bàn giao bản demo tĩnh với các giới hạn đã nêu.
- [ ] Chưa chấp nhận; yêu cầu khắc phục và kiểm thử lại.

**Người đánh giá:** ______________________________  
**Ngày xác nhận:** ____ / ____ / ______  
**Ghi chú:** ____________________________________________________________
