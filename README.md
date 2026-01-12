Auto Scaling Group with Application Load Balancer (AWS)


📌 Project Overview

This project demonstrates how to design and implement an Auto Scaling architecture using AWS. An Application Load Balancer (ALB) distributes incoming traffic across EC2 instances that are automatically launched or terminated by an Auto Scaling Group (ASG) based on demand. This setup ensures high availability, scalability, and fault tolerance.

-------------------------------------------------------------------------------

🎯 Objective

Automatically scale EC2 instances based on CPU utilization

Distribute traffic evenly using an Application Load Balancer

Improve reliability and performance of a web application

-------------------------------------------------------------------------


🛠️ AWS Services Used

Amazon EC2 – Compute resources

Launch Template – Defines EC2 configuration for Auto Scaling

Auto Scaling Group (ASG) – Automatically manages EC2 instances

Application Load Balancer (ALB) – Distributes traffic

Target Group – Routes requests and performs health checks

Amazon VPC – Networking

CloudWatch – Monitoring and scaling metrics

Security Groups – Network security

---------------------------------------------------------------

🧱 Architecture

Application Load Balancer (Internet-facing)

ALB Listener on HTTP (Port 80)

Target Group with EC2 instances

Auto Scaling Group across multiple Availability Zones

Launch Template used to create EC2 instances

CPU-based scaling policy

User → Application Load Balancer → Auto Scaling Group → EC2 Instances 

--------------------------------------------------------------

⚙️ Implementation Steps

1. Create Launch Template

Amazon Linux 2 AMI

Instance type: t2.micro

Apache Web Server installed using user data

Security group allows HTTP (80) and SSH (22)

2. Create Auto Scaling Group

Use the launch template

Deploy instances across multiple Availability Zones

Desired capacity: 2

Minimum capacity: 1

Maximum capacity: 4

3. Attach Application Load Balancer

Attach existing ALB

Associate the target group with ASG

Enable health checks

4. Configure Scaling Policy

Scaling type: Target tracking

Metric: Average CPU Utilization

Target value: 50%

5. Verify Deployment

Instances launched automatically

Targets show Healthy status

ALB DNS name serves the application

Traffic distributed across instances

--------------------------------------------------

✅ Results

Auto Scaling Group dynamically manages EC2 instances

Load Balancer distributes traffic efficiently

High availability achieved across Availability Zones

Fault tolerance ensured with automatic instance 

---------------------------------------------------------------

📈 Benefits

Automatic scaling based on demand

Improved performance and reliability

Cost optimization by scaling in during low traffic

Production-ready cloud architecture

-------------------------------------------------------------

👤 Author

Dharani Boominathan
AWS Learner | Cloud Computing Enthusiast



