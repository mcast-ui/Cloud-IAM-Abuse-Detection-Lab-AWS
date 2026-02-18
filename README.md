# Cloud-IAM-Abuse-Detection-Lab-AWS
## Project Overview 
This project simulates real-world cloud attack scenarios in AWS and Azure environments. It focuses on detecting identity abuse, privilege escalation, and misconfiguration using log analysis and detection engineering techniques aligned with MITRE ATT&CK.
### Project Purpose:
* Build a fake company cloud setup that will attack and defend
* Create IAM Users and intentinal over-permission users (intentionally insecure)
* S3 Bucket that simulates company data storage (intentionally make it public)
* CloudTrail records every action in AWS
* Attack Simulation escalates IAM privilege, exposed S3 bucket
* Using detection logic, log source and alert severity
* Automation contain Bash reposnce scripts
* Create Threat Model
* Document my process
### Key Features:
* Build a small AWS environment
* Create risky IAM permissions
* Perform suspicious actions
* Capture logs
* Write detection logic
* Automate response

## Tool Requirements
* AWS account
* VPC
* EC2 instance
* S3 bucket
* IAM users
* CloudTrail

## Architecture Diagram
<img width="1137" height="689" alt="Screenshot 2026-02-13 023154" src="https://github.com/user-attachments/assets/ea9fc078-fe6d-40b3-8866-4eb2379e55f9" />

## What is a VPC?
* A Virtual Private Network is a virtual networking environment in AWS that manages everything we do with networking. Configureation of the VPC determines how we connect different pieces of our infrastructure together and how we can connect it to the internet.
* Without VPC:
  * Everything would be a shared network
  * Wouldn't be able to control isolation
* With VPC:
  * I can control who talks to what
  * Design segmentation
  * Create network boundaries

## Creating a VPC
1. Log into AWS console
2. search for VPC
3. Create VPC:
   * Choose VPC only
   * Name tag : `cloud-lab-vpc`
   * IPv4 CIDR block: `10.0.0.0/16`
   * Leave everything as default
4. Click Create VPC

### VPC details
* IPv4 CIDR block: `10.0.0.0/16` defines the total IP address space my cloud network can use
  * 65,536 possible private IP addresses
  * Full control over segmentation
 
## What is a Subnet
* As shown in my architecture diagram a subnet is a smaller section in the VPC.

### Public Subnet
* What makes this public is that it routes to the internet gateway
* Instances inside can receive public IP's
* Public subnets include:
  * Web servers
  * Load Balancers
  * Bastion Hosts
* Security risk:
  * Anything here is exposed
  * Will restrict SSH to My IP
  
### Private Subnet
* No public IP
* No internet route
* Private subnet includes internal-only systems such as:
  * Databases
  * Internal APIs
  * Backend services
* Security princinple **Zero Trust Network Access (ZTNA) Framework**:
  * Never expose what doesn't need internet access (**Network Segmentation**)
 



