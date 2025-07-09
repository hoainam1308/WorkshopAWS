---
title : "Run and Test"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 4.3 </b> "
---


#### Run Backend with PM2
Use [PM2](https://pm2.keymetrics.io/) to keep your backend running persistently on the EC2 instance, even after restarts.
Install PM2 globally and run your app:
```bash
npm install -g pm2
pm2 start bin/www --name {myappname}
pm2 list
pm2 save
pm2 startup
```
After executing pm2 startup, PM2 will return a command. Copy and run that command to enable automatic startup on reboot.

#### Test Data Insertion into DocumentDB

Sử dụng REST client (như Postman hoặc Thunder Client) để gửi POSTyêu cầu đến API backend của bạn để tạo sản phẩm. Đảm bảo đính kèm tệp hình ảnh trong nội dung yêu cầu.

![Testing](/images/4/0097.png?featherlight=false&width=90pc)

#### Verify Data Retrieval on Frontend

![Testing](/images/4/0097.png?featherlight=false&width=90pc)

![Testing](/images/4/0099.png?featherlight=false&width=90pc)

![Testing](/images/4/0076.png?featherlight=false&width=90pc)