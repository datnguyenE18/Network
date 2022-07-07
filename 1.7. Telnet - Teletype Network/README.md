# **Telnet - Teletype Network**

Telnet được biết đến là giao thức đầu tiên được sử dụng khi internet ra mắt lần đầu vào năm 1969. Sau đó giao thức này được thay thế bởi SSH. Tất cả ưu điểm của Telnet đã được SSH thừa hưởng. Đến nay ít ai nhắc đến Telnet



Có thể gọi Telnet là một giao thức dòng lệnh được sử dụng để quản lý các thiết bị khác nhau như máy chủ, PC, router, switch, camera, tường lửa từ xa...Hoặc Telnet là một giao thức máy tính cung cấp khả năng giao tiếp tương tác hai chiều cho các máy tính trên internet và mạng cục bộ LAN



Telnet có nhiệm vụ là cung cấp kết nối từ xa, đảm nhiệm việc gửi các lệnh hoặc dữ liệu đến kết nối mạng từ xa nên chúng rất phổ biến trong hệ thống mạng. Giao thức này xuất hiện vào năm 1969 và nó đáp ứng mọi nhu cầu cơ bản về giao diện dòng lệnh trên internet. Sau khi SSH ra đời là người kế nhiệm của Telnet nên đã giải quyết những nhược điểm của Telnet.

***

**Cấu trúc của Telnet**

Trong cấu trúc của Telnet sẽ bao gồm khách hàng (Client) và máy chủ (Server). Ở phía  máy chủ (Server) sẽ cung cấp dịch vụ Telnet. Dịch vụ này sẽ đưa đến và kết nối các ứng dụng của máy khách (Client).

Thông qua cổng TCP 23 nên các máy chủ (Server) sẽ biết để kết nối với Telnet. Máy khách hàng cần xác định rõ cổng Telnet bởi cổng này có thể thay đổi với nhiều lý do khác nhau hoặc vì chế độ bảo mật....

***

**Tính năng của Telnet**

Vì là giao thức đầu tiên được sử dụng khi internet ra mắt lần đầu nên có rất nhiều thiếu sót, bởi nó một giao thức đơn giản nên có rất ít tính năng. Để quản lý hệ thống từ xa nên các giao thức Telnet đưa ra một số tính năng như sau:

- Telnet đơn giản nhưng không dễ sử dụng
- Hiển thị thông tin kết nối nhưng khá chậm chạp và thô sơ
- Kết nối nhanh
- Giao thức Telnet không an toàn, không bảo mật cao.

***

**Bảo mật**

Vì là giao thức phổ biến trước đây nên Telnet được sử dụng ở nhiều loại thiết bị khác nhau để dễ dàng quản lý từ xa. Chẳng hạn các thiết bị như Linux, Router, Switch, camera, windows, ....

Vấn đề bảo mật của Telnet là bất cập lớn nhất của giao thức này. Chính vì nó không được mã hóa nên đã trở thành mục tiêu tấn công xen giữa. Vậy nên các thông tin lưu lượng của giao thức Telnet có thể bị lộ bất cứ lúc nào, và trong quá trình sử dụng thì Telnet cũng chỉ cung cấp xác thực dựa trên mật khẩu. Chính vì dựa trên mật khẩu nên có thể bị những kẻ tấn công đánh cắp và chúng kém an toàn so với các giao thức khác, hay dựa trên việc chứng thực bằng key
