# Flask CI/CD Pipeline using Jenkins and GitHub Actions

## Project Overview

This project demonstrates the implementation of Continuous Integration and Continuous Deployment (CI/CD) for a simple Flask application using:

- Jenkins Pipeline
- GitHub Actions
- GitHub Repository
- Python (Flask)
- Pytest

The pipeline automatically installs dependencies, runs unit tests, and simulates deployment whenever code changes are pushed.

---

## Repository

GitHub Repository:

https://github.com/sanjuwatson-del/flask-cicd-jenkins

---

## Project Structure

```
flask-cicd-jenkins/
│
├── app.py
├── requirements.txt
├── Jenkinsfile
├── README.md
├── pytest.ini
├── .gitignore
├── tests/
│   └── test_app.py
└── .github/
    └── workflows/
        └── python-app.yml
```

---

## Technologies Used

- Python 3.x
- Flask
- Pytest
- Jenkins
- Git
- GitHub
- GitHub Actions

---

## Prerequisites

Before running this project, install:

- Python 3
- Git
- Jenkins
- Java 17 or later
- Homebrew (macOS)

Verify installations:

```bash
python3 --version
git --version
java -version
```

---

## Clone Repository

```bash
git clone https://github.com/sanjuwatson-del/flask-cicd-jenkins.git

cd flask-cicd-jenkins
```

---

## Create Virtual Environment

```bash
python3 -m venv venv
```

Activate the environment

macOS/Linux

```bash
source venv/bin/activate
```

Windows

```cmd
venv\Scripts\activate
```

---

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Run the Flask Application

```bash
python app.py
```

Application URL

```
http://localhost:5001
```

---

## Run Unit Tests

```bash
pytest
```

Expected Output

```
1 passed
```

---

# Jenkins Pipeline

The Jenkins pipeline performs the following stages.

### Build

- Creates Python virtual environment
- Installs required packages

### Test

- Executes unit tests using pytest

### Deploy

- Simulates deployment to a staging environment

---

## Jenkins Pipeline Flow

```
GitHub Push
      │
      ▼
 Jenkins Job
      │
      ▼
 Checkout Code
      │
      ▼
 Build
      │
      ▼
 Test
      │
      ▼
 Deploy
      │
      ▼
 Success / Failure Notification
```

---

## Jenkins Setup

1. Install Jenkins

2. Install required plugins

- Git
- Pipeline
- GitHub
- Email Extension Plugin

3. Configure

- Git
- Python
- Java

4. Create Pipeline Job

5. Connect GitHub Repository

6. Build Automatically

---

## GitHub Actions Workflow

Workflow file location

```
.github/workflows/python-app.yml
```

Workflow stages

- Checkout Repository
- Setup Python
- Install Dependencies
- Run Tests
- Build Application
- Deploy to Staging
- Deploy to Production (Release Tags)

---

## GitHub Secrets

The following secrets can be configured under

```
Repository
→ Settings
→ Secrets and Variables
→ Actions
```

Example

```
DEPLOY_KEY
API_TOKEN
STAGING_HOST
```

---

## Notifications

Jenkins Email Extension Plugin can be configured to send notifications on

- Build Success
- Build Failure

---

## Screenshots Included

- Jenkins Dashboard
- Jenkins Build Console
- Successful Pipeline Execution
- GitHub Actions Workflow
- GitHub Repository
- 
![Successful Build](screenshot/succesfull%20build.png)
![Jenkins Pipeline Stage View](screenshot/pipeline%20stage%20view.png)
![GitHub Webhook Configured](screenshot/Github%20webook%20configured.png)
![Jenkins Build Console Output](screenshot/build%20Console%20output.png)
