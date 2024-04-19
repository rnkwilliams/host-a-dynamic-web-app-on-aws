# Dynamic Website Hosting on AWS
![Alt text](Host_a_Dynamic_Web_App_on_AWS.png)

---
## Overview

This project demonstrates deploying a dynamic website on Amazon Web Services (AWS) using various AWS services to ensure high availability, scalability, fault tolerance, and security. Below is a detailed explanation of the resources and configurations used for this project.

## AWS Resources and Configurations

The website is hosted on EC2 instances within a Virtual Private Cloud (VPC) configured with public and private subnets spanning two Availability Zones. The infrastructure leverages the following AWS resources:

- **Virtual Private Cloud (VPC)**: Configured a VPC with public and private subnets spanning two availability zones for enhanced availability and fault tolerance.

- **Internet Gateway**: An Internet Gateway was deployed to enable connectivity between the VPC instances and the wider internet.

- **Security Groups**: Established Security Groups to serve as a network firewall mechanism to control inbound and outbound traffic to the instances.

- **Availability Zones**: Leveraged two Availability Zones to increase system reliability and fault tolerance.

- **Public Subnets**: Public subnets are used for infrastructure components like the NAT Gateway and Application Load Balancer.

- **Private Subnets**: Host the web servers (EC2 instances) and database (RDS) for enhanced security.

- **EC2 Instance Connect Endpoint**: Implemented EC2 Instance Connect Endpoint for secure SSH connections to assets within both public and private subnets.

- **Web Servers (EC2 Instances)**: Placed web servers within Private Subnets for enhanced security.

- **NAT Gateway**: Allowed instances in both the private Application and Data subnets to access the internet via the NAT Gateway.

- **Website Hosting**: Hosted the website on EC2 Instances.

- **Application Load Balancer (ALB)**: Utilized an Application Load Balancer and a target group for evenly distributing web traffic to an Auto Scaling Group of EC2 instances across multiple Availability Zones.

- **Auto Scaling Group**: Used an Auto Scaling Group to automatically manage EC2 instances, ensuring website availability, scalability, fault tolerance, and elasticity.

- **Certificate Manager**: Secured application communications using AWS Certificate Manager.

- **Simple Notification Service (SNS)**: Configured SNS to alert about activities within the Auto Scaling Group.

- **Domain Name and DNS**: Registered the domain name and set up a DNS record using Amazon Route 53.

- **Amazon S3**: Used Amazon S3 to store application codes.

- **IAM Role**: Created an IAM role for S3 bucket access.

- **Amazon RDS (Relational Database Service)**: Utilized Amazon RDS for the database to securely store dynamic content and user data.

- **Amazon Machine Image (AMI)**: Created an AMI from an EC2 instance so that the Auto Scaling Group can launch new EC2 instances with copies of website applications.

## Deployment

The deployment of this infrastructure is automated using scripts and configuration files stored in a GitHub repository. The repository includes the following:

- **Reference Diagram**: A visual representation of the AWS infrastructure and its components.
- **Deployment Scripts**: Provision and configure the necessary AWS resources.

## GitHub Repository

For detailed deployment scripts and the reference diagram, please visit the [GitHub repository](https://github.com/rnkwilliams/host-a-dynamic-web-app-on-aws).

## Contributing
Feel free to contribute, suggest improvements, or report issues by opening an issue or pull request on the GitHub repository.

## License
This project is licensed under the MIT License.

---
