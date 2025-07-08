---
title : "Tạo VPC"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---

#### Tạo VPC với các Subnets và các tài nguyên liên quan

**ℹ️ Thông tin:** Amazon Virtual Private Cloud (Amazon VPC) cho phép bạn khởi chạy tài nguyên AWS vào mạng ảo mà bạn đã xác định. Mạng ảo này rất giống với mạng truyền thống trong trung tâm dữ liệu của riêng bạn, với lợi ích là sử dụng cơ sở hạ tầng có thể mở rộng của AWS.  

Thực hiện theo các bước sau để tạo VPC với tất cả các thành phần cần thiết cho việc triển khai website của bạn:

1. Mở Amazon VPC console tại https://console.aws.amazon.com/vpc/.

2. Trên VPC dashboard, chọn **Create VPC**.

![Tạo VPC](/images/2/0001.png?featherlight=false&width=90pc)

3. Để tạo Resource, chọn **VPC and more** để tạo môi trường VPC hoàn chỉnh.

![Tạo VPC](/images/2/0002.png?featherlight=false&width=90pc)

4. Cấu hình tùy chọn **Auto-generate** thẻ Name theo sở thích của bạn. Tùy chọn này cho phép AWS tự động tạo tên nhất quán cho tất cả tài nguyên VPC.

5. Nhập một dải địa chỉ IPv4 CIDR cho VPC của bạn (ví dụ: 10.0.0.0/16). Dải địa chỉ này xác định phạm vi IP có sẵn trong VPC.

6. (Tùy chọn) Để bật hỗ trợ IPv6, chọn IPv6 CIDR block và chọn một dải IPv6 được Amazon cung cấp.

7. Đối với Number of Availability Zones (AZs), chọn ít nhất hai AZs để đảm bảo tính sẵn sàng cao.

8. Chọn ít nhất hai private subnets để tạo subnet group cho DocumentDB.

9. Xem lại phần Preview để xem sơ đồ trực quan về kiến trúc VPC bạn đã cấu hình.

10. Chọn **Create VPC** để khởi tạo tất cả các tài nguyên đã cấu hình.

![Tạo VPC](/images/2/0003.png?featherlight=false&width=90pc)

11. Cấu hình cho public subnet:
    - Trong VPC console chọn **public subnet**
    - Chọn **Actions** -> **Edit subnet settings**
    - Check vào **Enable auto-assign public IPv4 address**

![Tạo VPC](/images/2/0017.png?featherlight=false&width=90pc)
