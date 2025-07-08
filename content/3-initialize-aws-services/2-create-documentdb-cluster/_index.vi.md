---
title : "Tạo DocumentDB"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 3.2 </b> "
---

#### Tạo DocumentDB

1. Mở Amazon DocumentDB console tại https://console.aws.amazon.com/docdb

2. Tại danh sách **Clusters** chọn **Create**

![Tạo DocumentDB Cluster](/images/3/0034.png?featherlight=false&width=90pc)

3. Chọn **Instance-based cluster**

4. Tại **Number of regular replica instances** nhập số lượng bản sau

![Tạo DocumentDB Cluster](/images/3/0035.png?featherlight=false&width=90pc)

5. Ở phần **Authentication**:
   - Nhập Username ví dụ: ```workshopdb```
   - Chọn **Self managed**
   - Nhập **Password** và **Confirm**

![Tạo DocumentDB Cluster](/images/3/0038.png?featherlight=false&width=90pc)

6. Chọn show **advanced settings**, trong phần **Network settings**:
   - Chọn **VPC** đã tạo
   - Chọn **subnet group** đã tạo
   {{% notice tip %}}
   Nếu bạn không thấy VPC, hãy reload lại trang web
   {{% /notice %}}

![Tạo DocumentDB Cluster](/images/3/0037.png?featherlight=false&width=90pc)

7. Quay lại **Connectivity** ở trên chọn **Connect to an EC2 compute resource** và chọn **EC2** đã tạo

![Tạo DocumentDB Cluster](/images/3/0039.png?featherlight=false&width=90pc)

8. (Option) Uncheck Enable delection protection để sau này dễ dọn dẹp resouces

9. Chọn **Create cluster** để tạo

![Tạo DocumentDB Cluster](/images/3/0040.png?featherlight=false&width=90pc)