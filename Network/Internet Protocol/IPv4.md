- Là một địa chỉ IP độc nhất dùng để xác định một thiết bị ở trên không gian mạng hay cục bộ (IP Network).
- Gồm 32-bit địa chỉ, phân thành 4 đoạn 8-bit nhỏ hơn có dạng
  0.0.0.0 => 255.255.255.255 (Ví dụ: <font style="color:LightGreen">192.168.1.15</font>)
- Một phần được coi là network (<font style="color:LightBlue">192.168.1</font>), phần còn lại là host (<font style="color:LightBlue">15</font>)
- Có thể được cài đặt bởi người dùng
- Được sử dụng để xác định đường truyền (path)

###### Các địa chỉ đặc biệt (Dùng cho mục đích cá nhân)
- 10.0.0.0 -> 10.255.255.255
- 172.16.0.0 -> 172.31.255.255
- 192.168.0.0 -> 192.168.255.255
- Auto configuration IP addresses: 169.254.0.0 -> 169.254.255.255
- Loop back IP addresses: 127.0.0.0 -> 127.255.255.255
- Multicast IP addresses: 224.0.0.0 -> 239.255.255.255

###### Địa chỉ công khai (Public IP)
Là địa chỉ có thể được truy cập trực tiếp từ Internet.

###### Ký hiệu (Notation)
Thường có 2 loại:
- Subnet mask: 10.10.10.10 255.255.0.0
- CIDR[^1] : 10.10.10.10/16



[^1]: [[Classless Inter-Domain Routing]]