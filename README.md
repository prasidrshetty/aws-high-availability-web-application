# Highly Available Web Application on AWS

## Project Overview
Built and deployed a highly available web application using AWS infrastructure. The application runs on two EC2 instances across different Availability Zones, with an Application Load Balancer distributing incoming HTTP traffic.

## AWS Services Used
- Amazon VPC
- Public Subnets
- Internet Gateway
- Route Tables
- Security Groups
- Amazon EC2
- Application Load Balancer (ALB)
- Target Groups
- Apache Web Server

## Architecture
- Created a custom VPC with CIDR block `10.0.0.0/16`.
- Created two public subnets in separate Availability Zones.
- Configured an Internet Gateway and route table.
- Launched two Amazon Linux EC2 instances.
- Installed and configured Apache on both instances.
- Created a Target Group and registered both EC2 instances.
- Configured an internet-facing Application Load Balancer.
- Configured HTTP traffic routing through the ALB.

## Traffic Flow
Internet Users → Application Load Balancer → Target Group → EC2 Instance 1 / EC2 Instance 2 → Apache Web Server

## Implementation Results
- Successfully hosted a webpage on both EC2 instances.
- Accessed the application using the ALB DNS name.
- Verified traffic distribution by refreshing the webpage and observing responses from both instances.
-Tested failover by stopping one EC2 instance.
-Verified that the ALB continued serving requests through the remaining healthy instance.

## What I Learned
- AWS networking and VPC configuration.
- Public subnets and Internet Gateway.
- EC2 deployment and Linux administration.
- Security group configuration.
- Application Load Balancer and Target Groups.
- Basic cloud application deployment and traffic distribution.

## Future Improvements
- Test automatic failover when an EC2 instance becomes unhealthy.
- Configure Auto Scaling.
- Add CloudWatch monitoring.
- Automate infrastructure deployment using AWS CloudFormation.