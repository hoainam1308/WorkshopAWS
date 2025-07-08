---
title : "Tạo EC2 Instance"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 3.1 </b> "
---

**ℹ️ Thông tin:** Amazon EC2 (Elastic Compute Cloud) cung cấp năng lực điện toán có thể mở rộng trên AWS Cloud, loại bỏ nhu cầu đầu tư vào phần cứng ngay từ đầu.

Để tạo phiên bản Linux EC2 bằng AWS Management Console, hãy làm theo các hướng dẫn sau. Hướng dẫn này giúp bạn nhanh chóng khởi chạy phiên bản đầu tiên của mình với các cấu hình cần thiết

#### Tạo EC2 Instance

1. Mở trình duyệt web và điều hướng đến bảng điều khiển Amazon EC2 tại https://console.aws.amazon.com/ec2/.

![Tạo EC2](/images/3/0024.png?featherlight=false&width=90pc)

2. Trong thanh điều hướng bên trái, ở phần **Instances** chọn **Instances**, sau đó ấn **Launch instances**.

3. Nhập tên ví dụ: ```workshop-ec2```

4. Trong phần **Application and OS Images**:
   - Chọn **Amazon Linux**
   - Trong **Amazon Machine Image (AMI)** chọn **Amazon Linux 2 AMI**

![Tạo EC2](/images/3/0025.png?featherlight=false&width=90pc)

5. Chọn **t2.micro** trong **Instance type**

![Tạo EC2](/images/3/0026.png?featherlight=false&width=90pc)

6. Trong phần **Key pair** chọn **Create new key pair**
   - Nhập tên key pair ví dụ: ```my-workshop-keypair```
   - Tại Key pair type chọn **.RSA**
   - Private key file format chọn **.pem**
   - Chọn **Create key pair** và lưu key pair vào nơi thích hợp

![Tạo EC2](/images/3/0027.png?featherlight=false&width=90pc)

7. Trong phần **Network settings** chọn **Edit**
   - Chọn **VPC đã tạo**
   - Chọn **public subnet** đã **enable Auto-assign public IP**
   - Chọn **Select existing security group**
   - Chọn security group đã tạo cho ec2 **workshop-ec2-sg**

![Tạo EC2](/images/3/0028.png?featherlight=false&width=90pc)

![Tạo EC2](/images/3/0029.png?featherlight=false&width=90pc)

8. Kiểm tra lại trong **Summary** và chọn **Launch instance**

![Tạo EC2](/images/3/0031.png?featherlight=false&width=90pc)

![Tạo EC2](/images/3/0022.png?featherlight=false&width=90pc)