# Xe Ở Đâu

**Xe Ở Đâu** là ứng dụng theo dõi vị trí xe theo thời gian thực, tận dụng **màn hình Android của xe hơi** làm thiết bị định vị GPS. Thay vì cần gắn thêm hộp định vị riêng, ứng dụng Android chạy trực tiếp trên màn hình xe, đọc tọa độ GPS và gửi dữ liệu về hệ thống quản lý trên website.

Website chính thức:

```text
https://xeodau.com
```

Thông tin dự án:

- Đơn vị phát triển: **1Touch Pro**
- Người phát triển: **Nguyễn Thái**
- Điện thoại: **0917833184**

## Giới Thiệu

Xe Ở Đâu được xây dựng để giúp người dùng biết xe đang ở đâu, đang di chuyển hay dừng đỗ, đã đi qua những tuyến đường nào và có thể xem lại lịch sử hành trình khi cần.

Ứng dụng phù hợp với xe hơi có màn hình Android, xe dịch vụ, xe gia đình, xe cá nhân hoặc các đội xe nhỏ cần một giải pháp theo dõi vị trí đơn giản, dễ triển khai và không phụ thuộc hoàn toàn vào thiết bị GPS rời.

## Ý Tưởng Chính

Màn hình Android trên xe hơi thường đã có sẵn GPS, kết nối internet và khả năng chạy ứng dụng nền. Xe Ở Đâu tận dụng chính thiết bị này để:

- Lấy vị trí GPS của xe.
- Gửi tọa độ về server theo thời gian thực.
- Hiển thị vị trí xe trên bản đồ website.
- Lưu lại lịch sử di chuyển để xem lại sau.

Cách tiếp cận này giúp giảm chi phí phần cứng, dễ cập nhật phần mềm và phù hợp với các xe đã có màn hình Android tích hợp.

## Chức Năng Chính

- Theo dõi vị trí xe theo thời gian thực trên bản đồ.
- Dùng màn hình Android của xe làm thiết bị gửi GPS.
- Quản lý nhiều xe trên cùng một tài khoản.
- Hiển thị trạng thái xe: đang chạy, tạm dừng, dừng đỗ lâu hoặc mất kết nối.
- Xem lại lịch sử vị trí và hành trình theo ngày.
- Thống kê quãng đường, tốc độ, thời gian di chuyển và thời gian dừng.
- Cảnh báo theo giới hạn tốc độ.
- Cấu hình thời gian cảnh báo khi xe dừng quá lâu.
- Hỗ trợ vùng giám sát cơ bản bằng geofence.
- Chia sẻ vị trí xe bằng link có thời hạn.
- Xuất dữ liệu hành trình sang GPX hoặc CSV.
- Quản lý người dùng và xe bằng trang quản trị.

## Ứng Dụng Android Trên Xe

Ứng dụng Android được thiết kế để chạy trên màn hình Android của xe hơi. Sau khi người dùng đăng nhập và chọn xe, ứng dụng sẽ gửi vị trí GPS về server trong quá trình xe hoạt động.

Ứng dụng có thể chạy dưới dạng foreground service để duy trì việc gửi vị trí ngay cả khi người dùng chuyển sang ứng dụng khác trên màn hình xe.

## Website Quản Lý

Website Xe Ở Đâu cho phép người dùng:

- Đăng ký và đăng nhập tài khoản.
- Đăng nhập bằng Google.
- Thêm, sửa, xóa thông tin xe.
- Xem vị trí hiện tại của xe trên bản đồ.
- Xem trạng thái hoạt động của từng xe.
- Xem lại lịch sử di chuyển.
- Tạo báo cáo hành trình theo ngày.
- Chia sẻ vị trí xe cho người khác khi cần.

## Dữ Liệu Và Hiệu Năng

Hệ thống sử dụng cơ sở dữ liệu phù hợp cho dữ liệu vị trí và dữ liệu theo thời gian:

- **PostgreSQL** để lưu dữ liệu chính.
- **PostGIS** để xử lý dữ liệu tọa độ và không gian.
- **TimescaleDB** để tối ưu lịch sử GPS theo thời gian.

Kiến trúc này giúp hệ thống phù hợp hơn khi số lượng xe, số điểm GPS và lượng truy cập tăng lên.

## Trường Hợp Sử Dụng

- Chủ xe muốn theo dõi vị trí xe cá nhân.
- Gia đình muốn biết xe đang ở đâu khi người thân sử dụng.
- Xe dịch vụ cần ghi nhận lịch sử di chuyển.
- Đội xe nhỏ cần quản lý vị trí mà không muốn đầu tư thiết bị GPS rời.
- Xe đã có màn hình Android và muốn tận dụng làm thiết bị định vị.

## Trạng Thái Dự Án

Dự án hiện đã có các thành phần chính:

- Website quản lý và bản đồ theo dõi xe.
- API backend xử lý người dùng, xe và vị trí GPS.
- Ứng dụng Android gửi vị trí từ màn hình Android của xe.
- Lưu lịch sử hành trình.
- Hỗ trợ PostgreSQL, PostGIS và TimescaleDB.

## Ghi Chú

Xe Ở Đâu hướng đến một giải pháp định vị linh hoạt, dễ triển khai, tận dụng phần cứng có sẵn trên xe và có thể mở rộng thêm các tính năng quản lý hành trình, cảnh báo và phân tích dữ liệu trong tương lai.
