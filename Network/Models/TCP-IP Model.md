Là kết hợp của các giao thức riêng biệt. TCP/IP chỉ rõ cho chúng ta cách đóng gói thông tin, gửi và nhận giữa các máy tính có kết nối với nhau.

- Gồm 4 tầng:
	1. Tầng vật lý (**Network Access**): Sự <font style="color:LightGreen">kết hợp giữa Data-link và Physical</font> trong mô hình OSI. Chịu trách nhiệm <font style="color:LightCoral">đóng khung</font> (frame) và <font style="color:LightCoral">truyền tải</font> đến địa chỉ được chỉ định[^1]
	2. Tầng mạng (**Internet**): <font style="color:LightCoral">Xử lý các gói</font> (packet) và <font style="color:LightCoral">kết nối các mạng độc lập</font> để vận chuyển các gói dữ liệu. <font style="color:LightCoral">Đánh địa chỉ</font> và <font style="color:LightCoral">dịch địa chỉ</font> <font style="color:LightGreen">logic -> địa chỉ vật lý</font>. Có 2 giao thức chính là IP và ICMP
	3. Tầng giao vận (**Transport**): Chịu trách nhiệm <font style="color:LightCoral">duy trì liên lạc đầu cuối</font> trên <font style="color:LightGreen">toàn mạng</font>. Có 2 giao thức chính là TCP và UDP.
	4. Tầng ứng dụng: (**Application**): <font style="color:LightCoral">Cung cấp</font> <font style="color:LightGreen">các ứng dụng</font> với <font style="color:LightCoral">trao đổi dữ liệu</font> <font style="color:LightGreen">được chuẩn hóa</font>, sử dụng các giao thức như HTTP,FTP, SMTP, DNS,...

##### [[Data Encapsulation]]


[^1]: Chỉ áp dụng cho các thiết bị trong cùng mạng.