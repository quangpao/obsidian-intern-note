AWS Elastic Compute Cloud là một dịch vụ cung cấp khả năng <font style="color:LightGreen">thuê và quản lý các máy ảo</font> trên nền tảng đám mây của AWS[^1]. EC2 cho phép người dùng triển khai và quản lý các máy ảo, được gọi là các "instances", trên hạ tầng điện toán đám mây của AWS.

- Là một trong những dịch vụ phổ biến nhất của AWS.
- Là một ví dụ điển hình cho mô hình [[Infrastructure as a Service]].

##### Cách hoạt động của EC2
1. **Chạy** (<font style="color:Tomato">Launch</font>): Đầu tiên, chạy instance[^2] bằng cách tùy chọn các cấu hình như hệ điều hành, mạng, loại ứng dụng,...
	- Có thể tùy chỉnh cấu hình về mặt bảo mật để thiết lập cách mà bên ngoài có thể truy cập vào trong instance hoặc từ instance ra bên ngoài.
2. **Kết nối** (<font style="color:Tomato">Connect</font>): Bạn có thể kết nối vào Instance bằng nhiều cách: SSH, RDP,...
3. **Sử dụng** (<font style="color:Tomato">Use</font>): Từ giờ, ta có thể sử dụng nó bằng cách dùng lệnh để cài đặt các phần mềm, thêm bộ nhớ,... Như một máy tính bình thường.

##### Lợi ích của EC2
- Có thể tạo vào chạy EC2 chỉ trong <font style="color:LightGreen">vài phút</font>.
- Có thể dừng sử dụng sau khi chạy xong.
- Chỉ phải chi trả thời gian mình sử dụng khi dịch vụ[^3] (service).
- <font style="color:LightGreen">Tiết kiệm</font> chi phí bởi chỉ cần trả cho lưu lượng mình cần.

##### Kích thước của EC2 và các tùy chỉnh thiết lập
- Hệ điều hành (OS): Linux, Windows, MacOS
- Sức mạnh điện toán & số nhân (CPU)
- Dung lượng RAM:
- Kích thước bộ nhớ (Storage):
	- Network-attached (EBS & EFS)
	- Hardware (EC2 Instance Store)
- Network Card: Tốc độ băng thông, địa chỉ công cộng (Public IP Address)
- Firewall rules: Security Group, Dùng để kiểm soát lưu lượng truy cập vào và ra khỏi Instance, hoạt động ở Transport Layer
- Bootstrap script: Kịch bản soạn sẵn, sẽ được tự động chạy khi EC được khởi động.

##### Các loại Instance
- Chúng ta có thể sử dụng nhiều loại Instance khác nhau phù hợp cho từng mục đích sử dụng khác nhau.
- Cách đặt tên Instance của AWS
	  <center><font style="color:LightGreen">c</font><font style="color:Tomato">7</font><font style="color:LightSalmon">g</font><font style="color:Yellow">n</font>.<font style="color:LightBlue">2xlarge</font></center>
	- <font style="color:LightGreen">c</font>: Instance families  (c: Compute Optimized)
	- <font style="color:Tomato">7</font>: Instance generation (7: Generation 7)
	- <font style="color:LightSalmon">g</font>: Processor family (g: AWS Graviton processors)
	- <font style="color:Yellow">n</font>: Additional capabilities (n: Network and EBS optimized)
	- <font style="color:LightBlue">2xlarge</font>: Instance Size (2xlarge: 8 vCPU)
- Các loại Instance:
	1. General Purpose
		- Dùng có các mục đích thông thường
	2. Compute Optimized
		- Tốt cho các mục đích yêu cầu khả năng tính toán cao
	3. Memory Optimized
		- Dùng cho các mục yêu cầu bộ nhớ xử lý lớn
	4. Storage Optimized
		- Dùng cho các tác vụ yêu cầu bộ nhớ lưu trữ cũng như truy vấn tuần tự

##### Security Groups trong EC2
- Là thành phần cơ bản về bảo mật mạng của AWS EC2
- Kiểm soát cách mà lượng truy cập đi vào hay đi ra khỏi EC2 instances
- Hoạt động như một "tường lửa" (firewall) của EC2
- Được quy định:
	- Quyền truy cập vào cổng
	- Cấp quyền cho các IPv4 và IPv6
	- Kiểm soát lượng truy cập từ ngoài vào Instance (Inbound Network)
	- Kiểm soát lượng truy cập từ instance ra ngoài (Outbound Network)
- Lưu ý:
	- Security Groups chỉ bao gồm các luật lệ (rule) được cho phép (allowed rules)
	- Các luật có thể được tham chiếu bằng IP hay bằng một security group khác.




[^1]: Hoặc có thể gọi là dịch vụ Virtual Private Server (VPS) của nhà AWS. 
[^2]: Giống như là một chiếc máy ảo thực thụ có thể đang được chạy hoặc dùng.
[^3]: Pay-as-you-go