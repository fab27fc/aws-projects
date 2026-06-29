# Build a Serverless Lead Capture on AWS

## Overview

This project demonstrates how to build a fully serverless lead capture application on AWS. Users can download a free eBook through a static website hosted on Amazon S3. The application securely processes customer information using Amazon API Gateway and AWS Lambda, stores contact details in Amazon DynamoDB, and sends email notifications through Amazon SES. The solution is designed to be scalable, highly available, secure, and cost-effective by using AWS managed services.

---

## Architecture Diagram

<img width="1070" height="552" alt="image" src="https://github.com/user-attachments/assets/407767aa-35a1-44f5-9a85-89d63f26947d" />

---

## Business Requirements
The customer wants to build a serverless web application that allows visitors to download a free eBook while securely collecting customer information for analytics and email notifications.

### Functional Requirements

- Build a responsive website using HTML, CSS, and JavaScript.
- Allow users to download a free eBook.
- Capture the user's contact information through a web form.
- Send an email notification whenever a new download is requested.
- Store customer information in a database for future analytics.

### Non-Functional Requirements

- Support approximately 500 active users.
- Handle 10–15 eBook downloads per day.
- Provide high performance for global users.
- Secure all communication using HTTPS.
- Use the custom domain theepicbooks.com.
- Use a scalable and highly available serverless architecture.

---

## AWS Services Used

| AWS Service | Purpose |
|-------------|---------|
| Amazon Route 53 | Resolves the custom domain name and routes user requests. |
| Amazon CloudFront | Delivers website content globally with low latency and caching. |
| Amazon S3 | Hosts the static website files. |
| AWS Certificate Manager | Provides SSL/TLS certificates for HTTPS. |
| Amazon API Gateway | Exposes a secure REST API endpoint. |
| AWS Lambda | Processes contact form submissions and business logic. |
| Amazon DynamoDB | Stores customer contact information. |
| Amazon SES | Sends email notifications to the business owner. |
| Amazon CloudWatch | Collects logs and monitors application performance. |
| AWS IAM | Controls permissions between AWS services. |

---

## Architecture Flow

1. The user accesses the website using the custom domain.
2. Amazon Route 53 resolves the domain name.
3. Amazon CloudFront serves the static website hosted on Amazon S3.
4. The user submits the contact form.
5. Amazon API Gateway receives the HTTP request.
6. AWS Lambda validates and processes the submitted data.
7. Customer information is stored in Amazon DynamoDB.
8. AWS Lambda sends an email notification through Amazon SES.
9. Amazon CloudWatch records logs and metrics.
10. The business owner receives the email notification.

---

## Deployment Steps







### Prerequisites

- AWS Account
- AWS CLI
- Git
- Visual Studio Code

### Deployment

1. Create an Amazon S3 bucket.
2. Upload the website files.
3. Enable static website hosting.
4. Request an SSL/TLS certificate using AWS Certificate Manager.
5. Configure Amazon CloudFront.
6. Configure Amazon Route 53.
7. Configure Amazon SES.
8. Create the IAM policy and IAM role for AWS Lambda.
9. Create the AWS Lambda function.
10. Create and configure the Amazon API Gateway REST API.
11. Enable CORS for the API.
12. Create the Amazon DynamoDB table.
13. Update the Lambda function to store data in DynamoDB.
14. Update the website to call the API endpoint.
15. Upload the updated website to Amazon S3.
16. Test the application.
17. Verify logs in Amazon CloudWatch.

---

## Project Structure

```text
project-name/

├── frontend/
│   ├── index.html
│   ├── style.css
│   └── app.js
│
├── lambda/
│   └── index.py
│
├── images/
│   └── architecture.png
│
├── README.md
└── .gitignore
```

---

## Security

- HTTPS using AWS Certificate Manager.
- Least privilege IAM roles.
- Bucket Policy.
- CORS.
- API Gateway permissions.

---

## Cost Optimization

- Serverless Architecture.
- Pay-as-you-go pricing.
- CloudFront caching.
- Fully managed AWS services.

---

## Lessons Learned

- Built a complete serverless application using AWS managed services.
- Integrated multiple AWS services into a single workflow.
- Learned how Amazon API Gateway integrates with AWS Lambda.
- Learned how to store structured data in Amazon DynamoDB.
- Implemented monitoring using Amazon CloudWatch.
- Improved understanding of event-driven serverless architectures.
- Configured HTTPS using AWS Certificate Manager and Amazon CloudFront.
- Secured AWS resources using IAM roles and policies.

---

## Future Improvements

- Provision the infrastructure using Terraform.
- Implement a CI/CD pipeline with GitHub Actions.
- Protect the application using AWS WAF.
- Enable AWS X-Ray for distributed tracing.
- Implement user authentication using Amazon Cognito.
- Add Amazon CloudWatch alarms for proactive monitoring.
- Configure custom error handling and retry mechanisms.
- Add automated testing for the API and Lambda functions.

---

## Author

**Fabian C.**

AWS Solutions Architect Associate Candidate

- GitHub: https://github.com/fab27fc
