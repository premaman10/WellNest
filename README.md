# 🌿 WellNest – Mental Health Self-Assessment Platform

**WellNest** is a comprehensive Django web application that helps users self-identify their mental health status and get personalized guidance, support resources, and wellness recommendations.

---

## ✨ Features

### 🌐 Public Pages
- **Home** – Welcome page with featured content and quick access to assessments  
- **About** – Information about the platform and its mission  
- **How it Works** – Step-by-step guide on using the platform  
- **Resources & Support** – Mental health resources, crisis support, and reference links  

---

### 🧠 Self-Assessment Module
- **Quick Assessment** – 5-question rapid assessment for immediate results  
- **Full Assessments** – Comprehensive questionnaires (10–20 questions) covering:
  - Mood and emotional state  
  - Sleep quality  
  - Stress levels  
  - Social interactions  
  - Energy levels  
  - Appetite and physical health  

- **Risk Level Classification**
  - Low Risk  
  - Moderate Risk  
  - High Risk  

- **Personalized Recommendations**
  - Tailored advice based on assessment results  

---

### 🔐 User Authentication
- Secure Sign Up & Login  
- Profile Management  
- Password Reset System  

---

### 📊 User Dashboard
- Assessment History  
- Progress Tracking with Charts  
- Bookmarked Resources  
- Personalized Recommendations  

---

### 🧭 Guidance System
- Risk-based mental wellness content  
- Self-care tips  
- Professional help guidelines  
- Crisis support resources  

---

### 🛠 Admin Interface
- User Management  
- Assessment Data Monitoring  
- Content Management  
- Platform Analytics  

---

### 🔒 Security & Privacy
- Django secure authentication & password hashing  
- Secure data storage and transmission  
- User consent and privacy controls  
- HTTPS-ready deployment  

---

### 📱 Responsive Design
- Mobile-first UI  
- Tailwind CSS styling  
- WCAG accessibility compliant  

---

## 🧰 Technology Stack

| Layer | Technology |
|---|---|
| Backend | Django 4.2.7, Django REST Framework |
| Frontend | HTML5, Tailwind CSS, JavaScript |
| Database | SQLite (Dev), PostgreSQL (Prod) |
| Auth | Django Built-in User System |
| API | RESTful API (Mobile-ready) |

---

## 📁 Project Structure

wellnest/
├── manage.py
├── requirements.txt
├── README.md
├── wellnest/
│ ├── init.py
│ ├── settings.py
│ ├── urls.py
│ └── wsgi.py
├── accounts/
├── assessment/
├── resources/
├── core/
└── templates/


---

## ⚙️ Installation & Setup

### ✅ Prerequisites
- Python 3.8+
- pip
- Git

---

### 🖥 Local Development Setup

#### 1️⃣ Clone Repository
```bash
git clone <repository-url>
cd wellnest
2️⃣ Create Virtual Environment
python -m venv venv
Windows:

venv\Scripts\activate
Mac/Linux:

source venv/bin/activate
3️⃣ Install Dependencies
pip install -r requirements.txt
4️⃣ Environment Variables
Create .env file:

SECRET_KEY=your-secret-key
DEBUG=True
5️⃣ Database Setup
python manage.py makemigrations
python manage.py migrate
6️⃣ Create Superuser
python manage.py createsuperuser
7️⃣ Run Server
python manage.py runserver
Access:

App → http://127.0.0.1:8000

Admin → http://127.0.0.1:8000/admin

🚀 Production Deployment
🌍 Deploy on Render
Install production dependencies:

pip install gunicorn whitenoise
Create render.yaml:

services:
  - type: web
    name: wellnest
    env: python
    buildCommand: pip install -r requirements.txt && python manage.py migrate
    startCommand: gunicorn wellnest.wsgi:application
    envVars:
      - key: SECRET_KEY
        generateValue: true
      - key: DEBUG
        value: False
☁️ Deploy on Heroku
heroku create your-app-name
heroku config:set SECRET_KEY=your-secret-key
heroku config:set DEBUG=False
heroku config:set ALLOWED_HOSTS=your-app-name.herokuapp.com
git push heroku main
heroku run python manage.py migrate
📘 API Endpoints
Method	Endpoint	Description
GET	/api/assessments/	List assessments
GET	/api/results/<id>/	Get results
POST	/api/assessments/<id>/submit/	Submit responses
🔐 Security Best Practices
CSRF Protection

XSS Protection Headers

Secure Sessions

API Rate Limiting

🤝 Contributing
Fork repository

Create feature branch

Commit changes

Push branch

Open Pull Request

📜 License
MIT License

📩 Support
Email: support@wellnest.com

Documentation: Coming Soon

Issues: GitHub Issues

⚠️ Disclaimer
WellNest is for informational purposes only and is not a substitute for professional medical advice.

🆘 Crisis Support
If you are in crisis:

Suicide & Crisis Lifeline: 988

Crisis Text Line: Text HOME to 741741

Emergency Services: 911 / Local Emergency Number

🌿 About WellNest
WellNest – Your trusted companion for understanding your mental wellness and finding personalized support.
