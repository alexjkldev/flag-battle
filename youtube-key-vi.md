# Flag Battle: khóa API YouTube của bạn

Chế độ streamer đọc trò chuyện trong buổi phát trực tiếp của bạn qua YouTube Data API. Không có khóa, bạn được dùng thử 5 phút mỗi ngày; với khóa miễn phí của riêng bạn, bạn có thể phát hàng giờ. Mất khoảng 5 phút.

## 1. Mở Google Cloud

Truy cập [console.cloud.google.com](https://console.cloud.google.com/) và đăng nhập bằng bất kỳ tài khoản Google nào (không cần là tài khoản của kênh). Chấp nhận điều khoản nếu được yêu cầu. Không cần thẻ tín dụng.

## 2. Tạo dự án

Ở đầu trang, nhấp vào bộ chọn dự án (**Select a project**), rồi **New project**. Tên nào cũng được, ví dụ `flag-battle`. Nhấp **Create** và kiểm tra dự án mới đã được chọn ở trên cùng — mọi bước sau đều làm trong đó.

## 3. Bật YouTube Data API v3 — trước khi tạo khóa

Mở [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) và nhấp **Enable**. API đã bật khi nút đổi thành **Manage**. Không có bước này, khóa sẽ không hoạt động.

## 4. Tạo khóa

Mở [Credentials](https://console.cloud.google.com/apis/credentials) → **Create credentials** → **API key**. Trong danh sách giới hạn API, chỉ đánh dấu **YouTube Data API v3**, rồi nhấp **Create**. Cửa sổ **API key created** hiện khóa của bạn — hãy sao chép.

Nếu không thấy YouTube Data API v3 trong danh sách, quay lại bước 3. Để giới hạn ứng dụng ở **None**.

## 5. Dán vào ứng dụng

Trong Flag Battle: màn hình chính → **Cài đặt** → chế độ **Đấu tay đôi** → **Chế độ streamer** → **Bật**. Chạm nút dán cạnh **Khóa YouTube API v3 của bạn** — không phải ô văn bản gợi ý bên dưới. Khóa chỉ lưu trên điện thoại của bạn, trong bộ nhớ bảo mật, và không bao giờ hiện trên màn hình.

## Nếu khóa bị từ chối

Khối **TIẾP THEO** cho biết lý do:

- **«YouTube Data API v3 chưa bật cho khóa này»** — làm bước 3 trong cùng dự án chứa khóa, rồi đợi vài phút.
- **«giới hạn của khóa chặn YouTube»** — mở khóa trong [Credentials](https://console.cloud.google.com/apis/credentials): giới hạn API phải có **YouTube Data API v3**, giới hạn ứng dụng phải là **None**.
- **«khóa YouTube không hợp lệ»** — khóa được sao chép chưa đủ: bắt đầu bằng `AIza` và dài 39 ký tự.

Sau đó quay lại menu và bắt đầu phát lại.

## Nên biết

- **Miễn phí.** Hạn mức tiêu chuẩn là 10.000 đơn vị mỗi ngày. Ở chế độ «Tức thì», trò chuyện đến theo thời gian thực và hạn mức đủ cho khoảng 6 giờ phát mỗi ngày; «Tiết kiệm» kéo dài lên khoảng 12 giờ, với độ trễ tối đa 10 giây. Bạn chọn chế độ trong ứng dụng.
- **Hạn mức được đặt lại lúc nửa đêm theo giờ Thái Bình Dương.** Nếu hết, ứng dụng sẽ hiển thị trong khối **TIẾP THEO** và các trận đấu tiếp tục với cờ ngẫu nhiên.
- Chỉ dùng dự án này cho Flag Battle để không có gì khác tiêu tốn hạn mức.
- Để thu hồi khóa, hãy xóa nó trong [Credentials](https://console.cloud.google.com/apis/credentials).
