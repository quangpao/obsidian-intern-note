Là một giao thức hướng dữ liệu được sử dụng bởi các máy chủ nguồn và đích để truyền dữ liệu trong một liên mạng chuyển mạch gói. Hiện nay có 2 phiên bản, là [[IPv4]] và [[IPv6]].

- Hoạt động ở tầng Internet trong mô hình TCP/IP.
	- Tầng 3 trong mô hình OSI
- Là giao thức định tuyền cốt lõi của Internet.
- Giải quyết với việc truyền tải gói giữa các điểm cuối (endpoint).
- Xác định lược đồ địa chỉ cho Internet.

##### IPv4 Header
Là phần đầu của gói tin IPv4 (Phân biệt với IPv6), chứa thông tin cần thiết cho việc định tuyến và giao nhận.

![[IPv4 Header.png|white]]

- Key Fields:
	1. IP Version: Xác định phiên bản của IP
	2. Protocol: Xác định giao thức đóng gói
	3. TTL (Time To Live): Số lượng bước nhảy (hop) mà gói được cho phép thực hiện để đạt được đích đến.
	4. Fragmentation (Flags + Fragment offset): Dùng để phân mảnh hay tách các gói thành các gói độc lập nhỏ hơn.
	5. Source & Destination address