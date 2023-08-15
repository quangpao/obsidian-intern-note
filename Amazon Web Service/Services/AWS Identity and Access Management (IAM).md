Là một dịch vụ <font style="color:LightGreen">quản lý quyền truy cập</font> được cung cấp bởi Amazon Web Services. IAM cho phép bạn quản lý quyền và đặc quyền truy cập đối <font style="color:LightCoral">với các tài nguyên và dịch vụ</font> trong môi trường AWS của bạn. Giúp kiểm soát được ai có quyền truy cập vào tài nguyên cũng như dịch vụ nào trong tài khoản AWS của bạn.

###### <font style="color:LightBlue">Chức năng chính</font>:
1. **Người dùng và nhóm** (Users & User groups): Tạo ra người dùng hoặc nhóm người dùng với các quyền truy cập. Người dùng có thể <font style="color:LightGreen">gán quyền truy cập độc lập</font> hoặc <font style="color:LightGreen">thông qua nhóm</font>.
2. **Vai trò** (Roles): Cho phép <font style="color:LightGreen">cung cấp quyền truy cập</font> cho các dịch vụ hoặc nguồn bên ngoài, như các dịch vụ AWS khác hoặc ứng dụng của bạn mà <font style="color:LightCoral">không cần chia sẻ thông tin đăng nhập</font>.
3. **Chính sách** (Policies): Là các <font style="color:Tomato">tài liệu</font> có thể <font style="color:LightGreen">được đính kèm vào</font> người dùng, nhóm hoặc vai trò, <font style="color:LightGreen">xác định</font> các hành động mà họ <font style="color:LightCoral">được phép thực hiện</font> trên các tài nguyên cụ thể.
4. **Xác thực đa yếu tố** (MFA): IAM hổ trợ xác thực bằng nhiều yếu tố để <font style="color:Tomato">tăng cường bảo mật</font>.
5. **Ghi nhật ký** (Logging): Ghi nhật ký để giúp cho việc <font style="color:Tomato">kiểm tra lịch sử hoạt động</font> của người dùng, giúp theo dõi và kiểm tra các thay đổi quyền truy cập.
###### <font style="color:LightBlue">Tài khoản ROOT</font>
- Là tài khoản được khi lần đầu tạo AWS.
- Có thể được truy cập bằng email và mật khẩu dùng khi tạo tài khoản AWS.
###### <font style="color:LightBlue">Người dùng</font> (Users)
- Là một thực thể được tạo trong AWS IAM
- Tượng trưng cho người hoặc ứng dụng tương tác với các dịch vụ và tài nguyên của AWS
- Nó bao gồm tên và phương thức xác minh (credentials)
- Mặc định người dùng mới tạo sẽ không có quyền (permission).
###### <font style="color:LightBlue">Nhóm</font> (User Groups)
- Một nhóm IAM là một tập hợp các người dùng.
- Khi mà gắn một chính sách (policy) vào một nhóm, tất cả người dùng trong nhóm đều sẽ nhận được quyền mà chính sách cung cấp.
- Gắn một chính sách ở cấp độ nhóm sẽ giúp việc điều chỉnh quyền khi một người dùng chuyển sang vai trò khác dễ dàng hơn.
###### <font style="color:LightBlue">Chính sách</font> (Policies)
- Là một tài liệu cho phép hoặc từ chối quyền sử dụng các dịch vụ và tài nguyên của AWS.
- Cho phép bạn tùy chỉnh quyền truy cập tài nguyên của người dùng.
- **Cách người dùng kế thừa các chính sách trong IAM:**
![[Policy Inheritance.png]]
- **Cấu trúc một bộ chính sách**:
	- <font style="color:LightCoral">Bao gồm</font>:
		- <font style="color:LightBlue">Version</font>: Phiên bản của chính sách
		- <font style="color:LightBlue">Id</font>: Mã định danh cho chính sách
		- <font style="color:LightBlue">Statement</font>: 
			- <font style="color:LightGreen">Sid</font>: Mã định danh cho các khai báo độc lập
			- <font style="color:LightGreen">Effect</font>: Cho phép (Allow) hay chặn (Deny) quyền truy cập.
			- <font style="color:LightGreen">Principal</font>: Tài khoản, người dùng hay vai trò được gắn chính sách
			- <font style="color:LightGreen">Action</font>: Danh sách các hành động chính sách cho phép hay chặn
			- <font style="color:LightGreen">Resource</font>: Tài nguyên mà các hành động được phép truy cập
			- <font style="color:LightGreen">Condition</font>: Điều kiện hiệu lực của chính sách.

###### <font style="color:LightBlue">Vai trò</font> (Roles)
- Là một thực thể có thể tiêu thụ để nhận được quyền truy cập tạm thời.
- Để có thể sử dụng vai trò, trước tiên phải được cấp quyền để thay đổi vai trò.
- Khi một người đang ở trong một vai trò, thì tất cả quyền trước đó sẽ bị tước đi và thay thế bằng quyền mới.