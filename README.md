# AWS-VPC-Project Static Website Hosting with ASG & ALB  
# OVERVIEW
Deployed a static website on AWS using a custom VPC architecture with public/private subnets, an Auto Scaling Group, and an Application Load Balancer.
# Architecture
-1 VPC (10.0.0.0/24)
-4 Subnets across 2 AZs (ap-south-1a, ap-south-1b) — 2 public, 2 private.
-EC2 instance in private subnet, static site deployed via SSM/bastion.
-Auto Scaling Group launching instances from a custom AMI.
-Application Load Balancer in public subnets, internet-facing.
-Target Group health-checked and attached to ASG.
# steps
1)Created VPC with public/private subnets across 2 AZs
2)Launched EC2 instance in private subnet, installed web server, deployed static site, tested via bastion/SSM
3)Created Launch Template + AMI from configured instance
4)Created Auto Scaling Group across subnets
5)Created Application Load Balancer with Target Group
6)Verified site accessible via ALB DNS endpoint
# Screenshots
<img width="1920" height="1080" alt="Screenshot 2026-09-02 102338" src="https://github.com/user-attachments/assets/3527838c-8342-453f-a807-7c36dde2862e" />
<img width="1648" height="542" alt="Screenshot 2026-09-02 104315" src="https://github.com/user-attachments/assets/b5f96568-347d-4ea1-879e-b59c197a8a75" />
<img width="1920" height="1080" alt="Screenshot 2026-09-02 102422" src="https://github.com/user-attachments/assets/f06d8692-db5a-46ba-a87b-65195b8062c4" />
<img width="1920" height="1080" alt="Screenshot 2026-09-02 102948" src="https://github.com/user-attachments/assets/5adc2797-4f55-4f9b-8eca-f87303007e96" />
<img width="1920" height="1080" alt="Screenshot 2026-09-02 102523" src="https://github.com/user-attachments/assets/6511b277-dd2b-4b2f-bda1-bcf9aa171d4f" />
# Tech Used
AWS VPC, EC2, Auto Scaling Group, Application Load Balancer, S3
