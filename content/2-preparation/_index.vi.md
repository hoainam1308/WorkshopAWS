---
title : "Chuẩn bị"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 2. </b> "
---

## Tổng quan
***ℹ️ Những gì cần chuẩn bị***  
Trong workshop, bạn sẽ xây dựng một môi trường Amazon VPC hoàn chỉnh theo các biện pháp thực hành tốt nhất của AWS về kiến ​​trúc mạng và bảo mật. Bạn sẽ tạo tất cả các thành phần thiết yếu cần thiết cho việc triển khai VPC sẵn sàng cho production.

Ngoài ra các bạn nên để source code của mình trên github để dễ dàng tải xuống.  
[Backend nodejs](https://github.com/hoainam1308/DeployedBEAWS.git)  
[Frontend reacjs](https://github.com/hoainam1308/DeployedFEAWS.git)

Kiến trúc chúng tôi sẽ triển khai được minh họa trong sơ đồ bên dưới:


![Diagram](/images/2/diagram.png?featherlight=false&width=90pc)

#### Các bước chuẩn bị

Ở phần này chúng ta sẽ Tạo VPC và các dịch vụ liên quan

1. [Tạo VPC](2-preparation/1-create-vpc)
2. [Tạo Security Group](2-preparation/2-create-security-group)
3. [Tạo Subnet Group](2-preparation/3-create-subnet-group)