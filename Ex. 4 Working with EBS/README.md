# Lab 4 – Working with Amazon Elastic Block Store (EBS)

## Author

* **Name**: Ramitha chowdary S 
* **Register Number**: 212224240130
* **Date of Submission**: 09-03-2026

---

## Objective

The objective of this experiment is to understand how Amazon Elastic Block Store (EBS) provides persistent block-level storage for EC2 instances. This lab focuses on creating and attaching an EBS volume, formatting and mounting it on an EC2 instance, storing data, and verifying data persistence after instance reboot.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* An existing EC2 instance (Amazon Linux 2 preferred)
* Basic knowledge of Linux commands

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Amazon EBS
* SSH Client (Terminal / PuTTY)

---

## Tasks Performed

### Task 1: Explore Amazon EBS

Explore the Amazon EBS service through the EC2 dashboard. Observe different volume types such as General Purpose SSD (gp2/gp3), Provisioned IOPS SSD, Throughput Optimized HDD, and Cold HDD.

---

### Task 2: Create an EBS Volume

Create a new EBS volume in the same Availability Zone as the EC2 instance. Choose an appropriate size and volume type.

---

### Task 3: Attach EBS Volume to EC2 Instance

Attach the created EBS volume to the running EC2 instance as an additional block device.

---

### Task 4: Format the EBS Volume

Connect to the EC2 instance using SSH and format the attached volume with a file system (for example, ext4).

---

### Task 5: Mount the EBS Volume

Mount the formatted volume to a directory in the EC2 instance (for example, /data or /mnt/ebs).

---

### Task 6: Store Data in EBS Volume

Create files and directories inside the mounted EBS volume and store sample data.

---

### Task 7: Verify Data Persistence

Reboot the EC2 instance and verify that the data stored in the EBS volume is still available after reboot.

---

## Workflow (Student Explanation)

**1.** First, the AWS lab was started and the EC2 console was opened. The existing EC2 instance named Lab and its Availability Zone were checked.

**2.** A new EBS volume of size 1 GiB with type General Purpose SSD (gp2) was created in the same Availability Zone and named My Volume.

**3.** The created volume was then attached to the EC2 instance using the device name /dev/sdf.

**4.** The EC2 instance was opened using EC2 Instance Connect, and a file system was created on the new volume using Linux commands.

**5.** The volume was mounted to a directory (/mnt/data-store) and a sample file was created to store some text.

**6.** A snapshot of the volume was created as a backup.

**7.** A new volume was then created from the snapshot, attached to the EC2 instance, and mounted to verify that the previously created file was successfully restored.

---

## Output Screenshots (Attach 3)

### Screenshot 1: EBS Volume Created

<img width="1650" height="774" alt="556091506-a7eafcf5-cd52-4bf6-8e92-cffad8c7440d" src="https://github.com/user-attachments/assets/ae7b74fb-7673-4a4e-b89a-21e88f8a5924" />

<img width="1639" height="754" alt="556091560-617d843b-7f1c-43ff-a774-9cb5124e8f58" src="https://github.com/user-attachments/assets/76dad3e4-2a4f-4acd-855f-f4e1f0dbc310" />

---

### Screenshot 2: EBS Volume Attached to EC2

<img width="1588" height="501" alt="556091777-bc363f53-e0b3-4e25-af01-faa35022480a" src="https://github.com/user-attachments/assets/21ea1ebd-feb9-44de-af3a-565d080bdf27" />

<img width="1622" height="698" alt="556091939-42097645-c565-4099-8956-c15c7162d826" src="https://github.com/user-attachments/assets/fe799a1f-36db-4a37-93fc-cac322cacca4" />

---

### Screenshot 3: Mounted Volume with Data

<img width="1642" height="820" alt="556092194-4e6da46c-b747-42cd-819d-b2f717c920e2" src="https://github.com/user-attachments/assets/9a965101-52d2-40d6-865c-80e9fadfe2f6" />

<img width="1619" height="860" alt="556092523-e23ac8a4-0d3f-48b2-bcd4-337c25c590b0" src="https://github.com/user-attachments/assets/1767fe0d-74ff-4627-8b69-542836f19db9" />

---

## Result / Conclusion

This experiment demonstrated how Amazon EBS provides persistent storage for EC2 instances. By creating, attaching, formatting, and mounting an EBS volume, and by verifying data after reboot, the concept of durable block storage in the cloud was clearly understood.
