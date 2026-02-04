<p align="center"> <img src="https://img.shields.io/badge/AWS-Cloud-orange?style=for-the-badge\&logo=amazonaws\&logoColor=white"/> <img src="https://img.shields.io/badge/EC2-Compute-red?style=for-the-badge\&logo=amazonec2\&logoColor=white"/> <img src="https://img.shields.io/badge/VPC-Network-blue?style=for-the-badge\&logo=amazonaws\&logoColor=white"/> <img src="https://img.shields.io/badge/LoadBalancer-ALB-green?style=for-the-badge"/> <img src="https://img.shields.io/badge/AutoScaling-Enabled-brightgreen?style=for-the-badge"/> <img src="https://img.shields.io/badge/CloudWatch-Monitoring-yellow?style=for-the-badge"/> <img src="https://img.shields.io/badge/CloudTrail-Auditing-lightgrey?style=for-the-badge"/> <img src="https://img.shields.io/badge/Status-Production%20Ready-success?style=for-the-badge"/> </p>

Enterprise-Grade Highly Available Web Application on AWS

Project Overview



Designed and deployed a highly available and auto-healing web application on AWS using Ubuntu Linux.



Architecture ensures:



High Availability



Auto Scaling



Load Balancing



Monitoring



Security Auditing



AWS Services Used



VPC • Subnets • Internet Gateway • Route Tables • EC2 • AMI • Load Balancer • Auto Scaling • CloudWatch • CloudTrail



Architecture Flow



Users → Application Load Balancer → Auto Scaling EC2 → Monitoring + Logging



Implementation Steps

1\. Created Custom VPC



CIDR: 10.0.0.0/16

Public Subnet 1: 10.0.1.0/24

Public Subnet 2: 10.0.3.0/24

Private Subnet: 10.0.2.0/24



2\. Configured Security Group



SSH (22) → My IP

HTTP (80) → Public Access



3\. Launched Ubuntu EC2 \& Installed Apache



Commands used:

sudo apt update -y

sudo apt install apache2 -y

sudo systemctl start apache2

sudo systemctl enable apache2



4\. Created AMI (Golden Image)



Used to automatically create identical servers.



5\. Created Application Load Balancer



Traffic distributed across multiple EC2 instances.



6\. Created Auto Scaling Group



Min: 1

Desired: 2

Max: 3



Auto healing tested by terminating EC2 → new instance launched automatically.



7\. Configured CloudWatch Monitoring



CPU Alarm created for scaling.



8\. Enabled CloudTrail Auditing



Tracked RunInstances and TerminateInstances events.



Final Outcome



Highly Available • Self Healing • Auto Scaling • Monitored • Secure AWS Infrastructure



Author



AWS DevOps Hands-on Project

