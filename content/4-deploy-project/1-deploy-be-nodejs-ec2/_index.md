---
title : "Deploy Backend"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : " <b> 4.1 </b> "
---

## Deployment Steps

#### SSh into EC2
In this section, we use **MobaXterm**, which you can download [here](https://mobaxterm.mobatek.net/):

1. After installation, open the main interface, click **Sessions** → **New Session**, then choose **SSH**.

![Deploy Backend](/images/4/0041.png?featherlight=false&width=90pc)

2. Go back to the **EC2 Console**, under **Instances**, select your EC2 instance and click **Connect**.

![Deploy Backend](/images/3/0032.png?featherlight=false&width=90pc)

3. In the **SSH client** tab, copy the **Public DNS**.


4. In **Basic SSH settings** in MobaXterm:
   - Paste the copied **Public DNS** into **Remote host**
   - Tick **Specify username** and enter `ec2-user`

5. In **Advanced SSH settings**:
   - Tick **Use private key** and select the saved key file `my-workshop-keypair.pem`
   - Click **OK** to connect

![Deploy Backend](/images/4/0042.png?featherlight=false&width=90pc)

6. Click **Access** 

![Deploy Backend](/images/4/0043.png?featherlight=false&width=90pc)

![Deploy Backend](/images/4/0044.png?featherlight=false&width=90pc)

#### Tải source code từ Github về EC2 và cài các thư viện cần thiết

1. In the EC2 terminal, install Git:
```bash
sudo yum install git -y
```

2. Clone project:
```bash
git clone PROJECT_LINK
```

3. Refresh the folder view to verify the cloned repo.

![Deploy Backend](/images/4/0045.png?featherlight=false&width=90pc)

4. Install **nvm** (Node Version Manager):

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
```

5. Activate nvm:
```bash
NVM_DIR="$HOME/.nvm"
source "$NVM_DIR/nvm.sh"
```

6. Install and use Node.js version 16:
```bash
nvm use 16
```

7. Check installed versions:

```bash
node -v
npm -v
```

8. Inside the project folder, create the required .env and other configuration files.

9. Install dependencies:

```bash
cd FOLER_PROJECT
npm install
```

#### Connect to DocumentDB and Frontend

1. Download the [global bundle.pem](https://truststore.pki.rds.amazonaws.com/global/global-bundle.pem) and upload it to your project directory.

   {{% notice tip %}}
   It’s recommended to save the file in your user's Downloads or Documents folder to avoid permission issues when uploading.
   {{% /notice %}}

2. In the **DocumentDB console**, under **Clusters**, select your DocumentDB instance and copy the **Connect with application** URI.

![Deploy Backend](/images/4/0049.png?featherlight=false&width=90pc)

3. Insert your password into the copied connection URI and paste it into the mongoose.connect line in your backend code.

4. Copy your **S3 Static Website Hosting** URL and set it as the urlFE (frontend URL) in your backend’s Axios configuration.

5. Start the backend server:

```bash
npm start
```