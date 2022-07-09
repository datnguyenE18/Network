**Mô hình OSI và TCP/IP**

![OSI vs TCP](https://user-images.githubusercontent.com/43572616/178091608-ab2ce19b-70f4-4194-a8c4-064d4fe059ca.png)



- TCP/IP là viết tắt của Transmission Control Protocol / Internet Protocol và là một bộ các giao thức truyền thông được sử dụng để kết nối các thiết bị mạng với nhau trên internet.
 
- TCP/IP chỉ định cách dữ liệu được trao đổi qua internet bằng cách cung cấp các giao tiếp đầu cuối để xác định cách nó được chia thành các gói , định địa chỉ, truyền, định tuyến và nhận tại đích
 
- TCP/IP được sử dụng phổ biến và thực tế hơn OSI
 
- **Các thức hoạt động,** TCP/IP là sự kết hợp giữa 2 giao thức:
  - IP (Giao thức liên mạng) cho phép các gói tin được gửi đến đích đã định sẵn, bằng cách thêm các thông tin dẫn đường vào các gói tin để các gói tin được đến đúng đích đã định sẵn ban đầu
 
  - TCP (Giao thức truyền vận) đóng vai trò kiểm tra và đảm bảo sự an toàn cho mỗi gói tin khi đi qua mỗi trạm. Trong quá trình này, nếu giao thức TCP nhận thấy gói tin bị lỗi, một tín hiệu sẽ được truyền đi và yêu cầu hệ thống gửi lại một gói tin khác
 
  - Khi truyền dữ liệu , quá trình tiến hành từ tầng trên xuống tầng dưới, qua mỗi tầng dữ liệu được thêm vào thông tin điều khiển gọi là Header. Khi nhận dữ liệu thì quá trình xảy ra ngược lại, dữ liệu được truyền từ tầng dưới lên và qua mỗi tầng thì phần header tương ứng sẽ được lấy đi và khi đến tầng trên cùng thì dữ liệu không còn phần header nữa.



- **Tầng ứng dụng (Application):**
  - Cung cấp giao tiếp đến người dùng. Đảm nhận vai trò giao tiếp dữ liệu giữa 2 máy khác nhau thông qua các dịch vụ mạng khác nhau (duyệt web, chat, gửi email, một số giao thức trao đổi dữ liệu: SMTP, SSH, FTP,...).
 
  - Cung cấp các ứng dụng cho phép người dùng trao đổi dữ liệu ứng dụng thông qua các dịch vụ mạng khác nhau (như duyệt web, chat, gửi email,...).
 
  - Dữ liệu khi đến đây sẽ được định dạng theo kiểu byte nối byte, cùng với đó là các thông tin định tuyến giúp xác định đường đi đúng của một gói tin



- **Tầng giao vận (Transport):**
  - Xử lý vấn đề giao tiếp giữa các máy chủ trong cùng một mạng hoặc khác mạng được kết nối với nhau thông qua bộ định tuyến (Chịu trách nhiệm duy trì liên lạc đầu cuối trên toàn mạng)
 
  - Trong tầng này còn bao gồm 2 giao thức cốt lõi là TCP và UDP. Trong đó, TCP đảm bảo chất lượng gói tin nhưng tiêu tốn thời gian khá lâu để kiểm tra đầy đủ thông tin từ thứ tự dữ liệu cho đến việc kiểm soát vấn đề tắc nghẽn lưu lượng dữ liệu. Trái với điều đó, UDP cho thấy tốc độ truyền tải nhanh hơn nhưng lại không đảm bảo được chất lượng dữ liệu được gửi đi.
 
- **Tầng mạng (Internet):**
  - Xử lý quá trình truyền gói tin trên mạng. Chịu trách nhiệm truyền tải dữ liệu một cách logic trong mạng
 
  - *Định tuyến:* tìm tuyến đường qua các nút trung gian để gửi dữ liệu từ nguồn tới đích.
 
  - *Chuyển tiếp*: chuyển tiếp gói tin từ cổng nguồn tới cổng đích theo tuyến đường.
 
  - *Định địa chỉ* : định danh cho các nút mạng.
 
  - *Đóng gói dữ liệu*: nhận dữ liệu từ giao thức ở trên, chèn thêm phần Header chứa thông tin của tầng mạng và tiếp tục được chuyển đến tầng tiếp theo.
 
  - *Đảm bảo chất lượng dịch vụ(QoS)*: đảm bảo các thông số phù hợp của đường truyền theo từng dịch vụ.
 
  - Các giao thức của tầng này bao gồm: IP (Internet Protocol - giao thức được sử dụng rộng rãi trong mọi hệ thống mạng trên phạm vi toàn thế giới), ICMP (Internet Control Message Protocol), IGMP (Internet Group Message Protocol).



- **Tầng Vật lý (Physical):**
  - Chịu trách nhiệm truyền dữ liệu giữa hai thiết bị trong cùng một mạng. Các gói dữ liệu được đóng vào khung (gọi là Frame) và được định tuyến đi đến đích đã được chỉ định ban đầu
