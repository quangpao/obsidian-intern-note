##### Điện toán đám mây (Cloud Computing)
Là dịch vụ cung cấp tài nguyên dịch vụ điện toán[^1] theo yêu cầu trên Internet với định giá thanh toán theo mức sử dụng.

##### Mô hình triển khai (Deployment Models for Cloud Computing)
Có ba loại mô hình triển khai điện toán đám mây:
- [[Cloud-based]]: Triển khai hoàn toàn ở trên đám mây (ở đây là AWS)
- [[On-premises]]: Triển khai ở máy chủ vật lý, dùng ảo hóa và các công cụ quản lý
- [[Hybrid]]: Kết hợp giữa On-premises và Cloud-based, một phần sẽ được triển khai trên máy chủ vật lý, phần còn lại ở trên Cloud.

##### Lợi ích của Điện toán đám mây
- Chi phí linh hoạt: Các dịch vụ đám mây cho phép trả theo mức sử dụng, tránh việc đầu tư lớn vào hạ tầng máy chủ và phần mềm.
- Linh hoạt mở rộng: Dễ dàng mở rộng tài nguyên và khả năng xử lý khi nhu cầu tăng lên và thu hẹp lại khi nhu cầu giảm.
- Tiết kiệm thời gian: Các dịch vụ đám mây thường cung cấp tài nguyên và môi trường sẵn, tiết kiệm thời gian triển khai và cấu hình.
- Truy cập từ xa: Có thể truy cập vào dữ liệu và ứng dụng từ bất cứ đâu có kết nối Internet.
- Cập nhật tự động: Các dịch vụ đám mây thường tự động cập nhật phần mềm và bảo mật, giúp duy trì phiên bản mới nhất, bảo vệ khỏi lỗ hổng bảo mật.
- Hiệu suất và khả năng mở rộng
- Bảo mật và tuân thủ quy định
- Khả năng sao lưu và khôi phục
- Tiết kiệm không gian
- Tích hợp dễ dàng

##### Lịch sử phát triển
![[AWS History.png]]

##### Trường hợp sử dụng
- Cho phép xây dựng ứng dụng có độ phức tạp cao và khả năng mở rộng
- Khả năng cung cấp cho một tập hợp ngành công nghiệp phong phú
- Bao gồm:
	- Doanh nghiệp công nghệ thông tin, Sao lưu và lưu trữ, phân tích dữ liệu lớn
	- Web Hosting[^2], Ứng dụng di động, xã hội
	- Trò chơi (Gaming)

##### Cơ sở hạ tầng của AWS Cloud
- **AWS Regions** (Khu vực): Là một khu vực địa lý tách biệt, một khu vực có thể có nhiều AZ (Available Zones).
- **AWS Availability Zones** (Vùng khả dụng): Là một khu vực chứa các trung tâm dữ liệu, mỗi AZ đều tách biệt với nhau về mặt địa lý.
- **AWS Data Centers** (Trung tâm dữ liệu): Là một vị trí vật lý nơi mà lưu trữ các máy tính và những phần cứng liên quan.
- **AWS Edge Location/Point of Presence** (Điểm hiện diện): Là nơi mà End-User (người dùng cuối) có thể truy cập đến dịch vụ của AWS để giảm độ trễ khi request và nhận dữ liệu.

##### AWS Service
- [[AWS Identity and Access Management (IAM)]]
- 
[^1]: Bao gồm servers, storage, databases, networking, software, analytics, intelligence,...