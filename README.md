# LITA-AWS-Smartshop-Web-Infrastructure-Project
 Building a scalable and secure web infrastructure on AWS for SmartShop, a fictional retail company. This project includes EC2 instance setup, VPC configuration, security best practices, and monitoring solutions to ensure high availability and performance.
# SmartShop Web Infrastructure Project

## Table of Contents
1. [Project Overview](#project-overview)
2. [Objectives](#objectives)
3. [AWS Services Utilized](#aws-services-utilized)
4. [Project Tasks](#project-tasks)
   - [Configure a Custom VPC](#configure-a-custom-vpc)
   - [Launch an EC2 Instance with Apache Web Server](#launch-an-ec2-instance-with-apache-web-server)
5. [Cost Analysis](#cost-analysis)
6. [Future Work](#future-work)
7. [Screenshots](#screenshots)
8. [License](#license)

## Project Overview
SmartShop is a fictional retail company expanding into online sales. This project aims to design and deploy a scalable web infrastructure on AWS, ensuring high availability, security, and performance.

## Objectives
- Support anticipated growth with flexible resource allocation.
- Ensure high availability and consistent user experience.
- Implement strong security measures to protect customer data.
- Be cost-effective and optimized for performance.

## AWS Services Utilized
- **Amazon EC2**: Hosting the scalable web application.
- **Amazon VPC**: Isolating the network environment.
- **Amazon CloudWatch**: Monitoring resources and setting up alerts.
- **AWS CloudTrail**: Auditing AWS API calls.

## Project Tasks

### Configure a Custom VPC
A custom Virtual Private Cloud (VPC) was created to host the SmartShop infrastructure. The VPC has an IPv4 CIDR block of `10.0.0.0/16`. Within this VPC, two subnets were established:
- **Public Subnet**: CIDR `10.0.1.0/24`
- **Private Subnet**: CIDR `10.0.2.0/24`

An Internet Gateway was added and attached to the VPC, enabling internet access. A route table was created for the public subnet with a route directing traffic to `0.0.0.0/0` via the Internet Gateway. Network Access Control Lists (NACLs) were configured to allow inbound HTTP (port 80) and SSH (port 22) traffic.

Security Groups were set up to manage access to the EC2 instances, allowing inbound HTTP from anywhere and SSH access restricted to specific IP addresses.

### Launch an EC2 Instance with Apache Web Server
An EC2 instance named `nchedochukwuarinzechukwu_lita` was launched using Amazon Linux 2 with a t2.micro instance type, configured in the public subnet. A key pair named `MyKeyPair` was created for secure SSH access.

After configuring the network settings to enable auto-assigning a public IP, the instance was launched successfully. 

## Cost Analysis
The estimated monthly cost for running the SmartShop web infrastructure on AWS is approximately $15-$25, depending on usage patterns. This includes costs for EC2 instance usage, data transfer, and storage. Cost-optimization strategies include:

- Utilizing AWS Free Tier services where applicable.
- Monitoring usage with AWS CloudWatch to adjust resources as needed.

## Future Work
- Explore further scalability options and performance optimizations.
- Implement additional features based on user feedback.

## Screenshots
- **EC2 Instance Details**:
  ![EC2 Instance Details](/EC2_Instance.png)

- **VPC Configuration**:
  ![VPC Configuration](/VPC.png)

- **Security Group**:
  ![Security Group](/EC2_Instance_Security_group.png)

- **Private Subnet**:
  ![Private Subnet](/Private_subnet.png)

- **Public Subnet**:
  ![Public Subnet](/Public_subnet.png)

- **Apache Test Page**:
  ![Apache Test Page](/Apache_Test_page.png)



To install the Apache web server, the following commands were executed via SSH:
```bash
sudo yum update -y
sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd
