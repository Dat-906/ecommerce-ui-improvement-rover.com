# Pet Sitter UI Improvement

## 1. Giới thiệu
Bài tập cá nhân (btcn) môn Phát triển ứng dụng WEB/TMĐT — khảo sát một website
thương mại điện tử thiên hướng dịch vụ chăm sóc thú cưng, dùng AI hỗ trợ phân
tích, và tự thiết kế lại một khu vực giao diện bằng HTML5/CSS3.

## 2. Website tham khảo
- Tên website: Rover
- URL: https://www.rover.com/
- Khu vực đã khảo sát và cải tiến: Danh sách/thẻ hiển thị người chăm thú cưng
  (sitter listing)

## 3. Chức năng
- Hiển thị danh sách sitter dạng thẻ lưới (card grid)
- Mỗi thẻ hiển thị: ảnh, tên, đánh giá (số sao + số lượt), khoảng cách, giá
  kèm đơn vị, nút "Đặt lịch", nút lưu yêu thích
- Bố cục responsive: 4 cột (desktop) → 2 cột (tablet) → 1 cột (mobile)

## 4. Công nghệ
- HTML5
- CSS3 (CSS Grid, Flexbox, Media Queries)

## 5. Cách chạy
Mở file `index.html` bằng trình duyệt (không cần máy chủ, không cần cài đặt
gì thêm).

## 6. Vấn đề quan sát được
Qua khảo sát thực tế trên rover.com (trang kết quả tìm kiếm House Sitting),
danh sách sitter hiển thị dạng hàng dài với độ dài nội dung không đều (đoạn
trích đánh giá dài ngắn khác nhau giữa các sitter), khiến khách hàng khó so
sánh nhanh giá, đánh giá và khoảng cách giữa nhiều sitter cùng lúc. Giá hiển
thị dạng "from $X" cũng chưa rõ ràng về tổng chi phí thực tế.

## 7. Cải tiến đã thực hiện
Thiết kế lại danh sách sitter thành dạng thẻ lưới (card grid) thay vì danh
sách hàng dài:
- Nhóm các thông tin quan trọng (ảnh, tên, giá, đánh giá) vào cùng một khung
  nhìn cố định trên mỗi thẻ, kích thước đồng đều, dễ quét mắt so sánh
- Giá hiển thị rõ đơn vị (`/đêm`, `/buổi`, `/ngày`) ngay cạnh số tiền
- Thêm huy hiệu nổi bật ("Top sitter", "Mới tham gia") giúp nhận diện nhanh
  sitter đáng tin mà không cần mở từng hồ sơ
- Thêm nút lưu yêu thích (♡/♥) ngay trên thẻ để so sánh nhiều sitter cùng lúc
- Bố cục responsive để hiển thị tốt trên điện thoại
- Đổi màu chủ đạo từ cam sang xanh biển rồi xanh lá đậm

## 8. Hỗ trợ từ AI
AI hỗ trợ phân tích giao diện gốc (Nhiệm vụ 2) và đề xuất phương án bố cục
thẻ lưới trước khi viết mã nguồn (Nhiệm vụ 3, bước 2). Toàn bộ quan sát được
đối chiếu lại với website thật và ảnh chụp màn hình thực tế trước khi đưa
vào báo cáo. Chi tiết prompt và quá trình kiểm tra xem tại `AI_USAGE.md`.
