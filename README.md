# 📌 Smart-Resume-Upload-Auto-Reply-System
Serverless AWS Project

## 📖 Overview
The Smart Resume Upload & Auto-Reply System is a beginner-friendly, serverless AWS project designed to automate resume submission and acknowledgment.

When a user uploads a resume (PDF) to an AWS S3 bucket, an AWS Lambda function is automatically triggered. This function sends a confirmation email to the applicant using Amazon SES. The entire workflow is event-driven and does not require any servers.

This project demonstrates real-world cloud automation commonly used in recruitment platforms.

## 🧰Tech Stack
Cloud Platform
- Cloud Platform
  
AWS Services Used
- Amazon S3 – Resume storage
- AWS Lambda – Backend processing (Python)
- Amazon SES – Email notification service
- IAM – Permissions & security
- CloudWatch – Logging & monitoring
  
Language
- Python 3.10

## 🏗️ Architecture and Workflow
1️⃣ Create S3 Bucket

  Service: Amazon S3

  Bucket Name: pavithra-resume

  Region: Asia Pacific (Mumbai)

  Disable Block Public Access
  
<img width="1256" height="446" alt="s3 bucket" src="https://github.com/user-attachments/assets/de2019f4-7e42-4452-8b57-a22628fff001" />

Create folder: resumes/
<img width="1600" height="426" alt="inside s3- resumes" src="https://github.com/user-attachments/assets/84eb80a2-43c3-4228-83a6-9e255ab55035" />

Uploaded resume: PAVITHRA K_RESUME
<img width="1589" height="441" alt="uploaded resume" src="https://github.com/user-attachments/assets/f4ec90e5-9a0f-4e90-bfda-7880bd61e29e" />

2️⃣ Create Lambda Function

Service: AWS Lambda

Function name: ResumeAutoReply

Runtime: Python 3.10

<img width="1602" height="467" alt="lambda" src="https://github.com/user-attachments/assets/a960f95c-dd16-4806-a8b0-b71eb52b0388" />

<img width="1266" height="464" alt="lambda digram" src="https://github.com/user-attachments/assets/099ccc6e-4538-406f-9f37-ef743fe0cbe0" />

3️⃣IAM Permissions

Attach the following policies to Lambda role:

AmazonS3FullAccess

AmazonSESFullAccess

CloudWatchLogsFullAccess

<img width="1592" height="655" alt="IAM permissions" src="https://github.com/user-attachments/assets/211e7b62-52dd-40ed-bd4a-91a76484f2e4" />

4️⃣Configure Amazon SES

Verify your email address

Use the same AWS region (Mumbai)

<img width="1579" height="321" alt="Amazon SES" src="https://github.com/user-attachments/assets/5ac08a8f-aef3-417e-8e14-d53e50ed5988" />


5️⃣Lambda Function Code

<img width="880" height="499" alt="lambda code" src="https://github.com/user-attachments/assets/7310b92f-cda1-4e20-8d37-655681d91a25" />

6️⃣ Connect S3 to Lambda
S3 → Bucket → Properties

Event Notifications:

Prefix: resumes/

Event: Object Created

Destination: Lambda function

## ✨ Features
- 📤 Resume upload using Amazon S3
- ⚡ Automatic Lambda trigger on file upload
- 📧 Auto-reply email confirmation using SES
- ☁️ Fully serverless (no EC2 or servers)
- 🔐 Secure access using IAM roles
- 📊 Logs and monitoring via CloudWatch
- 🆓 Built using AWS Free Tier services

## 🎉 Final Output
<img width="1041" height="515" alt="project output" src="https://github.com/user-attachments/assets/f92c1c0e-81cf-4f57-aa03-935aefb9d1ff" />

✅ What Just Happened (Proof Your Project Works)
- ✔ Subject: Resume Received
- ✔ From: pavithrakalai2004@gmail.com
 via amazonses.com
- ✔ Body: “Thank you for submitting your resume…”
- ✔ Triggered automatically after upload

👉 This confirms ALL of these are working:
- S3 upload ✔
- S3 → Lambda trigger ✔
- Lambda execution ✔
- SES email sending ✔

🔥 End-to-end automation SUCCESS

❓ Why Did It Go to SPAM?
Reasons:
- New sender reputation
- Simple email content
- Sent via amazonses.com
- No custom domain / DKIM yet

🚫 This is NOT an error

🚫 This is NOT a mistake




## 📄☁️ Summary 
A beginner-friendly serverless AWS project that automates resume acknowledgments by triggering an AWS Lambda function when a resume is uploaded to an S3 bucket, which then sends a confirmation email using Amazon SES.
