# [LB] Load Balancing

- **Load Balancing** (cân bằng tải) là một kỹ thuật bảo đảm máy chủ không bị quá tải bởi lượng truy cập. Với các biện pháp cân bằng tải, khối lượng công việc, truy cập của người dùng được phân chia đều trên các máy chủ. Việc này cung cấp khả năng chịu lỗi cao, đảm bảo tính sẵn sàng phục vụ của hệ thống.

- **Load Balancer** (phần cứng hoặc phần mềm load balancing)**:** là một bộ phận có công việc phân bố đồng đều lưu lượng truy cập giữa hai hay nhiều các máy chủ có cùng chức năng trong cùng một hệ thống. Bằng cách đó, sẽ giúp cho hệ thống giảm thiểu tối đa tình trạng của máy chủ, thậm chí là datacenter
 
- Khi hệ thống có quá nhiều người sử dụng, một server đơn lẻ không đáp ứng được lượng requests khổng lồ được gửi đến cùng lúc. Cần chia sẻ công việc của server hiện tại với các server khác nữa. Khi này, việc tải dữ liệu từ server nào sẽ do bộ cân bằng tải quyết định

![20210826142332791r_7 png](https://user-images.githubusercontent.com/43572616/177664115-48d75793-8d28-4911-8fdf-407511202100.jpg)
***
- **Cách thức hoạt động của Load Balancing:**
  - **Website tiếp nhận lượng truy cập:** website của sẽ nhận một lượng lớn yêu cầu từ client. Các yêu cầu này có thể cùng một lúc đi đến máy chủ thông qua internet.
  - **Phân phối lưu lượng truy cập lên các server:** Sau khi tiếp nhận, load balancer xử lý từng yêu cầu, sau đó điều hướng đến các máy chủ thích hợp.
 
  - **Server tiếp nhận và xử lý yêu cầu:** Sau khi nhận yêu cầu, server có thể tiếp nhận yêu cầu hoặc gửi phản hồi lại với load balancer trong trường hợp không thể tiếp nhận thêm yêu cầu để tránh sự quá tải ở các nút.
 
  - **Server gửi phản hồi cho client**
 ***
- **Session Persistence:**
  - Ví dụ khi mua hàng onl, các sản phẩm trong giỏ hàng của người dùng có thể được lưu trữ ở cấp trình duyệt cho đến khi người dùng sẵn sàng mua chúng

    Việc thay đổi server ở giữa phiên mua sắm có thể gây ra các vấn đề về hiệu suất hoặc gây lỗi giao dịch.

    Như vậy khi đó quan trọng là tất cả các request từ một khách hàng phải được gửi đến cùng một server trong suốt thời gian của phiên. Điều này được gọi là Session Persistence
 
  - Các cân bằng tải tốt nhất có thể xử lý Session Persistence khi cần thiết.
 ***
- **Load Balancer dựa trên phần cứng và phần mềm:**
  - Việc cân bằng tải có thể được thực hiện ở cả phần cứng lẫn phần mềm
    - **Dựa trên phần cứng:** một phần cứng (hoặc phần cứng ảo) một loại thiết bị hoạt động như một Proxy ngược để phân phối lưu lượng mạng hoặc ứng dụng trên các máy chủ khác nhau.
 
    - **Dựa trên phần mềm:** đề cập đến việc sử dụng phần mềm để phân phối và cân bằng lượng người dùng. Được chia thành giao thức 7 Layer và giao thức 4 Layer. Nổi tiếng nhất là Nginx



- So sánh:

| |**Phần cứng**|**Phần mềm**|
| :-: | :-: | :-: |
|**Hiệu năng**|Cao hơn|Thấp hơn|
|**Tính linh hoạt**|Kém linh hoạt|Linh hoạt hơn|
|**Khả năng ảo hóa**|Tích hợp sẵn|Không tích hợp sẵn|
|**Kiến trúc**|Nhiều dung lượng vật lý|Dung lượng vật lý thấp|
|**Giá thành**|Cao, đặc biệt là chi phí bảo trì|Tương đối thấp|
|**Khả năng cấu hình**|Thấp|Cao|
***
- **Khi nào sử dụng LB:**
  - Được sử dụng khi service được triển khai trên nhiều hơn một server
***
**Phân loại cân bẳng tải:**

  Có nhiều cách cấu hình cân bằng tải, tùy thuộc vào các tính năng đặc thù

 - **Server Load Balancing:**

Mục tiêu là phân chia khối lượng công việc ra nhiều máy chủ dựa theo năng lực và tính khả dụng của chúng. Server Load Balancing dựa vào các thông tin ở tầng Application để điều hướng truy cập. Server Load Balancing còn được biết đến như Layer 7 Load Balancing.

 
 - **Network Load Balancing:**

Phân chia lưu lượng truy cập giữa các địa chỉ IP, switches, routers sử dụng thiết bị một cách hiệu quả và nâng cao tính ổn định

Các cấu hình này sẽ được thực hiện ở tầng Transport, do đó, Network Load Balancing còn được gọi với tên Layer 4 Load Balancing.


  - **Global Server Load Balancing (GSLB):**

Trong Global Server Load Balancing, một trung tâm điều hành sẽ xử lý việc cân bằng tải giữa khắp nơi trên toàn thế giới thông qua một loạt những thiết bị câng bằng tải Layer 4 và Layer 7

Trong việc triển khai GSLB, thường sẽ có các thiết bị ADC ở cấp độ toàn cầu lẫn cục bộ, nơi lưu lượng truy cập được phân phối đến.


  - **Container Load Balancing:** 

Container Load Balancing cung cấp các phiên bản ảo hóa, riêng biệt. Phổ biến nhất hiện nay là hệ thống Kubernetes orchestration, hệ thống này có thể phân chia load giữa các container pods với nhau để giúp nâng cao tính sẵn sàng.


  - **Cloud Load Balancing:**

Trong hạ tầng Cloud, có tương đối nhiều lựa chọn cho việc cân bằng tải. Cloud Load Balancing bao gồm cả Network Load Balancing (Layer-4) và Application Load Balancing (Layer-7)
***
**Không có cân bằng tải (No Load Balancing):**
 - Đây là dạng cơ bản nhất cho một ứng dụng web, thường được sử dụng trong môi trường số lượng người dùng ít hoặc không có để test, dev.

![khong-can-bang-tai](https://user-images.githubusercontent.com/43572616/177665651-44bbf0bf-f044-4ca3-b5e5-6caf1688231c.png)
 - Với mô hình này, người dùng sẽ kết nối trực tiếp với web server tại (yourdoamain.com) mà không sử dụng cân bằng tải. Nếu web server gặp sự cố, trục trặc thì người dùng sẽ không kết nối được đến ứng dụng web.

***
**Cân bằng tải tại tầng 4 (Layer 4 Load Balancing)**
  - Việc sử dụng cân bằng tải ở tầng 4 (Layer 4 Load Balancing) để có thể cân bằng tải tới nhiều server. Thì các request sẽ được điều hướng dựa trên địa chỉ IP và port. Ví dụ có một request đến example.com/something sẽ được điều hướng tới backend được dùng để điều hướng cho doamin example.com với port 80.

![can-bang-tai-layer-4](https://user-images.githubusercontent.com/43572616/177665809-c1bc7a91-c2d2-456e-9788-763d0510154a.png)

***
**Cân bằng tải tại tầng 7 (Layer 7 Load Balancing)**
  - Đây là cân bằng tải phức tạp nhất nhưng có nhiều tùy biến. Với việc sử dụng cân bằng tải tại tầng 7, có thể điều hướng các request dựa trên thông tin và nội dung của request đó. Cân bằng tải tầng 7 với nhiều backend có thể dùng một domain và port.

![photo-1-1531359506259816355323](https://user-images.githubusercontent.com/43572616/177665864-16929487-28a7-4048-b401-14f3b6912c4e.png)


- Ví dụ, có một request gửi tới example.com/something, request đó sẽ được điều hướng đến backend chuyên dụng cho something.

***
- **Các thuật toán cân bằng tải:**
  - **Round robin (roundrobin):** 
    - Là thuật toán điều phối vòng tròn, các máy chủ sẽ được xem ngang hàng và sắp xếp theo một vòng quay. Các truy vấn dịch vụ sẽ lần lượt được gửi tới các máy chủ theo thứ tự sắp xếp
 
    - roundrobin là thuật toán được sử dụng mặc định load balancing khi không có thuật toán nào được chỉ định

|backend web-backend<br>`    `option httplog<br>`    `option forwardfor<br>`    `server web1 192.168.1.110:8080 check<br>`    `server web2 192.168.1.111:8080 check<br>`    `server web3 192.168.1.112:8080 check|
| :- |


Dựa vào khả năng xử lý của từng server, chúng ta sẽ thay đổi giá trị trọng số của từng server để phân phối tải đến các server khác nhau. Sử dụng tham số “weight” để thay đổi trọng số. Tỷ lệ tải của các server sẽ tỷ lệ thuận trọng số của chúng so với tổng trọng số của tất cả server. Vì vậy mà server nào có trọng số càng cao, thì yêu cầu tải lên nó cũng sẽ cao. Ví dụ cân bằng tải khi thiết lập weight:



|backend web-backend<br>`    `balance  roundrobin<br>`    `option httplog<br>`    `option forwardfor<br>`    `server web1 192.168.1.110:8080 check weight 2<br>`    `server web2 192.168.1.111:8080 check weight 2<br>`    `server web3 192.168.1.112:8080 check weight 1|
| :- |


Khi đó mỗi 05 request, 2 request đầu tiên sẽ được chuyển tiếp lần lượt đến server web1 và web2, 3 request sau sẽ thực hiện chuyển tiếp lần lượt đến server web1, web2 và web3

Mặc định weight có giá trị là 1, giá trị tối đa của weight là 256. Nếu server giá trị weight là 0, khi đó nó sẽ không tham gia vào cụm server trong load balancing.

---
- **Least connections (leastconn):** 
  - Các requests sẽ được chuyển vào server có ít kết nối nhất trong hệ thống. Thuật toán này được coi như thuật toán động, vì nó phải đếm số kết nối đang hoạt động của server.
 
  - Nó sẽ tự động lựa chọn server với số lượng kết nối đang hoạt động là nhỏ nhất, để lượng connection giữa các server là tương đương nhau.
 
  - Thuật toán này khắc phục được tình trạng một số server có lượng connection rất lớn (do duy trì trạng thái connection), trong khi một số server khác thì lượng tải hay connection thấp

|backend web-backend<br>`      `leastconn<br>`    `option httplog<br>`    `option forwardfor<br>`    `server web1 192.168.1.110:8080 check<br>`    `server web2 192.168.1.111:8080 check<br>`    `server web3 192.168.1.112:8080 check|
| :- |


Thuật toán này hoạt động tốt khi mà hiệu suất và khả năng tải của các server là tương đương nhau.

---

- **IP Hash (source):** Thuật toán xác định kết nối chính xác từ một IP của máy khách sẽ được kết nối trực tiếp đến một server backend

---
- **Least response time:**  Đây là thuật toán dựa trên tính toán thời gian đáp ứng của mỗi server (response time), thuật toán này sẽ chọn server nào có thời gian đáp ứng nhanh nhất. Thời gian đáp ứng được xác định bởi khoảng thời gian giữa thời điểm gửi một gói tin đến server và thời điểm nhận được gói tin trả lời.
