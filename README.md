# TÌM HIỂU MÔ HÌNH TCP/IP  
Tên: Hallen_Trần    
Ngày cập nhật: 25/04/2017   

### 1. TCP/IP là gì ?  
**Mô hình TCP/IP (Transmission Control Protocol/Internet Protocol Model) là 1 tập các giao thức và quy tắc được phát triển để cho phép các máy tính liên kết với nhau, chia sẻ tài nguyên thông qua 1 hệ thống mạng.**  
![img](http://2.bp.blogspot.com/-jH4TzAOcspU/UzQeMUZ1JlI/AAAAAAAAADA/cWNGZjCtkI4/s1600/TCP-IP-Model.png)  
**Trong mô hình phân lớp:**  
- *Lớp 1 truy cập mạng (Network Access Layer):*  
    - Bao gồm tất cả các vấn đề mà 1 gói tin IP yêu cầu để tạo kết nối vật lý. Gồm tất cả đặc điểm của lớp/tầng vật lý và liên kết dữ liệu của mô hình OSI.  
        - Đặc điểm kỹ thuật điện, cơ.  
        - Tốc độ dữ liệu, khoảng cách, đầu nối vật lý (connector).  
        - Các khung (frame), địa chỉ vật lý.  
        - Việc đồng bộ hóa, kiểm soát luồng, kiểm soát lỗi.  
- *Lớp 2 liên mạng (Internet Layer):*  
    - Gửi các gói tin nguồn từ bất kỳ mạng nào, có những tuyến đường và mạng độc lập để đưa gói tin tới đích.  
        - Gói tin, địa chỉ logic.  
        - Giao thức liên mạng (Internet Protocol – IP).  
        - Tuyến đường (route), bảng định tuyến (routing table), giao thức định tuyến (routing protocol).  
- *Lớp 3 vận chuyển (Transport Layer):*  
    - Xử lý về chất lượng dịch vụ, các vấn đề độ tin cậy, kiểm soát luồng, sửa lỗi.  
        - Phân đoạn, dòng dữ liệu, lưu lượng.  
        - Kết nối có định hướng và không định hướng.  
        - Kiểm soát lường đầu cuối.  
        - Phát hiện lỗi và phục hồi.    
- *Lớp 4 ứng dụng (Application Layer):*  
    - Xử lý các giao thức cấp cao, các vấn đề về trình diễn, số hóa (encoding), kiểm soát dialog .TCP/IP gộp tất cả các vấn đề liên quan đến ứng dụng vào 1 lớp/tầng, và đảm bảo các dữ liệu này được đóng góp hoàn toàn ở lớp/tầng tiếp theo.  
        - FTP, HTTP, DNS, SMNP, …  
        - Định dạng dữ liệu, cấu trúc dữ liệu, encode…  
        - Kiểm soát dialog, quản trị phiên…  
![img](https://kimnguyen.info/kim/wp-content/uploads/2014/09/Chap-2-TCP-IP-Protocol-300x251.jpg)  
![img](https://image.slidesharecdn.com/ositcp-ip-120727232444-phpapp02/95/osi-tcp-ip-14-728.jpg?cb=1343431818)   

### 2.Phương thức hoạt động của bộ giao thức TCP/IP ?  
**Quá trình đóng mở gói dữ liệu trong TCP/IP**  
![img](http://www.vnpro.vn/wp-content/uploads/2015/11/Qu%C3%A1-tr%C3%ACnh-%C4%91%C3%B3ng-m%E1%BB%9F-g%C3%B3i-d%E1%BB%AF-li%E1%BB%87u-trong-TCP-IP.jpg)  
- Cũng tương tự như trong mô hình OSI, khi truyền dữ liệu , quá trình tiến hành từ tầng trên xuống tầng dưới, qua mỗi tầng dữ liệu được them vào thông tin điều khiển gọi là Header. Khi nhận dữ liệu thì quá trình xảy ra ngược lại. dữ liệu được truyền từ tấng dưới lên và qua mỗi tầng thì phần header tương ứng sẽ được lấy đi và khi đến tầng trên cùng thì dữ liệu không còn phần header nữa.    
**Cấu trúc dữ liệu trong TCP/IP**  
![img](http://www.vnpro.vn/wp-content/uploads/2015/11/C%E1%BA%A5u-tr%C3%BAc-d%E1%BB%AF-li%E1%BB%87u-trong-TCP-IP.jpg)  

Hình trên cho ta thấy lược đồ dữ liệu qua các tầng.. Trong hình ta thấy tại các tầng khác nhau dữ liệu được mang những thuật ngữ khác nhau  
    - Trong tầng ứng dụng: dữ liệu là các luồng được gọi là stream.  
    - Trong tầng giao vận: đơn vị dữ liệu mà TCP gửi xuống gọi là TCP segment.  
    - Trong tầng mạng, dữ liệu mà IP gửi xuống tầng dưới gọi là IP Datagram  
    - Trong tầng liên kết, dữ liệu được truyền đi gọi là frame.  


### 3.So sánh OSI với TCP/IP?  
![img](https://hsto.org/getpro/habr/comment_images/219/06c/99d/21906c99d593e1cbcef7d235df6b69e8.png)  
![img](http://www.vnpro.vn/wp-content/uploads/2015/11/sp-sanh.jpg)  
- **Giống nhau:**  
    - *Cả hai đều có kiến trúc phân lớp.  
    - Đều có **lớp Application**, mặc dù các dịch vụ ở mỗi lớp khác nhau.
    - Đều có các **lớp Transport** và **Network**.  
    - Sử dụng kĩ thuật chuyển packet **(packet-switched)**.
    - Các nhà quản trị mạng chuyên nghiệp cần phải biết rõ hai mô hình trên.  
- **Khác nhau:**   
    - Mô hình TCP/IP kết hợp **lớp Presentation** và **lớp Session** vào trong **lớp Application**.
    - Mô hình TCP/IP kết hợp **lớp DataLink** và **lớp Physical** vào trong một lớp.  
    - Mô hình TCP/IP đơn giản hơn bởi vì có ít lớp hơn.  
    - Nghi thức TCP/IP được chuẩn hóa và được sử dụng phổ biến trên toàn thế giới.*   
    
### 4.Nên sử dụng mô hình nào hơn?  
- **Mô hình TCP/IP thông dụng hơn.Đa phân sử dụng các giao thức của TCP/IP nhưng lại tham chiếu bằng OSI.


