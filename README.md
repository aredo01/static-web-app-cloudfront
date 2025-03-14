# Kittens Carousel Static Website Deployed on AWS CloudFront, S3, and Route 53 Using CloudFormation 🐱🌐

## Overview 🚀

The **Kittens Carousel** is a static web application deployed on AWS. The application is hosted on **Amazon S3**, distributed via **CloudFront**, and mapped to a custom domain using **Route 53**. The entire deployment process is automated using **AWS CloudFormation**.

## Problem Statement 💡

![Project_006](Project_006.png)

Your company has launched a new web application designed to attract pet lovers 🐾. As part of the project, you've successfully tested the design and functionality on an EC2 instance. Now, the next step is to deploy the app as a static webpage.

The development team has prepared the **Kittens Carousel** application, and the necessary files are pushed to a GitHub repository.

Your task is to deploy this static web page into a production environment with the following requirements:

### Requirements 📝

1. **Index Page**: Ensure the `index.html` is the default page when the web app is accessed 🌍.
   
2. **AWS S3**: The web application must be deployed on **Amazon S3** as a static website 🏠.
   
3. **Domain Name Setup**: The application should be served through a custom domain (e.g., `kittens.clarusway.us`) using **AWS CloudFront** and **Route 53**. You will use **CloudFormation** to configure the resources.

4. **CloudFormation Template**: You need to create a CloudFormation template with the following configurations:

   - **Input Parameters**:
     - DNS name of an existing **Route 53** hosted zone (e.g., `clarusway.us`).
     - The full domain name for the web application (e.g., `kittens.clarusway.us`).
   
   - **S3 Bucket Configuration**: The web files must be served from an S3 bucket configured as a static website host, ensuring the content is publicly accessible 🌐.
   
   - **CloudFront Configuration**: Set up a **CloudFront** distribution with the following:
     - CloudFront should be associated with the full domain name of the application 🔗.
     - Communication between CloudFront and S3 must be secure 🔒.
     - The default page for CloudFront should be `index.html` 🖥️.
     - Use HTTP/2.
     - Cache behavior should allow `GET` and `HEAD` methods, without forwarding cookies 🍪.
     - All requests should be redirected to HTTPS 🔑.
     - Use an ACM certificate for securing connections 🔐.

   - **Route 53 Record Set**: A Route 53 record set should point to the CloudFront distribution 🌟.

   - **Outputs**:
     - Full domain name of the **Kittens Carousel** web application 🏷️.
     - Endpoint of the **CloudFront** distribution 🌍.
     - Name of the **S3** bucket hosting the website 🏠.

5. **File Upload**: The application files must be uploaded to the S3 bucket from a local Git repository using AWS CLI commands 💻.

## Project Structure 📂

```text
006-kittens-carousel-static-web-s3-cf (folder)
|
|----readme.md              # Project definition and instructions 📄
|----cfn-template.yml       # CloudFormation template (to be delivered by students) 📜
|----upload-script.sh       # Script to upload website content to S3 (to be delivered by students) 📤
|----static-web
        |----index.html     # Main HTML file 🖥️
        |----cat0.jpg       # Image file 🐱
        |----cat1.jpg       # Image file 🐱
        |----cat2.jpg       # Image file 🐱

Expected Outcome 🎯
Skills Covered 🔧:
Static Website Deployment on AWS 🌐.
Bash Scripting for automation 📝.
AWS S3 for static web hosting 🏠.
AWS CloudFront for content delivery 🚀.
AWS Certificate Manager for secure connections 🔒.
AWS Route 53 for DNS management 🌍.
AWS CloudFormation for infrastructure as code 📦.
Git & GitHub for version control 🗂️.
Learning Outcomes 🎓:
By the end of this project, students will be able to:

Demonstrate bash scripting skills to upload application files to an S3 bucket using AWS CLI 🖥️.
Configure S3 buckets, ACM certificates, CloudFront distributions, and Route 53 record sets through CloudFormation 🔧.
Write a CloudFormation template to manage AWS resources 📜.
Launch AWS infrastructure stacks using CloudFormation 🚀.
Use Git for version control and interact with GitHub repositories 📍.
Solution Steps 🛠️
Step 1: Clone or download the project definition from the Clarusway GitHub repository 🧑‍💻.

Step 2: Create a local folder to store the project files 🗂️.

Step 3: Write the CloudFormation template to deploy the application 📜.

Step 4: Deploy the application using the CloudFormation template 🚀.

Step 5: Upload the application files to the S3 bucket using AWS CLI from your local Git repository 💻.

Additional Notes ⚙️
Customize the index.html by replacing student_name with your name ✍️.
Optional: You may upload objects to S3 using CloudFormation if desired 🎉.

## Resources

- [AWS Cloudformation User Guide](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/Welcome.html)

- [AWS CLI Command Reference](https://docs.aws.amazon.com/cli/latest/index.html)
🔗 **GitHub Repo:[ https://github.com/aredo01/static-web-app-cloudfront.git] 🚀
