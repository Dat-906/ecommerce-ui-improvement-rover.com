# AI Usage Log

## 1. Công cụ AI
ChatGPT (Nhiệm vụ 2 — phân tích giao diện); Claude (Nhiệm vụ 3 — đề xuất bố
cục và hỗ trợ viết mã nguồn).

## 2. Mục đích sử dụng
- Phân tích 5 khu vực chức năng của Rover.com (trang chủ, danh mục dịch vụ,
  hồ sơ sitter, tìm kiếm, đặt lịch/thanh toán) để xác định điểm thuận tiện
  và điểm có thể cải tiến.
- Đề xuất bố cục HTML/CSS cho khu vực thẻ sitter trước khi viết mã nguồn.

## 3. Prompt đã sử dụng

### Prompt 1 — Phân tích giao diện (Nhiệm vụ 2)
```
Bạn là chuyên gia phân tích nghiệp vụ và thiết kế trải nghiệm người dùng
cho website thương mại điện tử.

Tôi đang khảo sát website: Rover (https://www.rover.com/) - nền tảng kết
nối người nuôi thú cưng với sitter cung cấp dịch vụ trông giữ, dắt đi dạo,
ở lại qua đêm.

Hãy giúp tôi lập bảng phân tích các khu vực:
1. Trang chủ.
2. Danh mục dịch vụ.
3. Trang chi tiết (hồ sơ sitter).
4. Tìm kiếm.
5. Đặt lịch / thanh toán.

Với mỗi khu vực, hãy nêu:
- Mục đích của chức năng.
- Thành phần giao diện cần có.
- Điểm thuận tiện đối với khách hàng.
- Một vấn đề có thể phát sinh.
- Một đề xuất cải tiến.

Không khẳng định những tính năng chưa được kiểm chứng.
Phân biệt rõ nhận xét dựa trên quan sát và đề xuất của AI.
```

### Prompt 2 — Đề xuất bố cục thẻ sitter (Nhiệm vụ 3, bước 2)
```
Tôi đang thực hiện bài tập phát triển giao diện website thương mại điện tử
bằng HTML5 và CSS3.

Vấn đề quan sát được: Trên nền tảng đặt dịch vụ trông giữ thú cưng
(tham khảo Rover.com), danh sách sitter hiện hiển thị dạng hàng dài,
độ dài nội dung không đều giữa các mục, khiến khách hàng khó so sánh
nhanh giá, đánh giá và khoảng cách giữa nhiều sitter cùng lúc. Giá
hiển thị dạng "from $X" cũng chưa rõ ràng về tổng chi phí.

Tôi muốn cải tiến khu vực này thành dạng thẻ lưới (card grid), mỗi
thẻ gồm: ảnh sitter, tên, giá theo đêm/buổi, số sao đánh giá, khoảng
cách, nút "Đặt lịch", nút lưu yêu thích.

Đối tượng sử dụng: khách hàng nuôi thú cưng tại Việt Nam cần tìm
người chăm thú cưng.

Hãy đề xuất:
1. Bố cục giao diện.
2. Các thành phần HTML cần sử dụng.
3. Cách tổ chức CSS.
4. Cách hiển thị trên máy tính và điện thoại.
5. Những điểm cần kiểm tra về khả năng sử dụng.

Trước tiên, hãy giải thích phương án thiết kế.
Chưa tạo toàn bộ mã nguồn cho đến khi tôi yêu cầu.
```

## 4. Kết quả AI đề xuất
- **Prompt 1**: AI trả về bảng phân tích 5 khu vực, tách riêng phần "Quan
  sát" (dựa trên website/tài liệu chính thức của Rover) và "Đề xuất AI/Giả
  thuyết UX" (chưa kiểm chứng). Đề xuất nổi bật: làm rõ sự khác biệt giữa
  các loại dịch vụ, bổ sung tóm tắt nổi bật ở đầu hồ sơ sitter, cho phép
  lưu hồ sơ để so sánh, minh bạch tổng chi phí trước khi xác nhận đặt lịch.
- **Prompt 2**: AI đề xuất chuyển bố cục từ danh sách hàng dài sang lưới
  thẻ (CSS Grid), nhóm thông tin quan trọng vào vị trí cố định trên mỗi
  thẻ, dùng `<article>` cho mỗi thẻ sitter, và điều chỉnh số cột lưới theo
  kích thước màn hình bằng media query.

## 5. Kiểm tra và điều chỉnh
- Đã tự kiểm tra trực tiếp trên rover.com (trang tìm kiếm House Sitting tại
  New York), xác nhận các quan sát của AI đúng với thực tế: danh sách sitter
  hiển thị dạng hàng dài, độ dài nội dung không đều giữa các sitter (đoạn
  trích đánh giá dài/ngắn khác nhau), giá hiển thị dạng "from $X" mơ hồ về
  tổng chi phí — có ảnh chụp màn hình minh chứng.
- Không phát hiện ý nào AI bịa hoặc sai lệch so với website thật ở Prompt 1.
- Bố cục thẻ lưới do AI đề xuất ở Prompt 2 được giữ nguyên hướng; phần mã
  nguồn (màu sắc, nội dung mẫu, huy hiệu "Top sitter"/"Mới tham gia") do tôi
  tự điều chỉnh để phù hợp hơn với bối cảnh dịch vụ thú cưng tại Việt Nam.

## 6. Phần tôi hiểu và có thể giải thích
- Hiểu rõ sự khác biệt giữa "Quan sát" (sự thật trên web) và "Đề xuất AI"
  (giả thuyết UX cần kiểm chứng) — nguyên tắc AI tự đặt ra và tôi đã dùng
  để lọc lại kết quả trước khi đưa vào báo cáo.
- Hiểu cách CSS Grid (`display: grid; grid-template-columns`) tạo lưới thẻ
  co giãn, và cách `@media (max-width: ...)` đổi số cột theo kích thước
  màn hình để làm giao diện responsive.
- Hiểu vì sao dùng `<article>` cho mỗi thẻ sitter (mỗi thẻ là một đơn vị
  nội dung độc lập, đúng ngữ nghĩa HTML5) thay vì `<div>` thông thường.
