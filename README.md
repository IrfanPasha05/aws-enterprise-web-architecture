<h1 align="center">☁️ AWS Enterprise Production Architecture</h1>

<h3 align="center">
Highly Available • Auto Scaling • Self Healing • Monitoring • Auditing
</h3>

<p align="center">
  <img src="https://img.shields.io/badge/AWS-Cloud-orange?style=for-the-badge&logo=amazonaws&logoColor=white"/>
  <img src="https://img.shields.io/badge/EC2-Compute-red?style=for-the-badge&logo=amazonec2&logoColor=white"/>
  <img src="https://img.shields.io/badge/VPC-Network-blue?style=for-the-badge&logo=amazonaws&logoColor=white"/>
  <img src="https://img.shields.io/badge/ALB-LoadBalancer-green?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/AutoScaling-Enabled-brightgreen?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/CloudWatch-Monitoring-yellow?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/CloudTrail-Auditing-lightgrey?style=for-the-badge"/>
</p>

<p align="center">
  <img src="architecture.png" width="900"/>
</p>

---

# 🌟 Project Summary

Designed and deployed a **Production-Ready AWS Infrastructure** capable of handling real-world traffic using modern **Cloud & DevOps practices**.

This system automatically:
- Distributes traffic
- Replaces failed servers
- Scales based on demand
- Monitors performance
- Logs all activities

---

# 🎯 Why This Project Matters

Modern companies require **zero-downtime infrastructure**.  
This project demonstrates the core skills needed for a **Cloud / DevOps Engineer role**.

---

# 🧠 Architecture Overview

markdown
Copy code
         🌍 Internet Users
                │
                ▼
    ⚖️ Application Load Balancer
                │
    ┌───────────┴───────────┐
    ▼                       ▼
💻 EC2 Instance 💻 EC2 Instance
(Auto Scaling) (Auto Scaling)
│ │
└───────────┬───────────┘
▼
📊 CloudWatch Monitoring
▼
🔐 CloudTrail Logging

yaml
Copy code

---

# ☁️ AWS Services Used

| Category | Services |
|---|---|
| 🌐 Networking | VPC, Subnets, Internet Gateway, Route Tables |
| 💻 Compute | EC2 Ubuntu, AMI |
| ⚖️ Load Balancing | Application Load Balancer |
| 📈 Scaling | Auto Scaling Group |
| 📊 Monitoring | CloudWatch |
| 🔐 Security | Security Groups |
| 🕵️ Auditing | CloudTrail |

---

# ⚙️ Infrastructure Automation Script

`scripts/install_apache.sh`

```bash
#!/bin/bash
sudo apt update -y
sudo apt install apache2 -y
sudo systemctl start apache2
sudo systemctl enable apache2
echo "<h1>AWS Auto Scaling Server $(hostname)</h1>" > /var/www/html/index.html
🔥 Real Production Tests Performed
Test Scenario	Result
Access Website via Load Balancer	✅ Success
Manually Terminated EC2 Instance	✅ Auto-Healing Triggered
High CPU Simulation	✅ Auto Scaling Triggered
CloudWatch Alarm Triggered	✅ Verified
CloudTrail Logged Actions	✅ Verified

💡 Key Features Achieved
✨ High Availability
✨ Fault Tolerance
✨ Self-Healing Infrastructure
✨ Automatic Scaling
✨ Real-Time Monitoring
✨ Security Auditing

📸 What Happens When Server Fails?
1️⃣ EC2 instance terminated manually
2️⃣ Auto Scaling detects failure
3️⃣ New EC2 launched automatically
4️⃣ Load Balancer registers new instance
5️⃣ Website remains online 😎

💼 Skills Demonstrated
AWS • Linux • Networking • High Availability • Load Balancing • Monitoring • DevOps Fundamentals

🧑‍💻 Author
Irfan Pasha 
AWS DevOps Hands-On Project