#### Làm bài một bài Powerpoint để giải thích cách hoạt động của web.

###### Web là gì?
Web (hay W3[^1]) là tập hợp tất cả các trang web mà người dùng có thể truy cập từ máy tính cá nhân khi truy cập Internet.

###### Web có gì?
Web thường chứa các văn bản, hình ảnh, video, cùng các tài liệu khác. Các trang web được tạo ra bằng cách dùng HTML để định dạng và cấu trúc nội dung, cùng với CSS để tạo ra giao diện thẫm mỹ, và Javascript để thêm các tính năng tương tác.

###### Làm sao để truy cập một trang web?
Để truy cập vào trang web, ta có thể dùng URL[^2] để truy cập thông qua các web browser.

#### Cách một trang web hoạt động:
#web, #how-to 
##### <font style="color:Aquamarine">Diễn giải theo cách bản thân hiểu</font>:
1. Người dùng sử dụng browser yêu thích để truy cập.
2. Người dùng nhập URL của trang web lên thanh <font style="color:LightSalmon">search bar</font>.
3. URL hay domain của URL sẽ được DNS[^3] kiểm tra và phân giải thành địa chỉ IP của trang web.
4. Sau khi có được IP của trang web, thì browser sẽ gửi một gói tín hiệu TCP chứa IP nguồn, về IP đích đã được giải mã.
5. Tín hiệu sao khi về máy chủ của IP đích sẽ được xử lí để trả về dữ liệu mà bên client yêu cầu.

##### <font style="color:SkyBlue">Diễn giải phong cách ChatGPT</font>:
1. Người dụng nhập địa chỉ URL:
	- Bạn nhập một địa chỉ web vào thanh địa chỉ của trình duyệt
2. Trình duyệt tạo yêu cầu đến DNS
	- Trình duyệt tạo yêu cầu để chuyển đổi tên miền thành địa chỉ IP tương ứng.
3. Yêu cầu sẽ được gửi đến máy chủ DNS
	- Máy chủ DNS nhận yêu cầu
4. Máy chủ DNS truy vấn tên miền
	- Máy chủ DNS truy vấn trong cơ sở dữ liệu để tìm thông tin về tên miền bạn đã nhập
5. Trả về địa chỉ IP
	- Sau khi tìm được địa chỉ IP của tên miền, máy chủ DNS sẽ trả về lại IP của tên miền đó cho trình duyệt
6. Trình duyệt người yêu cầu HTTP
	- Trình duyệt sử dụng địa chỉ IP đã được chuyển đổi để gửi yêu cầu (request) về máy chủ. Thường thì sẽ là GET, hoặc POST.
7. Máy chủ xử lý yêu cầu và trả về dữ liệu
	- Máy chủ sau khi nhận được yêu cầu thì sẽ xử lí và trả về dữ liệu cho trình duyệt.
	- Ở đây ta sẽ xét một trường hợp cụ thể là request một trang web bằng method GET:
		- Máy chủ sẽ trả về một phản hồi (response) HTTP chứa trang web được yêu cầu và các dữ liệu liên quan. 
8. Trình duyệt hiển thị dữ liệu
	- Trình duyệt nhận phản hồi và hiển thị trang web được yêu cầu ra màn hình


[^1]: [World Wide Web](https://en.wikipedia.org/wiki/World_Wide_Web)
[^2]: [Uniform Resource Locator](https://vi.wikipedia.org/wiki/URL)
[^3]: [Domain Name System](https://en.wikipedia.org/wiki/Domain_Name_System)