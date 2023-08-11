Là cách mà các thiết bị mạng được kết nối với nhau trong một hệ thống mạng. Nó mô tả cấu trúc vật lý hoặc logic của mạng, bao gồm cả các mà các thiết bị được liên kết với nhau và truyền thông giữa chúng.

##### Một số loại cấu trúc mạng phổ biến:
1. **Point-to-point topology**: Các thiết bị mạng kết nối <font style="color:YellowGreen;font-weight:700">trực tiếp</font> với nhau và dành <font style="color:CadetBlue;font-weight:700">toàn bộ</font> băng thông để giao tiếp với nhau.
2. **Bus topology**: Các thiết bị mạng được kết nối với một <font style="color:LightGreen;font-weight:700">đường truyền chung</font> (thường là một đoạn cáp) duy nhất.
	- Ưu điểm:
		 Dễ <abbr title="Bus topology dễ dàng cài đặt và mở rộng. Khi bạn muốn thêm một thiết bị mới vào, chỉ cần kết nối nó với đoạn cáp chung">cài đặt và thay đổi</abbr>
		 Giá thành <abbr title="Dùng ít dây hơn các loại khác">thấp</abbr>
		 Đơn giản, dễ hiểu
		 Hiệu năng tốt (với lượng thiết bị nhỏ)
	- Nhược điểm:
		 Sự đụng độ dữ liệu[^1]
		 Khả năng <abbr title="Nếu đoạn cáp chia sẻ bị hỏng, toàn bộ mạng sẽ trở nên gián đoạn, khó truy vết lỗi dẫn đến khó khăn trong việc sửa chữa">chịu lỗi thấp</abbr>
		 Hiệu suất <abbr title="Khi số lượng thiết bị và dữ liệu trên mạng tăng lên, mà các thiết bị vẫn dùng chung một dây cáp. Điều này dẫn đến lưu lượng băng thông dành cho mỗi thiết bị sẽ bị giảm dẫn đến tốc độ cũng giảm">giới hạn</abbr>
		 Khả năng <abbr title="Vì dùng chung một đoạn cáp nên dữ liệu truyền tải có thể bị đánh cắp">bảo mật thấp</abbr>
		 Khó khăn trong quản lý
3. **Hub and spoke topology (*hay Star topology*)**: Các thiết bị mạng được kết nối trực tiếp với <font style="color:PaleTurquoise;font-weight:700">một thiết bị trung tâm</font>, thường là một bộ định tuyến hoặc chuyển mạch. 
	- Ưu điểm:
		 Dễ <abbr title="Muốn thêm hoặc loại bỏ thiết bị khỏi mạng, chỉ cần làm việc với thiết bị trung tâm">cài đặt và quản lý</abbr>
		 Dễ <abbr title="Khi sự cố xảy ra ở một thiết bị, sẽ không ảnh hưởng đến thiết bị khác">xác định và khắc phục sự cố</abbr>
		 Khả năng <abbr title="Có thể thêm nhiều thiết bị mạng mới bằng cách kết nối trực tiếp nó với thiết bị trung tâm">mở rộng tốt</abbr>
		 Tái cấu trúc <abbr title="tái cấu trúc không ảnh hưởng đến thiết bị khác">linh hoạt</abbr>
	- Nhược điểm:
		 Phụ thuộc vào thiết bị trung tâm
		 Chi phí cao hơn
		 Hiệu suất có thể bị <abbr title="chịu sự quyết định của thiết bị trung tâm">giới hạn</abbr>
4. **Tree topology**: Mô hình <font style="color:SpringGreen;font-weight:700">mở rộng từ</font> *Star topology* và kết hợp với các mạng con để tạo thành một cấu trúc hình cây. Trong tree topology, các thiết bị mạng được tổ chức thành các tầng hoặc cấp độ, giống như một cây thụ đầy nhánh.
	- Cách hoạt động:
		 1. Thiết bị gốc (root device): Có một thiết bị gốc ở cấp độ cao nhất của cây. Thông thường là một máy chủ hoặc bộ định tuyến quan trong trong mạng.
		 2. Cấp độ con (child level): Từ thiết bị gốc, dùng dây cáp hoặc cách khác để kết nối thiết bị ở các cấp độ con. Có thể là máy tính, máy chủ hoặc thiết bị mạng khác.
		 3. Cấp độ lát (leaf level): Thiết bị không có thiết bị con nào được kết nối với chúng.
	- Ưu điểm:
		 Mở rộng <abbr title="Chỉ cần thêm thiết bị vào thiết bị ở cấp độ con hoặc lá">dễ dàng</abbr>
		 Quản lý tốt
		 Tích hợp nhiều topology khác nhau
	- Nhược điểm:
		 Sự cố <abbr title="Khi sự cố xảy ra ở một cấp độ thì toàn bộ con và lá của nó sẽ bị ảnh hưởng">ảnh hưởng đến toàn bộ nhánh</abbr>
		 Phụ thuộc vào thiết bị gốc
		 Chi phí cao hơn
5. **Mesh topology**: Các thiết bị mạng được kết nối trực tiếp với <font style="color:Aquamarine;font-weight:700">tất cả (hay nhiều)</font> thiết bị khác trong mạng. Việc này tạo ra một mô hình mạng <font style="color:DarkSeaGreen;font-weight:700">rất linh hoạt và có khả năng chịu lỗi cao</font>.
	- Phân loại:
		1. Full Mesh Topology (Lưới đầy đủ): mỗi thiết bị kết nối trực tiếp với tất cả thiết bị khác trong mạng.
		2. Partial Mesh Topology (Lưới một phần): một số thiết bị được kết nối trực tiếp với tất cả thiết bị khác, trong khi một số chỉ kết nối với một số thiết bị khác.
	- Ưu điểm:
		 Khả năng <abbr title="Khi một đường truyền bị hỏng, ta vẫn có thể kết nối thông qua một đường truyền khác">chịu lỗi cao</abbr>
		 Hiệu suất <abbr title="Nhiều đường kết nối có thể hoạt động đồng thời">cao và băng thông lớn</abbr>
		 Bảo mật <abbr title="Với nhiều đường kết nối trực tiếp nên dữ liệu không phải đi qua các thiết bị trung gian">tốt hơn</abbr>
	- Nhược điểm:
		 Cài đặt và quản lí phức tạp
		 Chi phí cao
		 Không phù hợp với mạng nhỏ
6. **Ring topology**: Các thiết bị được kết nối với nhau thành một vòng khép kín. Dữ liệu được truyền theo một hướng cố định. Thiết bị sẽ nhận và chuyển tiếp cho đến khi đến được thiết bị gốc[^2].
	- Ưu điểm:
		 Dễ <abbr title="Dễ cài đặt và quản lý hơn so với các mô hình phức tạp">cài đặt và quản lý</abbr>
		 Hiệu suất <abbr title="Ít gặp đụng độ dữ liệu, tốc độ truyền nhanh khi có ít thiết bị">tốt</abbr> trong mạng nhỏ
		 Phản hồi <abbr title="Vì dữ liệu chỉ di chuyển theo một hướng nên phản hồi nhanh hơn so với một số mô hình khác">nhanh</abbr>
	- Nhược điểm:
		 Khả năng <abbr title="Việc lỗi sẽ ảnh hưởng đến toàn bộ hệ thống">chịu lỗi thấp</abbr>
		 Khó khăn trong việc <abbr title="Phải can thiệp thủ công để thêm thiết bị mới">thêm thiết bị mới</abbr>
		 Số lượng thiết bị <abbr title="Càng nhiều thiết bị khiến cho thời gian hoàn thành một vòng truyền tải sẽ lâu hơn">tỉ lệ nghịch với hiệu suất</abbr>
7. **Hybric topology**: Mô hình <font style="color:LightBlue;font-weight:700">kết hợp nhiều loại topology</font> để tạo ra một mô hình <font style="color:LightGreen;font-weight:700">phức tạp hơn</font>, <font style="color:CadetBlue">phù hợp với các yêu cầu cụ thể</font> của mạng.
	- Ưu điểm:
		 Tích hợp nhiều loại topology
		 Tùy chỉnh cho yêu cầu cụ thể
		 Tối ưu hóa hiệu suất và bảo mật
	- Nhược điểm:
		 Phức tạp trong cài đặt và quản lí
		 Chi phí cao hơn





[^1]: Khi hai hay nhiều thiết bị cố gắng truyền dữ liệu cùng một lúc, xung đột có thể xảy ra và gây mất hoặc làm hỏng dữ liệu.
[^2]: Truyền cho đến khi quay về lại thiết bị gốc để tạo thành một vòng khép kín.