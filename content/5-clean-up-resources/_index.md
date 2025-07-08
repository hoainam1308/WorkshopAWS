---
title : "Dọn dẹp tài nguyên"
date : "`r Sys.Date()`"
weight : 5
chapter : false
pre : " <b> 5. </b> "
---

#### Empty bucket
1. Đi đến AWS S3
2. Trong danh sách **Bucket**, hãy chọn **Bucket** liên quan
3. Chọn **Empty**
4. Trong trang **Empty bucket**, hãy xác nhận và chọn **Empty**

#### Delete S3 Bucket
1. Đến AWS S3
2. Chọn **S3 bucket** liên quan
3. Chọn **Delete** sau đó xác nhận và chọn **Delete bucket**

#### Delete DocumentDB Cluster
1. Đến AWS DocumentDB
2. Trong danh sách **Cluster**, hãy chọn **Cluster** liên quan
3. (Optional) Nếu bạn chưa tắt **deletion protection** thì chọn **Acions** -> **Modify** sau đó bỏ chọn **Enable deletion protection** rôi chọn **Continue** -> **Modify cluster**
4. Chọn **Actions** -> **Delete**
5. Xác nhận và chọn **Delete**

#### Terminate EC2 Instance
1. Thoát SSH EC2
2. Vào Amazon EC2 console.
3. Trong thanh điều hướng bên trái, chọn **Instances**
4. Chọn **EC2 instances** liên quan
5. Chọn **Instance state**
6. Chọn **Terminate instance**
7. Xác nhận **Termination**

#### Delete Subnet group
{{% notice note %}}
Lưu ý, bạn phải đợi xoá xong DocumentDB Cluster mới có thể xoá Subnet group
{{% /notice %}}
1. Đến AWS DocumentDB
2. Trong thanh điều hướng bên trái, chọn **Subnet groups**
3. Chọn **Subnet groups** liên quan
4. Chọn **Actions** -> **Delete**
5. Xác nhận **Delete**

#### Delete Security groups
1. Đến AWS VPC
2. Trong thanh điều hướng bên trái, chọn **Security groups**
3. Trong danh sách **Security groups**, hãy chọn **tất cả** **Security groups** liên quan
4. Chọn **Actions** -> **Delete Security groups**
5. Xác nhận **Delete**

#### Delete VPC
1. Đến AWS VPC
2. Trong thanh điều hướng bên trái, chọn **Your VPCs**
3. Trong danh sách **VPCs**, hãy chọn **VPC** liên quan
4. Chọn **Actions** -> **Delete VPC**
5. Xác nhận **Delete**
