---
name: AMI/Setup Issue
about: Report problems with KohaSupport AWS Marketplace AMI deployment or configuration
title: '[AMI ISSUE] '
labels: ['ami-issue', 'bug']
assignees: []
---

## Issue Description
**Provide a clear and concise description of the problem:**
<!-- What went wrong? What were you trying to do? -->



## Environment Details
**AMI Information:**
- **Tier:** <!-- Free, Basic, or Standard -->
- **Architecture:** <!-- ARM64 or x86 -->
- **Version:** <!-- e.g., v25.05.05 -->
- **AMI ID:** <!-- Found in EC2 console, starts with ami- -->

**AWS Configuration:**
- **Region:** <!-- e.g., us-east-1 -->
- **Instance Type:** <!-- e.g., t4g.medium, t3a.medium -->
- **VPC Type:** <!-- Default VPC or Custom VPC -->

**Deployment Method:**
- [ ] CloudFormation (AWS Marketplace 1-click)
- [ ] CloudFormation (custom parameters)
- [ ] Manual EC2 launch
- [ ] Other (please specify)

## Problem Category
**What area is affected?**
- [ ] CloudFormation stack deployment failure
- [ ] Instance launch issues
- [ ] S3 backup problems (Standard Tier)
- [ ] Custom domain setup (Standard Tier)
- [ ] SSL/TLS certificate issues (Standard Tier)
- [ ] Koha application errors
- [ ] Network/connectivity issues
- [ ] SSH access problems
- [ ] Performance issues
- [ ] Other (please specify)

## Steps to Reproduce
**How did you encounter this issue?**
1. 
2. 
3. 

## Expected Behavior
**What did you expect to happen?**
<!-- Describe the expected outcome -->



## Actual Behavior
**What actually happened?**
<!-- Describe what went wrong -->



## Error Messages
**Include any error messages, logs, or screenshots:**
```
<!-- Paste error messages here -->
```

**CloudFormation Events (if deployment failed):**
```
<!-- Copy relevant CloudFormation stack events -->
```

**System Logs (if accessible via SSH):**
```bash
# Koha logs
sudo tail -100 /var/log/koha/library/plack-error.log
sudo tail -100 /var/log/koha/library/plack-intranet-error.log

# Apache logs
sudo tail -100 /var/log/apache2/error.log

# S3 backup logs (Standard Tier)
sudo journalctl -u koha-s3-backup.service -n 100
```

## Troubleshooting Already Attempted
**What have you tried so far?**
- [ ] Checked CloudFormation stack events
- [ ] Verified security group settings
- [ ] Confirmed DNS configuration (if using custom domain)
- [ ] Checked AWS Systems Manager Parameter Store for credentials
- [ ] Reviewed instance system logs
- [ ] Attempted SSH access
- [ ] Verified Elastic IP association
- [ ] Other (please describe):

## Stack Outputs
**If using CloudFormation, provide the stack outputs:**
```
<!-- Copy from CloudFormation Outputs tab -->
KohaServerIPAddress: 
KohaAdminInterfaceURL: 
KohaPublicCatalogURL: 
CustomOPACURL (if applicable):
CustomStaffURL (if applicable):
```

## Additional Context
**Any other relevant information:**
<!-- Network architecture, custom configurations, timing of issue, etc. -->



**Is this blocking production use?**
- [ ] Yes - Critical
- [ ] No - Development/Testing

**When did this issue start?**
<!-- New deployment, after update, suddenly appeared, etc. -->



---
**Support Resources:**
- **Knowledge Base:** https://kohasupport.com/knowledge-base
- **Professional Support:** https://kohasupport.com/contact
- **AWS Marketplace Listing:** https://aws.amazon.com/marketplace/seller-profile\?id\=569572031893
