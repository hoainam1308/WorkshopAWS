---
title : "Tạo Security Group"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---

#### Tạo Security Group cho EC2

**ℹ️ Thông tin:** Security groups hoạt động như các tường lửa ảo cho các Amazon EC2 instances, giúp kiểm soát lưu lượng inbound (vào) và outbound (ra).
Đối với triển khai DocumentDB, chúng ta cần tạo một security group cho các EC2 instances sẽ kết nối đến cơ sở dữ liệu của chúng ta.

Thực hiện theo các bước sau để tạo Security Group với các cổng cần thiết:

1. Mở Amazon VPC console tại https://console.aws.amazon.com/vpc/.

2. Trong thanh điều hướng VPC, trong phần **Security**, chọn **Security groups**.

3. Chọn **Create security group**.

![Tạo Security group](/images/2/0004.png?featherlight=false&width=90pc)

4. Trong phần Basic details
   - Nhập tên security goup ví dụ: ```workshop-ec2-sg```
   - Nhập mô tả 
   - Trong phần VPC, chọn vpc vừa tạo trước đó

5. Trong phần **Inbound rules**, **Add rule** để cấu hình quyền truy cập
   - Type: **SSH**, Source: **My IP**
   - Type: **HTTP**, Source: **Anywhere**
   - Type: **HTTPS**, Source: **Anywhere**
   - Type: **Custom TCP**, Port range: **3000**, Source: **Anywhere**

   {{% notice note %}}
   Đối với môi trường production, hãy hạn chế địa chỉ IP nguồn để truy cập SSH chỉ ở các dải IP đáng tin cậy thay vì cho phép truy cập từ bất kỳ đâu (0.0.0.0/0).
   {{% /notice %}}

![Tạo Security group](/images/2/0005.png?featherlight=false&width=90pc)

6. Xem lại cài đặt của bạn và nhấp vào **Create security group**.

![Tạo Security group](/images/2/0006.png?featherlight=false&width=90pc)

7. Sau khi tạo, security group mới sẽ xuất hiện trong danh sách. Lưu ý ID vì bạn sẽ cần nó khi khởi chạy phiên bản EC2.

![Tạo Security group](/images/2/0007.png?featherlight=false&width=90pc)


#### Tạo Security Group cho DocumentDB

Thực hiện theo các bước sau để tạo Security Group cho DocumentDB với các cổng cần thiết:

1. Tại danh sách **Security Groups**, chọn **Create security group**.
![Tạo Security group](/images/2/0008.png?featherlight=false&width=90pc)

2. Trong phần **Basic details**
   - Nhập tên security goup ví dụ: ```workshop-documentdb-sg```
   - Nhập mô tả 
   - Trong phần **VPC**, chọn vpc vừa tạo trước đó

3. Trong phần **Inbound rules**, ấn Add rule để cấu hình quyền truy cập
   - Type: **Custom TCP**, Port range: **27017**, Source: **Custom** và chọn **workshop-ec2-sg**

![Tạo Security group](/images/2/0009.png?featherlight=false&width=90pc)

4. Xem lại cài đặt của bạn và nhấp vào **Create security group**.

![Tạo Security group](/images/2/0010.png?featherlight=false&width=90pc)

![Tạo Security group](/images/2/0011.png?featherlight=false&width=90pc)

![Tạo Security group](/images/2/0012.png?featherlight=false&width=90pc)
