---
title : "Tạo S3 Bucket"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 3.3 </b> "
---

#### Tạo S3 Bucket

1. Mở Amazon S3 console tại https://console.aws.amazon.com/s3 chọn Create bucket

![Tạo S3 Bucket](/images/3/0052.png?featherlight=false&width=90pc)

2. Nhập bucket name ví dụ: ```workshop-s3-fe```

![Tạo S3 Bucket](/images/3/0053.png?featherlight=false&width=90pc)

3. Uncheck **Block all public access** và check vào xác nhận bên dưới

![Tạo S3 Bucket](/images/3/0054.png?featherlight=false&width=90pc)

4. Kiểm tra và **Create bucket**

![Tạo S3 Bucket](/images/3/0055.png?featherlight=false&width=90pc)

![Tạo S3 Bucket](/images/3/0056.png?featherlight=false&width=90pc)

5. Trong tab **permission** của bucket vừa tạo, tại phần **Bucket policy** chọn **Edit**, copy đoạn code sau và cho vào **Policy**:
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::workshop-s3-fe/*"
    }
  ]
}
```

![Tạo S3 Bucket](/images/3/0058.png?featherlight=false&width=90pc)

![Tạo S3 Bucket](/images/3/0060.png?featherlight=false&width=90pc)

![Tạo S3 Bucket](/images/3/0061.png?featherlight=false&width=90pc)

6. Chọn **Save changes**

![Tạo S3 Bucket](/images/3/0062.png?featherlight=false&width=90pc)

![Tạo S3 Bucket](/images/3/0063.png?featherlight=false&width=90pc)

7. Lấy địa chỉ EC2 để cấu hình urlBE trong Frontend reactjs

8. Build Frontend:
   - Mở Fronend reactjs bằng Visual Studio Code
   - Sửa lại biến môi trường ```VITE_BACKEND_URL``` trong file .env
   - Build Frontendh bằng câu lẹnh ```npm run build``` trong terminal sẽ tạo ra folder **dist** (hoặc **build**)

![Tạo S3 Bucket](/images/3/0059.png?featherlight=false&width=90pc)

9. Upload các file/folder trong thư mục vừa build được lên S3:
   - Tại tab **Objects** của S3 bucket, chọn **Upload**
   ![Tạo S3 Bucket](/images/3/0064.png?featherlight=false&width=90pc)
   - Kéo các file/folder trong thư mục vừa build được vào phần **Upload**
   ![Tạo S3 Bucket](/images/3/0065.png?featherlight=false&width=90pc)
   ![Tạo S3 Bucket](/images/3/0066.png?featherlight=false&width=90pc)
   - Chọn **Upload** và đợi upload xong
   ![Tạo S3 Bucket](/images/3/0069.png?featherlight=false&width=90pc)
   ![Tạo S3 Bucket](/images/3/0070.png?featherlight=false&width=90pc)


10. Enable static website hosting
   - Tại tab **Properties**, trong phần **Static website hosting** chọn **Edit**
   ![Tạo S3 Bucket](/images/3/0071.png?featherlight=false&width=90pc)
   ![Tạo S3 Bucket](/images/3/0072.png?featherlight=false&width=90pc)
   - Check **Enable** tại **Static website hosting**
   - Trong phần **Index document** nhập ```index.html```
   ![Tạo S3 Bucket](/images/3/0073.png?featherlight=false&width=90pc)
   - Nhấn **Save change** để lưu lại và kiểm tra Frontend
   ![Tạo S3 Bucket](/images/3/0074.png?featherlight=false&width=90pc)
   ![Tạo S3 Bucket](/images/3/0075.png?featherlight=false&width=90pc)