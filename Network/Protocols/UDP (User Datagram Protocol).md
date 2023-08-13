Là một giao thức truyền tải dữ liệu trong mô hình TCP/IP. Dùng để gửi những gói dữ liệu (hay datagram) mà không cần phải thiết lập kết nối.

- UDP cho phép gửi các datagram mà không cần thiết lập kết nối trước.
- UDP có tốc độ truyền cao hơn TCP nhưng không đảm bảo việc giao nhận và sắp xếp các gói tin.
- Tốt nếu dùng cho những ứng dụng yêu cầu độ trễ thấp và cho phép sự mất mát dữ liệu.

###### Được dùng cho việc:
- Giao tiếp thời gian thực (Multimedia/VoIP)
- NTP
- Syslog
###### Các cổng UDP phổ biến:
- DNS (53)
- Bootp (67, 68)
- TFTP (69)
- NTP (123)
- SNMP (161, 162)
- NFS (2049)

###### UDP Header
![[UDP Header.png]]