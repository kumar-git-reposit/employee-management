# 📋 Employee Management System

## 🧩 What It Does
This is a full-stack web application that allows users to:
- Submit employee details via a web form
- Store employee data securely in AWS DynamoDB
- Upload documents (optional) to AWS S3
- Trigger backend logic using AWS Lambda
- Host the frontend on AWS Amplify for public access

## ⚙️ How It Works

### Frontend
- A simple HTML form (`index.html`) collects employee data
- JavaScript captures form submission and sends data to an API Gateway endpoint

### Backend
- **API Gateway** receives HTTP POST requests
- **Lambda Function** processes the request and stores data in **DynamoDB**
- (Optional) Lambda can also upload files to **S3** if document handling is added

### Hosting
- The frontend is deployed using **AWS Amplify**, connected to a GitHub repo
- Amplify auto-builds and hosts the site whenever code is pushed

## 🛠️ Technologies Used

| Layer       | Technology        |
|-------------|-------------------|
| Frontend    | HTML, JavaScript  |
| Backend     | AWS Lambda        |
| API         | AWS API Gateway   |
| Database    | AWS DynamoDB      |
| File Storage| AWS S3 (optional) |
| Hosting     | AWS Amplify       |
| Versioning  | Git + GitHub      |

## 🚀 How to Deploy or Test

### 1. Frontend Setup
- Create `index.html` with form and JavaScript
- Push to GitHub repo (`employee-management`)

### 2. Amplify Hosting
- Go to AWS Amplify Console
- Connect GitHub repo and deploy the `main` branch
- Get live URL to access the form

### 3. Backend Setup
- Create DynamoDB table for employee data
- Create Lambda function to handle POST requests
- Set up API Gateway to trigger Lambda
- (Optional) Configure S3 bucket for document uploads

### 4. Connect Frontend to Backend
- In `index.html`, update the `fetch()` URL to your API Gateway endpoint

### 5. Test the App
- Visit Amplify URL
- Fill out and submit the form
- Check DynamoDB for stored data
- Monitor Lambda logs in CloudWatch


---

