# **Subnet mask**

- Thường thì mỗi tổ chức, công ty hay quốc gia đựơc InterNIC cấp cho một số địa chỉ IP nhất định và nó có các máy tính đặt ở các vùng khác nhau. Cách tốt nhất để quản lý là chia ra thành các mạng nhỏ và kết nối với nhau bởi router. Những mạng nhỏ như thế gọi là Subnets. Khi chia ra thành các Subnet nhằm:
  - Giảm giao dịch trên mạng: lúc này router sẽ kiểm soát các gói tin trên mạng – chỉ có gói tin nào có địa chỉ đích ở ngoài mới được chuyển ra
  - Quản lý đơn giản hơn và nếu có sự cố thì cũng dễ kiểm tra và xác định đựơc nguyên nhân gây lỗi hơn là trong một mạng lớn



![image](https://user-images.githubusercontent.com/43572616/177848833-d0280cca-19ba-4cc4-8ffb-672b37b6968e.png)



- Mỗi máy tính trong một mạng cụ thể nào đó thì phải có cùng một địa chỉ mạng => địa chỉ mạng không thể thay đổi được => chỉ còn cách lấy một phần địa chỉ Node Address để làm định danh cho mỗi Subnet

![image](https://user-images.githubusercontent.com/43572616/177848914-401ccd52-9a4a-4887-973e-0b9700e42a15.png)



- Không phải là tất cả các mạng đều cần có Subnet và vì thế không cần sử dụng Subnet – Trong trường hợp này sử dụng Subnet mask mặc định:
  - Lớp A Subnet mask là 255.0.0.0
  - Lớp B Subnet mask là 255.255.0.0
  - Lớp C Subnet mask là 255.255.255.0
