<h1 align="center"> Python Flask Application Deployment on AWS EC2</h1>


#  Introduction

This project demonstrates how to deploy a Python Flask application on an AWS EC2 instance using Amazon Linux, GitHub, Python Virtual Environment, and Gunicorn.

---

#  Table of Contents

- Introduction
- Technologies Used
- Architecture
- Project Structure
- Deployment Steps
- Screenshots
- Features
- Knowledge Gained
- Future Improvements
- Author

---

#  Technologies Used

| Technology | Purpose |
|------------|----------|
| AWS EC2 | Cloud Server |
| Amazon Linux | Operating System |
| Python 3 | Programming Language |
| Flask | Web Framework |
| Git | Version Control |
| GitHub | Source Code Hosting |
| Gunicorn | WSGI Server |

---

#  Architecture Diagram

![](/images/Screenshot%202026-08-07%20142717.png)
---

#  Project Structure

```text
pythonapp/
├── app.py
├── requirements.txt
├── screenshots/
├── README.md
└── myenv/
```

---

#  Deployment Steps

## 1. Launch EC2 Instance

Open AWS Console → Launch Amazon Linux EC2

Security Group:
- Port 22 (SSH)
- Port 5000 (Flask)

## 2. Connect EC2

```bash
ssh -i my-key.pem ec2-user@your-public-ip
```

## 3. Install Packages

```bash
sudo yum update -y
sudo yum install python3-pip git -y
```

## 4. Clone Repository

```bash
git clone https://github.com/iamtruptimane/pythonapp.git
cd pythonapp
```

## 5. Create Virtual Environment

```bash
python3 -m venv myenv
source myenv/bin/activate
```

## 6. Install Dependencies

```bash
pip install -r requirements.txt
```

## 7. Run Application

```bash
python3 app.py
```

## 8. Run with Gunicorn

```bash
gunicorn app:app --bind 0.0.0.0:5000
```

---

#  Screenshots

## EC2 Instance Creation
Add screenshot here:

```text
screenshots/ec2-instance.png
```

## Security Group Configuration

```text
screenshots/security-group.png
```

## Flask Application Output

```text
screenshots/flask-output.png
```

---

#  Features

- AWS EC2 Deployment
- Flask Web Hosting
- GitHub Integration
- Linux Server Management
- Python Virtual Environment
- Gunicorn Support

---

#  Knowledge Gained

- EC2 Instance Management
- Linux Commands
- Git & GitHub
- Flask Deployment
- Python Environment Management
- Cloud Computing Basics

---

#  Future Improvements

- Nginx Reverse Proxy
- Custom Domain
- HTTPS SSL Certificate
- CI/CD Pipeline with GitHub Actions
- Docker Containerization

---

#  Author

**Prafulla Patil**

Cloud & DevOps Enthusiast 

---
