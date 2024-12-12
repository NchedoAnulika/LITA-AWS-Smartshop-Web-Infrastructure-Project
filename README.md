# LITA-AWS-Smartshop-Web-Infrastructure-Project
 Building a scalable and secure web infrastructure on AWS for SmartShop, a fictional retail company. This project includes EC2 instance setup, VPC configuration, security best practices, and monitoring solutions to ensure high availability and performance.
# SmartShop Web Infrastructure Project

## Project Overview

SmartShop is a fictional mid-sized retail company launching an online store. To support increased web traffic and ensure a smooth customer experience, we have designed a scalable and reliable web infrastructure on AWS.

## Objectives

- **Scalable Resource Allocation**: Support anticipated growth with flexible resource management.
- **High Availability**: Ensure consistent user experience across various traffic loads.
- **Security**: Implement strong measures to protect customer data.
- **Cost-Effectiveness**: Optimize performance while minimizing operational costs.

## AWS Services Utilized

- **Amazon EC2**: Hosting the scalable web application.
- **Amazon VPC**: Isolating the network environment for better security.
- **Amazon CloudWatch**: Monitoring resources and setting up alerts.
- **AWS CloudTrail**: Auditing AWS API calls for security compliance.

## Project Tasks

1. **Launch EC2 Instances**
   - Selected an appropriate Amazon Machine Image (AMI) and launched instances within the chosen VPC.
   - Installed and configured a web server (Apache/Nginx) and deployed the SmartShop web application.

2. **Set Up a Virtual Private Cloud (VPC)**
   - Created a new VPC with public and private subnets across multiple Availability Zones.
   - Configured Internet Gateways and Route Tables for traffic management.

3. **Configure Security Groups**
   - Created Security Groups to control inbound and outbound traffic.
   - Allowed HTTP (port 80) and HTTPS (port 443) while restricting SSH (port 22) access.

4. **Implement Security Best Practices**
   - Used Network Access Control Lists (NACLs) for additional subnet-level security.

5. **Enable Monitoring and Logging**
   - Set up CloudWatch for monitoring key metrics and established alerts for critical events.
   - Utilized AWS CloudTrail for auditing API calls.

## Documentation

- Comprehensive documentation includes configurations for VPC settings, security groups, IAM roles, and scaling policies.
- A cost analysis has been conducted to estimate monthly AWS costs, with suggestions for cost-optimization strategies.

## Expected Outcomes

- A fully functional web application infrastructure tailored to SmartShop's needs.
- Documentation and a professional presentation for stakeholders.
- Hands-on experience with essential AWS services.