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
    - Xử lý các giao thức cấp cao, các vấn đề về trình diễn, số hóa (encoding), kiểm soát dialog.  
    - TCP/IP gộp tất cả các vấn đề liên quan đến ứng dụng vào 1 lớp/tầng, và đảm bảo các dữ liệu này được đóng góp hoàn toàn ở lớp/tầng tiếp theo.  
    - FTP, HTTP, DNS, SMNP, …  
    - Định dạng dữ liệu, cấu trúc dữ liệu, encode…  
    - Kiểm soát dialog, quản trị phiên…  
