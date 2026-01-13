🚀 Jenkins CI/CD Demo Project
This project demonstrates a simple yet effective CI/CD pipeline using Jenkins, GitHub, Docker, and Nginx. Any change made to the HTML code is automatically built and deployed using Jenkins.

📌 Project Overview
The goal of this project is to understand how real-world CI/CD pipelines work by automating the build and deployment of a static website.

Whenever the developer updates the HTML file and pushes changes to GitHub, Jenkins:

Pulls the latest code
Builds a Docker image
Deploys the updated website automatically
🔄 Project Workflow
Code Change (GitHub) ↓ Jenkins Pipeline ↓ Docker Image Build ↓ Website Deployed (Nginx)

🛠 Tools & Technologies Used
Jenkins – CI/CD automation
GitHub – Source code management
Docker – Containerization
Nginx – Web server
HTML – Frontend
jenkins-ci-cd-demo-project/ ├── index.html ├── Dockerfile └── Jenkinsfile

🧩 File Descriptions
📄 index.html
Static HTML page
Any change in this file triggers a new Jenkins build
📄 Dockerfile
Builds a Docker image using Nginx
Copies HTML file into Nginx web directory
📄 Jenkinsfile
Defines Jenkins pipeline stages:
Clone GitHub repository
Build Docker image
Run Docker container
▶️ How to Run This Project
1️⃣ Prerequisites
Jenkins installed and running
Docker installed on Jenkins server
GitHub repository configured in Jenkins
2️⃣ Jenkins Job Setup
Create a Pipeline job in Jenkins
Select Pipeline script from SCM
Provide GitHub repository URL
Build the job
3️⃣ Access the Application
Open browser and visit:

http://:8081

🔁 Updating the Website
Edit index.html
Commit and push changes to GitHub
Trigger Jenkins build
Refresh browser to see updated content
🎯 Key Learnings
Understanding CI/CD pipeline concepts
Automating builds and deployments using Jenkins
Docker image creation and container deployment
Real-world DevOps workflow
🚀 Future Enhancements
GitHub Webhooks for auto-triggered builds
Docker image versioning
Jenkins credentials management
Kubernetes deployment
