---
title : "Chạy và kiểm tra"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 4.3 </b> "
---


#### Chạy Backend với pm2
```bash
npm install -g pm2
pm2 start bin/www --name {myappname}
pm2 list
pm2 save
pm2 startup
```
Sau khi chạy xong sẽ trả về một dòng lệnh bạn chỉ cần chạy dòng lệnh đó là server backend sẽ hoạt động

#### Kiểm tra nhập dữ liệu vào DocumentDB

Gọi hàm create sản phẩm với file ảnh trong body

![Testing](/images/4/0097.png?featherlight=false&width=90pc)

#### Kiểm tra truy xuất dữ liệu trong DocumentDB trên web

![Testing](/images/4/0097.png?featherlight=false&width=90pc)

![Testing](/images/4/0099.png?featherlight=false&width=90pc)

![Testing](/images/4/0076.png?featherlight=false&width=90pc)