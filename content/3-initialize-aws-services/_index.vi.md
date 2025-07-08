---
title: "Khởi tạo các dịch vụ AWS cần thiết"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

## EC2

{{< figure src="/images/Arch_Amazon-EC2_64.png" title="Amazon DocumentDB" width="150pc" >}}

Amazon Elastic Compute Cloud (EC2) là một dịch vụ cốt lõi của Amazon Web Services cung cấp năng lực tính toán co giãn trên nền tảng đám mây. Dưới đây là tổng quan về EC2:[[1]](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/compute-services.html)

- EC2 cho phép người dùng khởi chạy các máy chủ ảo (gọi là instance) trong môi trường đám mây AWS.
- Hỗ trợ nhiều loại instance được tối ưu hóa cho các mục đích khác nhau, cung cấp sự kết hợp đa dạng giữa CPU, bộ nhớ, lưu trữ và băng thông mạng.
- Người dùng có toàn quyền kiểm soát đối với các instance EC2, bao gồm việc khởi động, dừng và kết thúc bất cứ lúc nào.
- Hỗ trợ nhiều hệ điều hành như các bản phân phối Linux khác nhau và Windows Server.
- Cung cấp nhiều mô hình giá linh hoạt: On-Demand, Reserved Instance và Spot Instance giúp tối ưu chi phí theo nhu cầu công việc.
- EC2 tích hợp với các dịch vụ khác của AWS như Elastic Block Store (EBS) để lưu trữ dữ liệu bền vững và Auto Scaling để tự động mở rộng quy mô theo nhu cầu.
- Tích hợp bảo mật như VPC, security groups và key pair để truy cập an toàn.
- Instance EC2 có thể được khởi chạy tại nhiều Availability Zone trong cùng một vùng để đảm bảo tính sẵn sàng cao và khả năng chịu lỗi.

EC2 là nền tảng quan trọng cho nhiều ứng dụng và khối lượng công việc dựa trên đám mây nhờ khả năng mở rộng, linh hoạt và tích hợp chặt chẽ với các dịch vụ khác.

**Nguồn:**  
[[1] AWS Compute Services category icon Compute - Overview of Amazon Web Services](https://docs.aws.amazon.com/whitepapers/latest/aws-overview/compute-services.html)

---

## S3

{{< figure src="/images/Arch_Amazon-Simple-Storage-Service_48.png" title="Amazon DocumentDB" width="150pc" >}}

Amazon Simple Storage Service (S3) là một dịch vụ lưu trữ đối tượng có khả năng mở rộng cao, độ bền cao và linh hoạt do AWS cung cấp. Tổng quan về S3: [[1]](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html)

- **Lưu trữ đối tượng:** S3 lưu trữ dữ liệu dưới dạng đối tượng trong các bucket – lý tưởng cho dữ liệu không có cấu trúc như tài liệu, hình ảnh và video. [[2]](https://aws.amazon.com/s3/)
- **Khả năng mở rộng:** S3 có thể lưu trữ gần như không giới hạn dữ liệu, cho phép doanh nghiệp mở rộng lưu trữ linh hoạt.
- **Độ bền và khả năng sẵn sàng:** Được thiết kế với độ bền lên tới 99.999999999% (11 số 9), đảm bảo dữ liệu luôn an toàn.
- **Bảo mật:** Hỗ trợ mã hóa dữ liệu khi lưu trữ và khi truyền tải, chính sách kiểm soát truy cập và tích hợp IAM.
- **Hiệu năng:** Truy xuất dữ liệu với độ trễ thấp và tốc độ xử lý cao, phù hợp cho nhiều loại ứng dụng.
- **Lớp lưu trữ đa dạng:** Các lớp như S3 Standard, Intelligent-Tiering, S3 Glacier giúp tối ưu chi phí theo tần suất truy cập.
- **Quản lý dữ liệu:** Hỗ trợ versioning, replication, lifecycle policies giúp quản lý hiệu quả vòng đời dữ liệu.
- **Tích hợp:** Kết nối dễ dàng với các dịch vụ khác của AWS như Lambda, CloudFront, Athena…
- **Chi phí hợp lý:** Tính phí theo mức sử dụng thực tế.
- **Khả năng truy cập toàn cầu:** Truy cập dữ liệu từ bất kỳ đâu, lý tưởng cho phân phối nội dung toàn cầu.

**Nguồn:**  
[[1] What is Amazon S3? - Amazon Simple Storage Service](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html)  
[[2] Cloud Object Storage – Amazon S3 – Amazon Web Services](https://aws.amazon.com/s3/)

---

## DocumentDB

{{< figure src="/images/Arch_Amazon-DocumentDB_64.png" title="Amazon DocumentDB" width="150pc" >}}

Amazon DocumentDB là một dịch vụ cơ sở dữ liệu dạng tài liệu được quản lý hoàn toàn bởi AWS, tương thích với MongoDB. Tổng quan về DocumentDB: [[1]](https://aws.amazon.com/documentdb/features/)  

- **Tương thích MongoDB:** Hỗ trợ API MongoDB 3.6 và 4.0 – có thể sử dụng driver và công cụ MongoDB sẵn có với thay đổi tối thiểu.[[2]](https://docs.aws.amazon.com/whitepapers/latest/choosing-an-aws-nosql-database/amazon-documentdb.html)  
- **Quản lý hoàn toàn:** AWS đảm nhiệm việc cấp phát hạ tầng, vá lỗi, sao lưu và các tác vụ quản trị – bạn chỉ cần tập trung vào phát triển ứng dụng.[[3]](https://aws.amazon.com/blogs/publicsector/value-of-document-databases-in-public-sector-amazon-documentdb/)
- **Khả năng mở rộng:** Hỗ trợ hàng triệu truy vấn mỗi giây, lưu trữ mở rộng tự động – tối đa 128 TiB với instance-based và 4 PiB với Elastic Clusters.
- **Hiệu suất cao:** Sử dụng hệ thống lưu trữ phân tán, tự phục hồi và có khả năng chịu lỗi.
- **Tính sẵn sàng cao:** Dữ liệu được nhân bản qua nhiều Availability Zone.
- **Bảo mật:** Cách ly mạng, mã hóa khi lưu trữ và khi truyền, tích hợp IAM để kiểm soát truy cập.
- **Trường hợp sử dụng:** Phù hợp với hệ thống quản lý nội dung, hồ sơ người dùng, backend mobile và ứng dụng JSON động.
- **Mô hình dữ liệu:** Lưu trữ, truy vấn và đánh chỉ mục dữ liệu dạng JSON – phù hợp cho schema linh hoạt.
- **Tích hợp:** Kết nối với các dịch vụ như AWS Glue, Amazon S3, Amazon SageMaker để xử lý dữ liệu và machine learning.

**Nguồn:**  
[[1] JSON Document Database - Amazon DocumentDB (with MongoDB compatibility) Features - AWS](https://aws.amazon.com/documentdb/features/)  
[[2] Amazon DocumentDB (with MongoDB compatibility) - Choosing an AWS NoSQL Database](https://docs.aws.amazon.com/whitepapers/latest/choosing-an-aws-nosql-database/amazon-documentdb.html)  
[[3] The value of document databases in the public sector - AWS Public Sector Blog](https://aws.amazon.com/blogs/publicsector/value-of-document-databases-in-public-sector-amazon-documentdb/)