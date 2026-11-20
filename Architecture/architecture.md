# AWS High Availability Architecture

## Infrastructure

- **Region:** Asia Pacific (Mumbai) – ap-south-1
- **VPC:** cloud-devops-vpc
- **VPC CIDR:** 10.0.0.0/16

## Availability Zones

    | Subnet | Availability Zone | CIDR |

| public-subnet-1 | ap-south-1a | 10.0.1.0/24 |
| public-subnet-2 | ap-south-1b | 10.0.2.0/24 |

## Components

1. Internet Gateway – provides internet connectivity.
2. Application Load Balancer – receives incoming HTTP requests.
3. Target Group – manages registered EC2 targets and health checks.
4. EC2 Instance 1 – hosts the Apache web server.
5. EC2 Instance 2 – hosts the Apache web server.

## Request Flow

Internet → Application Load Balancer → Target Group → EC2 Instances → Apache Web Server

## Security

- ALB accepts HTTP traffic on port 80.
- EC2 instances accept HTTP traffic from the ALB security group.
- SSH access is restricted to the configured client IP.
