Thường được dùng để mô tả hay khi nói về các tầng của ngăn xếp giao thức (Protocol Stack).
- Gồm 7 tầng:
	1. Tầng vật lý (**Physical**): Là tầng đầu tiên, cũng như tầng thấp nhất trong mô hình OSI, dùng để <font style="color:LightBlue">chuyển đổi dữ liệu dưới dạng bit</font> thông qua cáp hoặc các phương tiện vật lý.
	2. Tầng liên kết (**Data-link**): Chia nhỏ <font style="color:LightGreen">packet thành các frame</font> và ngược lại. Thực hiện <font style="color:LightCoral">checksum</font>[^1] để kiểm tra lại dữ liệu. 
	3. Tầng mạng (**Network**): Gắn IP để <font style="color:LightBlue">định tuyến đích</font> gói tin.
	4. Tầng giao vận (**Transport**): <font style="color:Aquamarine">Chia dữ liệu (Data) thành các packet nhỏ hơn</font> và ngược lại. Thực hiện checksum để kiểm tra tính toàn vẹn của dữ liệu.
	5. Tầng phiên (**Session**): <font style="color:LightCyan">Kiểm soát (Quản lý) các phiên</font> giao tiếp giữa các máy tính.
	6. Tầng trình bày (**Presentation**): <font style="color:LightCoral">Chuyển đổi, nén dữ liệu, mã hóa, giải mã</font>.
	7. Tầng ứng dụng (**Application**): Là nơi <font style="color:#6A5ACD">tương tác với các ứng dụng và mạng</font>. 


[^1]: [[Checksum]]