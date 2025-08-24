# CDevOps Movie App 🎬

CDevOps Movie App is a **Django-based web application** built as part of a DevOps/DevSecOps pipeline project. It demonstrates how to integrate modern CI/CD practices with **automated testing, code quality analysis, and secure deployment**.

---

##  Features

* 🎥 **Movie Booking System** – Browse and book movies.
* 👤 **User Authentication** – Secure login/logout with Django.
* 🛡 **DevSecOps Integration**:

  * **PyTest** – Automated unit and integration tests.
  * **Pylint** – Static code analysis for Python best practices.
  * **SonarQube** – Security & code quality scanning.
  * **AWS CodeDeploy** – Automated deployment pipeline.
* 🗄 **Database** – SQLite (local dev), PostgreSQL (production-ready).
* 📦 **Container/Cloud Ready** – Can be deployed to AWS, Docker, or Kubernetes.

---

## 🛠 Tech Stack

* **Framework**: Django (Python)
* **Database**: SQLite (default), PostgreSQL (production)
* **Testing**: PyTest, unittest
* **CI/CD**: Jenkins, AWS CodeDeploy
* **Quality & Security**: SonarQube, Pylint
* **Version Control**: Git & GitHub

---

## 📂 Project Structure

```
Cdevopsmovieapp/
│── movie_booking/         # Django app with settings, urls, views
│── templates/             # HTML templates (movie list, booking, etc.)
│── static/                # CSS, JS, images
│── manage.py              # Django entry point
│── requirements.txt       # Python dependencies
│── pytest.ini             # PyTest config
│── buildspec-pylint.yml   # AWS CI config for Pylint
│── buildspec-sonar.yml    # AWS CI config for SonarQube
│── appspec.yml            # AWS CodeDeploy config
│── db.sqlite3             # Local DB (ignored in production)
└── README.md              # Documentation
```

---

## ⚡ Getting Started

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/adithyanaren/Cdevopsmovieapp.git
cd Cdevopsmovieapp
```

### 2️⃣ Create Virtual Environment

```bash
python -m venv .venv
source .venv/bin/activate   # Mac/Linux
.venv\Scripts\activate      # Windows
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 4️⃣ Run Migrations

```bash
python manage.py migrate
```

### 5️⃣ Start Development Server

```bash
python manage.py runserver
```

Visit 👉 `http://127.0.0.1:8000`

---

##  Testing & Quality

Run **PyTest**:

```bash
pytest
```

Run **Pylint**:

```bash
pylint movie_booking
```

Run **SonarQube Scan** (via Jenkins/CLI):

```bash
sonar-scanner
```

---

##  Deployment

### Deploy with AWS CodeDeploy

* Uses `appspec.yml` and `buildspec-*.yml` for pipeline automation.
* Jenkins triggers builds on push to `main`.
* SonarQube & Pylint integrated before deployment.
* CodeDeploy handles release to EC2/AWS environment.

### Docker/Kubernetes (Optional)

```bash
docker build -t cdevops-movieapp .
docker run -p 8000:8000 cdevops-movieapp
```

---

##  Contribution

1. Fork the repo
2. Create feature branch (`git checkout -b feature-name`)
3. Commit changes (`git commit -m "Added feature"`)
4. Push branch (`git push origin feature-name`)
5. Open Pull Request

---

## 📜 License

This project is licensed under the **MIT License**.

---

## 👨‍💻 Author

* **Adithya Naren**
  🌐 [LinkedIn](https://www.linkedin.com/in/adhithya0616/) | 💻 [GitHub](https://github.com/adithyanaren)

---

✨ *CDevOps Movie App – where DevSecOps meets Django.*
