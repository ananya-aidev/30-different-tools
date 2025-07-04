# 🚀 AWS EC2: Launch Instance & Install Apache

This guide explains how to launch an AWS EC2 instance, SSH into it, and install the Apache web server.

---

## 🧠 What is AWS EC2?

**EC2 (Elastic Compute Cloud)** is like a virtual computer (server) in the cloud.

You can:
- Launch a Linux/Windows machine
- Install packages (like Apache, Python, Docker, etc.)
- Use it like a remote server for websites or apps

---

## ✅ Step-by-Step: Launch EC2 and Install Apache

### 1. Launch EC2 Instance
- Go to the **AWS EC2 Console**
- Click **Launch Instance**
- Choose an OS: **Ubuntu** or **Amazon Linux**
- Instance type: **t2.micro** (Free Tier)
- Create or use an existing **key pair** (`.pem` file)
- Configure **security group** to allow:
  - **SSH (22)** for remote login
  - **HTTP (80)** for Apache

---

### 2. Connect via SSH

```bash
chmod 400 my-key.pem
ssh -i my-key.pem ubuntu@<your-ec2-public-ip>       # For Ubuntu
# OR
ssh -i my-key.pem ec2-user@<your-ec2-public-ip>     # For Amazon Linux
