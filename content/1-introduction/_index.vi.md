---
title : "Giới thiệu"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 1. </b> "
---

**Nội dung:**
- [Tổng quan dự án](#tổng-quan-dự-án)
- [Amazon DocumentDB](#amazon-documentdb)

#### Tổng quan dự án
Dự án website bán hàng được xây dựng với backend Node.js, cơ sở dữ liệu MongoDB và frontend React. Hệ thống hỗ trợ các tính năng cơ bản như: đăng ký, đăng nhập, thêm sản phẩm vào giỏ hàng, thanh toán và xem danh sách đơn hàng đã đặt. Đây là nền tảng có thể mở rộng cho các ứng dụng thương mại điện tử hiện đại.

#### Amazon DocumentDB
Amazon DocumentDB là dịch vụ cơ sở dữ liệu tài liệu tương thích MongoDB do AWS cung cấp, hỗ trợ hai loại cluster (instance-based và elastic) với khả năng mở rộng đọc/ghi lên đến hàng triệu yêu cầu mỗi giây. Dung lượng lưu trữ tự động tăng tối đa 128 TiB, hỗ trợ tối đa 15 bản sao để tăng hiệu năng đọc, và cho phép thay đổi tài nguyên tính toán linh hoạt. Dữ liệu được mã hóa bằng AWS KMS, chạy trong mạng riêng VPC, và hỗ trợ sao lưu tự động cùng khôi phục theo thời gian. DocumentDB có khả năng tự động khôi phục và chuyển đổi dự phòng (failover) khi có sự cố, đồng thời đáp ứng các tiêu chuẩn bảo mật nghiêm ngặt như FedRAMP.

{{< figure src="/images/Arch_Amazon-DocumentDB_16.svg" title="Amazon DocumentDB" width="150pc" >}}