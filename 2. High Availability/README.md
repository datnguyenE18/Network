# High Availability


- **High Availability (HA)** là một giải pháp/quy trình/công nghệ để đảm bảo ứng dụng/cơ sở dữ liệu có thể truy cập được 24/7 trong bất kì điều kiện nào, dù là có dự định trước hay bất ngờ. Nghĩa là là server hoặc thiết bị luôn trong trạng thái sẵn sàng phục vụ, giảm thiểu tình trạng gián đoạn của hệ thống
 
- HA là một lý thuyết chứ không phải là một công nghệ cụ thể, được đo bằng % uptime của dịch vụ đó trong khoảng thời gian, ví dụ HA=99.999%/1 năm. Để nâng cao %HA người ta phải kết hợp nhiều công nghệ đồng thời.
 
- Để ứng dụng và cơ sở dữ liệu có khả năng truy cập 24/7 ở mọi hoàn cảnh thì High availability cần tối thiểu 2 server chạy song song, hoạt động liên tục. Nếu một trong 2 server gặp sự cố, server còn lại sẽ thay thế để đảm bảo cho hệ thống có thể hoạt động bình thường.

***
- **High Availability vs Load Balancing:**
  - Cân bằng tải (Load Balancing): Các node bên hoạt động song song, chia sẻ các tác vụ để năng cao hiệu năng
 
  - Tính sẵn sàng cao (High availability): Các tài nguyên luôn sẵn sàng xử lý yêu cầu, ngay cả khi có vấn đề xảy ra với các thành phần bên trong (hardware, software)

***

**Lợi ích của High availability:**
  - Tất cả dữ liệu trong High availability đều được bảo mật, đảm bảo an toàn

![1_lXik7zGdIEYql3GvZ2gkgg](https://user-images.githubusercontent.com/43572616/177666520-40832c47-d0b2-469b-9143-8925adfd39f3.png)



- Dữ liệu trong server được lưu ở các vị trí khác nhau
- Tất cả dữ liệu đều được bảo mật, đảm bảo an toàn
- Nếu VPS xảy ra sự cố, dữ liệu sẽ không bị ảnh hưởng
- Người dùng có thể truy cập dễ dàng vào website, truy cập mọi lúc mọi nơi mà không lo bị gián đoạn
- Các bản sao VPS được lưu trữ tại nhiều cụm khác nhau. Nếu sự cố xảy ra tại 1 VPS thì VPS
