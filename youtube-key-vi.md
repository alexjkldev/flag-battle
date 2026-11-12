# Flag Battle: khóa API YouTube của bạn

Chế độ streamer đọc trò chuyện trong buổi phát trực tiếp của bạn qua YouTube Data API. Không có khóa, bạn được dùng thử 5 phút mỗi ngày; với khóa miễn phí của riêng bạn, bạn có thể phát hàng giờ. Mất khoảng 5 phút.

## 1. Mở Google Cloud

Truy cập [console.cloud.google.com](https://console.cloud.google.com/) và đăng nhập bằng bất kỳ tài khoản Google nào (không cần là tài khoản của kênh). Chấp nhận điều khoản nếu được yêu cầu. Không cần thẻ tín dụng.

## 2. Tạo dự án

Ở đầu trang, nhấp vào bộ chọn dự án (**Select a project**), rồi **New project**. Đặt tên gì cũng được, ví dụ `flag-battle`. Nhấp **Create** và kiểm tra rằng dự án mới đã được chọn ở đầu trang.

## 3. Bật YouTube Data API

Mở [YouTube Data API v3](https://console.cloud.google.com/apis/library/youtube.googleapis.com) và nhấp **Enable**.

## 4. Tạo khóa

Mở [Credentials](https://console.cloud.google.com/apis/credentials), nhấp **Create credentials** → **API key**. Mở khóa mới để chỉnh sửa:

- **API restrictions** → **Restrict key** → chỉ đánh dấu **YouTube Data API v3**. Khi đó, khóa bị lộ cũng không dùng được vào việc khác.
- **Application restrictions** có thể để **None**.

Nhấp **Save**, rồi sao chép khóa (**Show key** → sao chép).

## 5. Dán vào ứng dụng

Trong Flag Battle, mở **Cài đặt → Đấu tay đôi → Chế độ streamer** và chạm vào nút dán cạnh ô khóa API YouTube. Khóa chỉ được lưu trên điện thoại của bạn, trong bộ nhớ an toàn, và không bao giờ hiển thị trên màn hình.

## Nên biết

- **Miễn phí.** Hạn mức tiêu chuẩn là 10.000 đơn vị mỗi ngày. Nếu đọc trò chuyện mỗi 8 giây, hạn mức đủ cho khoảng 4,4 giờ phát mỗi ngày (mỗi 5 giây ≈ 2,8 giờ, mỗi 10 giây ≈ 5,6 giờ); bạn chọn khoảng thời gian trong ứng dụng.
- **Hạn mức được đặt lại lúc nửa đêm theo giờ Thái Bình Dương.** Nếu hết, ứng dụng sẽ hiển thị trong khối **TIẾP THEO** và các trận đấu tiếp tục với cờ ngẫu nhiên.
- Chỉ dùng dự án này cho Flag Battle để không có gì khác tiêu tốn hạn mức.
- Để thu hồi khóa, hãy xóa nó trong [Credentials](https://console.cloud.google.com/apis/credentials).
