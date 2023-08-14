Là một dịch vụ quản lý quyền truy cập được cung cấp bởi Amazon Web Services. IAM cho phép bạn quản lý quyền và đặc quyền truy cập đối với các tài nguyên và dịch vụ trong môi trường AWS của bạn. Giúp kiểm soát được ai có quyền truy cập vào tài nguyên cũng như dịch vụ nào trong tài khoản AWS của bạn.

###### Chức năng chính:
1. **Người dùng và nhóm** (Users & User groups): Tạo ra người dùng hoặc nhóm người dùng với các quyền truy cập. Người dùng có thể gán quyền truy cập độc lập hoặc thông qua nhóm.
2. **Vai trò** (Roles): Cho phép cung cấp quyền truy cập cho các dịch vụ hoặc nguồn bên ngoài, như các dịch vụ AWS khác hoặc ứng dụng của bạn mà không cần chia sẻ thông tin đăng nhập.
3. **Chính sách** (Policies): Là các tài liệu có thể được đính kèm vào người dùng, nhóm hoặc vai trò, xác định các hành động mà họ được phép thực hiện trên các tài nguyên cụ thể.
4. **Xác thực đa yếu tố** (MFA): IAM hổ trợ xác thực bằng nhiều yếu tố để tăng cường bảo mật.
5. **Ghi nhật ký** (Logging): Ghi nhật ký để giúp cho việc kiểm tra lịch sử hoạt động của người dùng, giúp theo dõi và kiểm tra các thay đổi quyền truy cập.
###### Tài khoản ROOT
- Là tài khoản được khi lần đầu tạo AWS.
- Có thể được truy cập bằng email và mật khẩu dùng khi tạo tài khoản AWS.
###### Người dùng
- Là một đơn vị được tạo trong AWS IAM
- Tượng trưng cho người hoặc ứng dụng tương tác với các dịch vụ và tài nguyên của AWS
- Nó bao gồm tên và phương thức xác minh (credentials)
- Mặc định người dùng mới tạo sẽ không có quyền (permission).
###### Nhóm
- Một nhóm IAM là một tập hợp các người dùng.
- Khi mà gắn một chính sách (policy) vào một nhóm, tất cả người dùng trong nhóm đều sẽ nhận được quyền mà chính sách cung cấp.
- Gắn một chính sách ở cấp độ nhóm sẽ giúp việc điều chỉnh quyền khi một người dùng chuyển sang vai trò khác dễ dàng hơn.
###### Chính sách
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

###### Vai trò (Roles)