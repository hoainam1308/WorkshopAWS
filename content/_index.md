---
title : "Starting deploy web to AWS"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
---

# Starting deploy web to AWS

#### Dự Án Website Bán Hàng
Dự án website bán hàng được xây dựng với backend Node.js, cơ sở dữ liệu MongoDB và frontend React. Hệ thống hỗ trợ các tính năng cơ bản như: đăng ký, đăng nhập, thêm sản phẩm vào giỏ hàng, thanh toán và xem danh sách đơn hàng đã đặt. Đây là nền tảng có thể mở rộng cho các ứng dụng thương mại điện tử hiện đại.

#### Các Dịch vụ AWS Đã Sử Dụng
- **Amazon EC2**: Triển khai backend Node.js.
- **Amazon S3**: Lưu trữ và phân phối frontend React (tĩnh).
- **Amazon DocumentDB**: Cung cấp cơ sở dữ liệu tương thích MongoDB với khả năng mở rộng, sao lưu, và mã hóa.

#### Main Content

1. [Giới thiệu](1-introduction/)
2. [Chuẩn bị](2-preparation/)
3. [Khởi tạo các dịch vụ AWS](3-initialize-aws-services)
4. [Triển khai dự án](4-deploy-project/)
5. [Dọn dẹp tài nguyên](5-clean-up-resources/)
<!-- need to remove parenthesis for path in Hugo 0.88.1 for Windows-->