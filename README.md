# AWS S3 Static Website Deployment Exercise

## Overview
In this exercise, you will deploy a progress tracking webpage using AWS S3 and CloudFormation. This hands-on activity will help you understand cloud resource deployment and static website hosting.

## Learning Objectives
- Deploy AWS resources using CloudFormation
- Configure S3 static website hosting
- Understand cloud infrastructure automation
- Practice problem-solving in a cloud environment

## Prerequisites
- AWS account with administrative access
- AWS CLI installed and configured
- Basic understanding of:
  - AWS Services (S3, CloudFormation)
  - JSON format
  - Web technologies (HTML, CSS, JavaScript)
  - Command line interface

## Required Resources
- Text editor
- Web browser
- Terminal/Command prompt
- AWS account credentials

## Exercise Steps

### 1. Template Preparation
Create a new file named `website-stack.json` with the CloudFormation stored in this repository

### 2. Deployment Process

#### Using AWS Console
1. Access AWS Management Console
2. Navigate to CloudFormation
3. Create new stack:
   - Click "Create stack"
   - Select "With new resources (standard)"
   - Upload template file
   - Follow configuration wizard

#### Using AWS CLI
```bash
aws cloudformation create-stack \
  --stack-name progress-tracker-website \
  --template-body file://website-stack.json \
  --capabilities CAPABILITY_IAM
```

### 3. Verification Steps

#### Stack Deployment
- Monitor stack creation progress
- Check for successful completion
- Review any error messages
- Verify resource creation

#### Website Testing
1. Locate website URL in stack outputs
2. Test website functionality:
   - Progress bar animation
   - Timer countdown
   - Status message updates
   - Responsive design
   - Panic mode activation

### 4. Documentation Requirements

#### Deployment Documentation
- Screenshots of:
  - Successful stack creation
  - Resource configuration
  - Website functionality
- Website URL
- Any error messages encountered

#### Technical Analysis
- Deployment process explanation
- Challenge resolution steps
- Resource configuration details
- Security considerations

### 5. Clean Up Procedure

#### Using AWS Console
1. Navigate to CloudFormation
2. Select stack
3. Choose Delete
4. Confirm deletion

#### Using AWS CLI
```bash
aws cloudformation delete-stack \
  --stack-name progress-tracker-website
```

## Common Issues and Solutions

### Deployment Failures
- **Issue**: Permission denied
  - **Solution**: Verify AWS credentials and IAM permissions

- **Issue**: Stack creation fails
  - **Solution**: Check CloudFormation events for specific error messages

- **Issue**: Website not accessible
  - **Solution**: Verify S3 bucket permissions and policy configuration

## Best Practices

### Security
- Use principle of least privilege
- Implement proper bucket policies
- Regular security audits
- Clean up unused resources

### Performance
- Optimize website assets
- Consider regional deployment
- Monitor resource usage
- Implement caching strategies

## Extended Learning Opportunities

### Additional Features
- Custom domain implementation
- SSL/TLS configuration
- Content delivery network
- Monitoring and analytics

### Advanced Topics
- Infrastructure as Code
- CI/CD integration
- Cost optimization
- High availability design

## Submission Guidelines

### Required Elements
1. Deployment documentation
2. Working website URL
3. Technical analysis report
4. Clean-up confirmation


## Support Resources
- AWS Documentation
- CloudFormation User Guide
- S3 Website Hosting Guide
- AWS CLI Reference

## Notes
- Keep resources running only as needed
- Document all steps carefully
- Follow AWS best practices
