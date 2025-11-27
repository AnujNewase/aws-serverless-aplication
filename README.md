AWS Serverless Application

This project is a fully serverless web application built using AWS services such as S3, Lambda, API Gateway, DynamoDB and CloudFront. It allows users to save and retrieve student details through a simple web interface.

Features

Serverless architecture with AWS Lambda functions
RESTful API created using API Gateway
Data storage using DynamoDB
Static website hosting through S3
Global content delivery and HTTPS support via CloudFront
AJAX-based frontend for saving and viewing student records

Technologies Used

AWS S3
AWS Lambda (Python)
AWS API Gateway
AWS DynamoDB
AWS CloudFront
HTML, CSS, JavaScript, jQuery


How It Works
1. The frontend website is hosted on an S3 bucket.

2. CloudFront distributes the website globally and serves it over HTTPS.

3. When the user submits student data, an AJAX POST request hits the API Gateway endpoint.

4. API Gateway triggers a Lambda function that inserts the record into DynamoDB.

5. For viewing records, a GET request calls another Lambda function that scans the table and returns all students.



Lambda Functions

getStudent
Retrieves all student records from DynamoDB.

insertStudentData
Inserts a new student record into DynamoDB using values received from the API.


API Endpoints

POST /
Saves student data.

GET /
Retrieves all stored student records.
