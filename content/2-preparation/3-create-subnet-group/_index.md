---
title : "Tạo Subnet Group"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 2.3 </b> "
---

#### Tạo Subnet Group cho DocumentDB
1. Mở Amazon DocumentDB console tại https://console.aws.amazon.com/docdb/

2. Trong thanh điều hướng bên trái, chọn **Subnet groups** sau đó ấn **Create**.

![Tạo Subnet group](/images/2/0014.png?featherlight=false&width=90pc)

3. Trong phần **Subnet group detail**:
    - Nhập name ví dụ: ```workshop-documentdb-subnet-group```
    - Nhập mô tả

4. Trong phần **Add subnets**:
    - Chọn **vpc** đã tạo
    - Chọn lần lượt **hai Availability zone** có subnet 
    - Mỗi AZ chọn **một private subnet**
    - **Add subnet**

![Tạo Subnet group](/images/2/0019.png?featherlight=false&width=90pc)

![Tạo Subnet group](/images/2/0020.png?featherlight=false&width=90pc)

5. Kiểm tra lại thông tin các subnet

6. Ấn **Create** để tạo subnet group

![Tạo Subnet group](/images/2/0021.png?featherlight=false&width=90pc)

![Tạo Subnet group](/images/2/0022.png?featherlight=false&width=90pc)