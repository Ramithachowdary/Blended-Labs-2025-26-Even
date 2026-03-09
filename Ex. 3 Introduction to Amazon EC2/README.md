# Lab 3 – Introduction to Amazon Elastic Compute Cloud (EC2)

## Author

* **Name**: Ramitha chowdary S 
* **Register Number**: 212224240130
* **Date of Submission**: 09-03-2026

---

## Objective

The objective of this experiment is to understand the fundamentals of Amazon Elastic Compute Cloud (EC2). This lab focuses on launching and managing a virtual server, understanding instance types and AMIs, connecting to an EC2 instance, monitoring its status, and performing basic instance operations such as start, stop, and terminate.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity
* Basic knowledge of Linux commands (optional)

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Key Pair
* Security Group
* SSH Client (PuTTY / Terminal)

---

## Tasks Performed

### Task 1: Explore Amazon EC2 Dashboard

Explore the EC2 service dashboard in the AWS Management Console. Observe the different sections such as Instances, AMIs, Instance Types, Key Pairs, Security Groups, and Elastic IPs.

---

### Task 2: Launch an EC2 Instance

Launch a new EC2 instance using Amazon Linux 2 AMI. Select an appropriate instance type (t2.micro) under the free tier. Configure basic settings such as instance name, key pair, and security group.

---

### Task 3: Configure Security Group

Configure a security group to allow inbound access:

* SSH (Port 22) from your IP address
* HTTP (Port 80) from anywhere (0.0.0.0/0)

This security group acts as a firewall for the instance.

---

### Task 4: Connect to EC2 Instance

Connect to the running EC2 instance using SSH. Use the downloaded key pair and connect via terminal or PuTTY.

For Amazon Linux:

```
ssh -i "keyname.pem" ec2-user@<Public-IP>
```

---

### Task 5: Perform Basic Instance Operations

Perform the following operations from the EC2 console:

* Stop the instance
* Start the instance
* Reboot the instance

Observe the state changes of the instance.

---

### Task 6: Monitor EC2 Instance

Monitor the EC2 instance using the Monitoring tab. Observe metrics such as CPU utilization, network in/out, and instance status checks.

---

### Task 7: Terminate EC2 Instance

Terminate the EC2 instance after completing the experiment to avoid unnecessary AWS charges.

---

## Workflow (Student Explanation)

**1.**  First, the AWS Academy Lab environment was started and the AWS Management Console was opened. The EC2 service was selected from the AWS services list, and the region was verified as N. Virginia (us-east-1).

**2.** A new EC2 instance was launched by selecting Launch Instance. The instance was named Web Server, and the Amazon Linux 2023 AMI was selected with the instance type t2.micro. The key pair vockey was chosen for authentication.

**3.** The network configuration was edited by selecting the Lab VPC and the default PublicSubnet1. A new Security Group named Web Server security group was created. Initially, all inbound rules were removed.

**4.** In the Advanced Details section, termination protection was enabled to prevent accidental deletion of the instance. A User Data script was added to automatically install and start the Apache web server and create a simple HTML page.

**5.** The instance was launched and its status was monitored until it changed from Pending → Initializing → Running with 2/2 status checks passed.

**6.** The instance monitoring features were explored using the Status Checks, Monitoring, System Log, and Instance Screenshot options available in the EC2 console.

**7.** To access the web server, the public IPv4 address of the instance was copied and opened in a browser. Initially, the page did not load because HTTP traffic was not allowed.

**8.** The security group inbound rules were updated by adding a rule to allow HTTP (Port 80) from Anywhere (IPv4). After refreshing the browser, the message "Hello From Your Web Server!" was successfully displayed.

**9.** The instance was then stopped in order to resize it. The instance type was changed from t2.micro to t2.small, and stop protection was enabled.

**10.** The Elastic Block Store (EBS) volume size was modified from 8 GiB to 10 GiB to increase storage capacity.

**11.** The instance was started again with the updated configuration, and the EC2 Service Quotas section was explored to understand resource limits.

**12.** Finally, stop protection was tested by attempting to stop the instance. After disabling stop protection, the instance was successfully stopped.

---

## Output Screenshots (Attach 3)

### Screenshot 1: EC2 Dashboard / Instance List

<img width="1643" height="845" alt="556085594-f8311234-c712-45ca-a78d-f6bb3b95e8c5" src="https://github.com/user-attachments/assets/9f5f8919-cc14-4232-8536-dea7c218236c" />

<img width="1630" height="811" alt="556085755-7fe87298-c97d-4a17-9fcf-ec30a2e959c2" src="https://github.com/user-attachments/assets/d559042d-9c49-4aa9-baa2-c53a1e69f166" />

---

### Screenshot 2: SSH Connection to Instance

<img width="1638" height="831" alt="556085913-e3bb52b2-d70e-4421-a179-3823546a6619" src="https://github.com/user-attachments/assets/4c94ac4e-2541-4e37-b481-ab8f47bb806d" />

---

### Screenshot 3: Instance Monitoring / Status

<img width="1325" height="651" alt="556087296-ee22e6e9-2458-4b29-b75f-fa6918f452dc" src="https://github.com/user-attachments/assets/b2ca35cf-defe-4b76-8a9e-9d8586a530be" />

<img width="1250" height="642" alt="556086125-c88b80c8-873f-490f-baee-c5f27b79fc05" src="https://github.com/user-attachments/assets/a14aecb2-75f1-439d-896f-a0bb1d20cc5c" />

---

## Result 

This experiment provided hands-on experience with Amazon EC2 by demonstrating how to launch, connect, manage, and monitor a virtual server in AWS. It helped in understanding the concept of Infrastructure as a Service (IaaS) and how compute resources can be provisioned and controlled on demand in the cloud.
