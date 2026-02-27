# Build Your VPC and Launch a Web Server (AWS) 

## Author

* **Name**: Ramitha Chowdary S
* **Register Number**: 212224240130
* **Date of Submission**: 26-02-2026

---

## Objective

The objective of this experiment is to understand how to design and configure a basic network infrastructure in AWS using a Virtual Private Cloud (VPC). This lab focuses on creating a VPC with a public subnet, configuring an Internet Gateway and route table, launching an EC2 instance, and hosting a simple web server that can be accessed over the internet.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity

---

## Tools Used

* AWS Management Console
* Amazon VPC
* Amazon EC2
* Internet Gateway
* Route Table
* Security Groups

---

## Tasks Performed

### Task 1: Create a VPC

Create a new Virtual Private Cloud (VPC) with a private IP address range. The VPC acts as a logically isolated network in AWS where all other resources will be deployed.

Students should create a VPC with an appropriate CIDR block (for example, 10.0.0.0/16) and assign a meaningful name.


### Task 2: Create a Public Subnet

Create a subnet inside the VPC to host public resources. Enable auto-assign public IPv4 so that instances launched in this subnet receive a public IP address.

The subnet should use a smaller CIDR range (for example, 10.0.1.0/24).


### Task 3: Create and Attach Internet Gateway

Create an Internet Gateway (IGW) and attach it to the VPC. This allows communication between resources in the VPC and the internet.


### Task 4: Configure Route Table

Create a route table and add a default route (0.0.0.0/0) pointing to the Internet Gateway. Associate this route table with the public subnet.

This step ensures that traffic from the subnet can reach the internet.


### Task 5: Create Security Group

Create a security group to act as a virtual firewall for the EC2 instance. Configure inbound rules to allow:

SSH on port 22

HTTP on port 80


### Task 6: Launch EC2 Instance

Launch an EC2 instance inside the public subnet using Amazon Linux 2 AMI and a suitable instance type (t2.micro).

Attach the previously created security group and key pair.


### Task 7: Configure Web Server

Install and start a web server (Apache HTTPD) on the EC2 instance using user data or manual commands.

Create a simple HTML page and verify that it can be accessed from a web browser using the public IP address of the instance.---

## Workflow (Student Explanation)

**1.** First, I logged into the AWS Management Console and created a new VPC using the VPC wizard with a CIDR block of 10.0.0.0/16. This automatically created public and private subnets, route tables, and an Internet Gateway.<br>

**2.** Next, I verified the subnets and ensured that the public subnet had internet access through the Internet Gateway and proper routing configuration.<br>

**3.** After that, I created a security group to allow HTTP traffic so that the web server could be accessed from the internet.<br>

**4.** Then, I launched an EC2 instance using Amazon Linux, placed it inside the public subnet, and attached the created security group.<br>

**5.** Finally, I configured the instance to run an Apache web server using user data and verified the deployment by accessing the web page through the instance’s public IP address in a browser.<br>

---

## Output Screenshots (Attach 3)

### Screenshot 1: VPC and Subnet Details

<img width="1919" height="916" alt="552477825-d13a6965-f6e5-4ab2-b5b5-89003ab8a84d" src="https://github.com/user-attachments/assets/9c0aa90e-f74d-4f77-8367-9880e00bbc86" />

---

### Screenshot 2: EC2 Instance Running

<img width="1919" height="928" alt="552477986-a0aaeecd-52b7-4d48-9d87-b5ad7cd8205b" src="https://github.com/user-attachments/assets/70b895b8-0d62-44d4-b203-cadeb3c62034" />

---

### Screenshot 3: Web Server Output in Browser

<img width="1918" height="955" alt="552477703-eb3b5407-5ade-4455-9b5b-02281bd0c2c8" src="https://github.com/user-attachments/assets/10a9b624-373e-4d72-b3d7-6c9f3d457a6a" />

---

## Result 

This experiment successfully demonstrated the creation of a custom VPC and deployment of a public-facing web server in AWS. By configuring networking components such as subnets, route tables, and security groups, and by launching an EC2 instance with a web server, the basic architecture of a cloud-hosted application was understood.
