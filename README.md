# End-to-End-Web-App-Hosting-on-AWS-Lift-Shift-Approach-
This project demonstrates the Lift &amp; Shift deployment of a web application on AWS using key services like EC2, Security Groups, Route 53, Load Balancer, and Auto Scaling Group. It provides a step-by-step setup to host, secure, and scale a web app in the AWS cloud.

Flow of Execution : 

Follow the steps below to deploy and configure the application infrastructure on AWS:

1. Login to AWS Account
Access the AWS Management Console using your credentials.

2. Create Key Pairs
Generate a key pair to securely access EC2 instances.

3. Create Security Groups
Set up security groups with appropriate inbound and outbound rules (e.g., allowing SSH, HTTP, HTTPS).

4. Launch EC2 Instances with User Data
Deploy EC2 instances using user data scripts (e.g., Bash scripts for initial setup and configuration).

5. Update IP to Name Mapping in Route 53
Use AWS Route 53 to map your instance IP to a domain/subdomain name.

6. Build Application from Source Code
Compile or package the application using your build tool (e.g., Maven, Gradle).

7. Upload Artifact to S3 Bucket
Upload the built application (e.g., WAR/JAR files) to an Amazon S3 bucket.

8. Download Artifact on Tomcat EC2 Instance
Pull the application artifact from S3 onto the Tomcat EC2 instance for deployment.

9. Set Up Elastic Load Balancer (ELB) with HTTPS
Configure an ELB with an HTTPS listener using an SSL certificate from AWS Certificate Manager.

10. Map ELB Endpoint to Website Name in GoDaddy DNS
Update DNS records in your GoDaddy account to point your domain name to the ELB endpoint.

11. Verify Deployment
Check if the application is accessible through the browser and functioning as expected.

12. Configure Auto Scaling Group for Tomcat Instances
Set up an Auto Scaling Group to manage load and ensure high availability of Tomcat instances.