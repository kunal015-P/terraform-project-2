# 🚀 Terraform Project 2: AWS 3-Tier Infrastructure with ALB

## 📌 Project Overview

This project demonstrates how to use Terraform to provision a scalable and highly available infrastructure on AWS.

The architecture includes:

* Custom VPC
* Public subnets across multiple Availability Zones
* EC2 instance
* Application Load Balancer (ALB)
* Security groups and networking components

---

## 🏗️ Architecture

* VPC with CIDR block `10.10.0.0/16`
* Two public subnets:

  * `10.10.1.0/24` (AZ-1)
  * `10.10.2.0/24` (AZ-2)
* Internet Gateway for public access
* Route table associated with both subnets
* EC2 instance running Apache web server
* Application Load Balancer distributing traffic

---

## ⚙️ Technologies Used

* Terraform
* AWS (EC2, VPC, ALB, Subnets, IGW)
* Bash (user data script)

---

## 📁 Project Structure

```
terraform-project-2/
│── main.tf
│── variables.tf
│── terraform.tfvars
│── outputs.tf
│── user_data.sh
│── .gitignore
│── README.md
```

---

## 🚀 Deployment Steps

### 1. Clone the repository

```
git clone <your-repo-url>
cd terraform-project-2
```

### 2. Initialize Terraform

```
terraform init
```

### 3. Preview changes

```
terraform plan
```

### 4. Apply configuration

```
terraform apply
```

Type `yes` when prompted.

---

## 🌐 Access the Application

After successful deployment, Terraform will output:

```
alb_dns = http://<load-balancer-dns>
```

Open this URL in your browser to see the web application.

---

## 🧹 Destroy Infrastructure

To avoid AWS charges, run:

```
terraform destroy
```

---

## ⚠️ Important Notes

* Ensure AWS credentials are configured (`aws configure`)
* Update AMI ID based on your region if needed
* Do not commit sensitive files like `terraform.tfstate`

---

## 📚 Key Learnings

* Infrastructure as Code (IaC) using Terraform
* AWS networking (VPC, subnets, routing)
* Load balancing and high availability
* Automating EC2 provisioning with user data

---

## 🔥 Future Improvements

* Add Auto Scaling Group
* Use Terraform modules
* Implement remote backend (S3 + DynamoDB)
* Add HTTPS with ACM

---

## 👨‍💻 Author

Kunal

---

## ⭐ If you like this project, give it a star!
