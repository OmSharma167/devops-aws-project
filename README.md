# devops-aws-project
🚀 End-to-End DevOps project implementing CI/CD on AWS using Terraform, Ansible, Docker, Jenkins, Kubernetes (EKS), and Amazon ECR.


# devops-aws-project
🚀 End-to-End DevOps project implementing CI/CD on AWS using Terraform, Ansible, Docker, Jenkins, Kubernetes (EKS), and Amazon ECR.



Repository name
  
devops-aws-project

Description
  
🚀 End-to-End DevOps CI/CD project on AWS using Terraform, Ansible, Docker, Jenkins, Kubernetes (EKS), Amazon ECR, and GitHub.

Recommended topics
  
devops
aws
docker
kubernetes
terraform
ansible
jenkins
cicd
eks
ecr
github

1. Create repository on GitHub

Go to:

  
https://github.com/new


Set:

  
Repository name: devops-aws-project
Visibility: Public


I recommend Public because you can later show this project to recruiters/interviewers.

Since you already have Git configured on your local Windows/VS Code system, you do not need to install Git again just for this step.

2. Create Project Folder

In VS Code PowerShell:

PowerShell
cd C:\Users\Om.3.Sharma\vscode
 
mkdir devops-aws-project
cd devops-aws-project
 


Open the folder in VS Code:

PowerShell
code .

3. Create Repository Structure

Your project should eventually look like:

  
devops-aws-project/
│
├── app/
│ └── index.html
│
├── terraform/
│ ├── provider.tf
│ ├── variables.tf
│ ├── vpc.tf
│ ├── ec2.tf
│ ├── ecr.tf
│ ├── eks.tf
│ ├── iam.tf
│ └── outputs.tf
│
├── ansible/
│ ├── inventory.ini
│ ├── jenkins.yml
│ └── tools.yml
│
├── kubernetes/
│ ├── deployment.yaml
│ └── service.yaml
│
├── Dockerfile
├── Jenkinsfile
├── .gitignore
└── README.md


Important: Don't create all complicated Terraform/Ansible/Jenkins code immediately. Build the project phase by phase.

4. First Create Application

Create:

  
app/index.html
code



5. Create Dockerfile

In the root directory create:

  
Dockerfile


Add:

Dockerfile
FROM nginx:alpine
 
COPY app/index.html /usr/share/nginx/html/index.html
 
EXPOSE 80


Your structure is now:

  
devops-aws-project/
│
├── app/
│ └── index.html
│
└── Dockerfile
Show more lines
6. Create .gitignore

Create:

  
.gitignore


Add:

.ignore
# Terraform
.terraform/
*.tfstate
*.tfstate.*
.terraform.lock.hcl
crash.log
 
# Terraform variable files that may contain secrets
*.tfvars
*.tfvars.json
 
# SSH keys
*.pem
*.key
 
# Environment variables
.env
.env.*
 
# VS Code
.vscode/
 
# OS files
.DS_Store
Thumbs.db
 
# Logs
*.log
 
# Ansible
*.retry
Show more lines

This is very important because you should never push AWS credentials, SSH private keys, passwords, or other secrets to GitHub.

7. Create README.md

Create:

  
REA*ME.md


Use this:

Markdown
* 🚀 End-to-End DevOps Project on A*S
 
This project demonstrates an au*omated CI/CD pipeline for deployin* a containerized web application t* AWS EKS.
 
## 🛠 Technologies Used*
- Git
- GitHub
- AWS
- Docker
- A*azon ECR
- Kubernetes
- Amazon EKS*- Terraform
- Ansible
- Jenkins
- *I/CD
 
## 🏗 Architecture
 
Develope*
|
| git push
v
GitHub* |
| Webhook
v
Jenkins
* |
+--> Build Application
* |
+--> Build Docker Image
*|
+--> Push Image to Amazon EC*
|
+--> Deploy to Amazon E*S
|
v
Kubernetes Deploymen*
|
v
Kubernetes Service
* |
v
AWS Load Balancer
|
* v
User
 
## 📁 Project Structure
*devops-aws-project/
│
├── app/
│ *└── index.html
│
├── terraform/
│
*── ansible/
│
├── kubernetes/
│
├─* Dockerfile
├── Jenkinsfile
├── .g*tignore
└── README.md
 
## 🔄 CI/CD*Workflow
 
1. Developer updates app*ication code
2. Code is pushed to *itHub
3. GitHub triggers Jenkins
4* Jenkins checks out the source cod*
5. Jenkins builds the Docker imag*
6. Docker image is pushed to Amaz*n ECR
7. Jenkins deploys the image*to AWS EKS
8. Kubernetes performs *he deployment
9. Application is ex*osed through a LoadBalancer
 
## 🏗*Infrastructure as Code
 
Terraform *s used to provision AWS resources *uch as:
 
- VPC
- Subnets
- Securit* Groups
- IAM Roles
- EC2
- Amazon*ECR
- Amazon EKS
 
## ⚙️ Configurat*on Management
 
Ansible is used to *onfigure the Jenkins EC2 server an* install:
 
- Java
- Jenkins
- Dock*r
- Git
- AWS CLI
- kubectl
- Terr*form
 
## 🐳 Docker
 
The applicatio* is containerized using Docker and*Nginx.
 
Build:
 
docker build -t de*ops-app .
 
Run:
 
docker run -d -p *080:80 devops-app
 
## ☸️ Kubernete*
 
Kubernetes manifests are used to*create:
 
- Deployment
- Pods
- Ser*ice
- Load Balancer
 
## 👨‍💻 Auth*r
 
**Om Sharma**
 
Cloud | DevOps |*AWS | Docker | Kubernetes | Terraf*rm | Ansible | Jenkins
Show more lines
8. Initialize Git

From your project folder:

PowerShell
git init
*


Check:

PowerShell
git stat*s


Add the files:

PowerShell
git add .


Commit:

PowerShell
git commit -m "Initial DevOps*project setup"


Set your branch:

PowerShell
git branch -M mai*

9. Connect Your Local Project to GitHub

Suppose your GitHub username is:

  
YOUR_USE*NAME


Run:

PowerShell
git *emote add origin https://github.co*/YOUR_USERNAME/devops-aws-project.*it


Check:

PowerShell
git *emote -v


You should see:

  
origin https://github.com/YOU*_USERNAME/devops-aws-project.git (*etch)
origin https://github.com/Y*UR_USERNAME/devops-aws-project.git*(push)
Show more lines
10. Push to GitHub

Run:

PowerShell
git push -* origin main


Then refresh your GitHub repository.

You should see:

  
devops-aws-project
│
├─* app
│ └── index.html
│
├── .git*gnore
├── Dockerfile
└── README.md*
Show more lines
11. Your Development Workflow

From this point onward, whenever you modify your project:

PowerShell
git status


Then:

PowerShell
git add .


Commit:

PowerShell
git commit -m "Upd*te application"


Push:

PowerShell
git push


Later, the same git push will automatically trigger your Jenkins pipeline through the GitHub webhook:

  
You / VS Code
│
│ git push
▼
GitHub
│
│ Webhook
▼
Jenkins
│
├── Checkout
├── Test
├── Docker Build
├── Push to ECR
└── Deploy
│
▼
AWS EKS
│
▼
Kubernetes
│
▼
Load Balancer
│
▼
User

⚠️ One important point for your current situation

Because Docker Desktop is not working on your company laptop due to virtualization being unavailable, don't get stuck trying to run:

PowerShell
docker build -t devops-app .


locally.

Your practical route can be:

  
Windows Laptop
│
├── VS Code
└── Git
│
│ git push
▼
GitHub
│
▼
AWS EC2 Linux
│
├── Git
├── Docker
├── Terraform
├── Ansible
├── Jenkins
├── AWS CLI
└── kubectl


And yes, Git needs to be installed on the EC2 machine if you want that EC2 machine itself to clone/pull your GitHub repository. Your local Git installation does not automatically make Git available on EC2.

Your immediate next step

For now, complete only:

  
✅ GitHub repository
✅ app/index.html
✅ Dockerfile
✅ .gitignore
✅ README.md
✅ git add
✅ git commit
✅ git push


Then move to Activity 2: launch an Ubuntu EC2 instance, install Git + Docker there, clone this GitHub repository, build the image, run the container, and access the website using the EC2 public IP.
