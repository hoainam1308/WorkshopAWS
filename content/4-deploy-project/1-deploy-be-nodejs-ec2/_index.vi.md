---
title : "Triển khai Backend"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 4.1 </b> "
---

## Các bước triển khai

#### SSh vào EC2
Ở phần này mình dùng MobaXterm các bạn có thể tải [tại đây](https://mobaxterm.mobatek.net/):  
1. Sau khi cài đặt xong, trong giao diện chính, chọn **Sessions** -> **New Session** sau đó chọn **SSH**

![Triển khai Backend](/images/4/0041.png?featherlight=false&width=90pc)

2. Quay lại EC2 Console, trong phần **Instances** chọn **Instances** sau đó chọn EC2 đã tạo và chọn **Connect**

![Triển khai Backend](/images/3/0032.png?featherlight=false&width=90pc)

3. Trong tab **SHH client** copy **Public DNS**

4. Trong phần **Basic SSH settings** của MobaXterm:
   - Dán **Public DNS** vừa copy vào **Remote host**
   - Tick vào **Specify username** và nhập ```ec2-user```
5. Chọn **Advanced SSH settings**:
   - Tick **Use private key** và chọn file **my-workshop-keypair.pem** đã lưu
   - Nhấn **OK** để connect

![Triển khai Backend](/images/4/0042.png?featherlight=false&width=90pc)

6. Chọn **Access** 

![Triển khai Backend](/images/4/0043.png?featherlight=false&width=90pc)

![Triển khai Backend](/images/4/0044.png?featherlight=false&width=90pc)

#### Tải source code từ Github về EC2 và cài các thư viện cần thiết

1. Trong EC2 chạy câu lệnh sau để cài git:
```bash
sudo yum install git -y
```

2. Clone project:
```bash
git clone PROJECT_LINK
```

3. Refresh thư mục để kiểm tra

![Deploy Backend](/images/4/0045.png?featherlight=false&width=90pc)

4. Cài nvm:

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
```

5. Kích hoạt nvm:
```bash
NVM_DIR="$HOME/.nvm"
source "$NVM_DIR/nvm.sh"
```

6. Cài và sử dụng node nvm install 16:

```bash
nvm use 16
```

7. Kiểm tra node:

```bash
node -v
npm -v
```

8. Trong thư mục project, tạo các file cần thiết như .env

9. Tải dependencies:

```bash
cd project
npm install
```

#### Kết nối tới DocumentDB và FE

1. Tải tệp [global bundle.pem](https://truststore.pki.rds.amazonaws.com/global/global-bundle.pem) và upload lên thư mục project 

   {{% notice tip %}}
   Khi tải về nên đặt trong Downloads hoặc Documents của của user bạn dang dùng để tránh gặp lỗi permission khi upload
   {{% /notice %}}

2. Vào DocumentDB console tại **Clusters** chọn DocumentDB đã tạo copy phần **connect with application**

![Triển khai Backend](/images/4/0049.png?featherlight=false&width=90pc)

3. Sau đó nhập mật khẩu của bạn vào uri vừa copy và đặt vào phần mongoose.connect trong project trên ec2

4. Copy đường dẫn đến static website hosting s3 của bạn và đặt vào urlFE axios trong Backend

5. Chạy Backend để kiểm tra:

```bash
npm start
```