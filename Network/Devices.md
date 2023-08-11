
1. **Repeater**: Hoạt động ở tầng vật lý (physical layer). Tái tạo lại tín hiệu trước khi nó trở nên yếu hoặc ngắt để mở rộng tín hiệu truyền tải qua cùng một mạng
   => <font style="color:LightCoral;font-weight:500">Mở rộng và tái tạo tín hiệu</font>
2. **Hub**: Được xem như là Repeater với nhiều cổng (multi-port repeater) Nhân bản traffics[^1] rồi truyền cho tất cả các cổng, không thể lọc dữ liệu, không có trí thông minh để tìm đường truyền tốt nhất 
   => <font style="color:LightCoral;font-weight:500">Bảo mật kém, kém hiệu quả, lãng phí</font>
3. **Bridge**:  Hoạt động ở tầng liên kết dữ liệu (data-link layer). Là một con repeater được thêm chức năng lọc nội dung bằng các đọc địa chỉ MAC ([[MAC Address]]) của nguồn và đích. Có một đầu vào và một đầu ra.
   => <font style="color:LightCoral;font-weight:500">Thường được dùng để kết nối 2 mạng LAN dùng chung phương thức (protocol)</font>
4. **Switch**: Là một chiếc bridge có nhiều cổng (multi-port bridge) có một buffer[^1] và được thiết kế để có thể tăng sự <abbr title="càng nhiều cổng thì lưu lượng truy cập sẽ nhỏ hơn">hiệu quả</abbr> và hiệu suất. Switch có thể kiểm tra lỗi trước khi chuyển tiếp dữ liệu.
   => <font style="color:LightCoral;font-weight:500">Mang tính hiệu quả cao, chỉ chuyển tiếp gói tin <font style="color:LightGreen;;font-weight:700">không lỗi</font> vào đúng cổng mà nó cần được chuyển tới</font> 
5. **Router**: Một thiết bị thường hoạt động ở tầng Network (network layer). Là một thiết bị giống như switch có khả năng xác định hướng đi (route) của gói dữ liệu dựa trên địa chỉ IP. 
   => <font style="color:LightCoral;font-weight:500">Dùng để kết nối nhiều mạng với nhau và xác định đường đi của gói dữ liệu</font>