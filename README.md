# Flask CI/CD Pipeline

A simple Flask web application demonstrating a **Continuous Integration and Continuous Deployment (CI/CD) pipeline**. The application returns a version message, making it easy to verify that new code changes are deployed successfully.

## 🚀 Project Overview

This project demonstrates how a Flask application can be integrated with an automated CI/CD workflow to streamline building, testing, and deployment.

The application exposes a simple HTTP endpoint that displays the current application version.

## 🛠️ Tech Stack

- **Python** — Application programming language
- **Flask** — Lightweight web framework
- **Git & GitHub** — Source code management
- **CI/CD Pipeline** — Automated integration and deployment

## 📁 Project Structure

```text
.
├── app.py
├── requirements.txt
└── README.md
```

*Your repository may contain additional files for your CI/CD configuration and deployment setup.*

## ⚙️ Application

The Flask application serves a message at the root endpoint:

```python
from flask import Flask

app = Flask(__name__)

@app.route("/")
def home():
    return "Version 2 CI/CD Pipeline"

if __name__ == "__main__":
    app.run(host="0.0.0.0", port=5000)
```

**Endpoint:** `/`

**Port:** `5000`

**Expected response:** `Version 2 CI/CD Pipeline`

## 💻 Run Locally

### 1. Clone the repository


### 2. Create and activate a virtual environment

```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install dependencies

Create a `requirements.txt` file containing:

```text
Flask
```

Then install the dependencies:

```bash
pip install -r requirements.txt
```

### 4. Start the application

```bash
python3 app.py
```

Open `http://localhost:5000` in your browser.

You should see:

```text
Version 2 CI/CD Pipeline
```

## 🔄 CI/CD Workflow

The project is intended to demonstrate an automated deployment workflow:

1. **Code changes:** Update the Flask application.
2. **Version control:** Commit and push changes to GitHub.
3. **Continuous Integration:** Run configured checks or tests.
4. **Continuous Deployment:** Deploy the updated application using the configured pipeline.
5. **Verification:** Access the application endpoint and confirm the new version.

The exact automation steps depend on the CI/CD platform and workflow configuration used in the repository.

## 🧪 Verify Deployment

After deploying a new version, test the endpoint:

```bash
curl http://<YOUR_SERVER_IP>:5000/
```

Expected output:

```text
Version 2 CI/CD Pipeline
```

If the response changes after a successful deployment, it confirms that the updated application version is being served.

## 🎯 Project Objectives

- Understand CI/CD fundamentals.
- Automate application integration and deployment.
- Practice version control and release workflows.
- Verify deployments through a simple HTTP endpoint.
- Reduce manual effort when releasing code changes.

## 🔮 Future Improvements

- Add automated unit tests using `pytest`.
- Add a GitHub Actions or Jenkins pipeline.
- Containerize the application using Docker.
- Deploy the container to Amazon ECR and run it on an appropriate compute platform.
- Add application health checks and deployment monitoring.

## 📄 License

This project is available for educational and learning purposes. Add a license file if you intend to distribute it under a specific open-source license.
