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
* Document
### Key Features:
* Build a small AWS environment
* Create risky IAM permissions
* Perform suspicious actions
* Capture logs
* Write detection logic
* Automate response

## Tool Requirements
*AWS account
* VPC
* EC2 instance
* S3 bucket
* IAM users
* CloudTrail
