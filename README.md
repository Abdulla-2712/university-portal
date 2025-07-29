**Please finish the README file for proper configuration**

## 🎓 University Portal
A full-stack web application for managing student complaint and suggestion systems. Built with a modern stack:

   - **Frontend:** Next.js (React)
   - **Backend:** Django + PostgreSQL
   - **Auth:** JWT
   - **Email:** SMTP for user notifications



## 🗂 Repository Structure
university-portal/

      ├── university-portal-frontend/ → Next.js (React)
      ├── university-portal-backend/ → Django + PostgreSQL
      └── README.md → You’re here




## 🛠 Prerequisites
Make sure you have installed:
- **Node.js** (v18+)
- **Python** (3.10+)
- **PostgreSQL**
- **pipenv** or `virtualenv`
- **Git** with submodule support




## 🚀 How to Run the Project
**Clone into the frontend:**
-
run:

      cd university-portal-frontend
      npm install
      npm run dev
   **Runs the app at: http://localhost:3000**

**Clone into the backend:**
-
run:

      cd university-portal-backend
      python -m venv venv
      source venv/bin/activate  # Or `venv\Scripts\activate` on Windows
      pip install -r requirements.txt
      rav run migrate
      rav run makemigrations
      rav run server

   **Runs the API at: http://localhost:8001**




## 🛢 PostgreSQL Configuration
Ensure PostgreSQL is running, and update your backend UniversityPortal/settings.py with:




      DATABASES = {
         'default': {
            'ENGINE': 'django.db.backends.postgresql',
            'NAME': 'your_db_name',
            'USER': 'your_db_user',
            'PASSWORD': 'your_db_password',
            'HOST': 'localhost',
            'PORT': '5432',
         }
      }





## 📧 Email Configuration
To enable email functionalities such as sending confirmation messages, the backend uses SMTP through Gmail. The email configuration is located in the Django project's `settings.py` file.

### 🔐 Securely Setting Up Gmail for SMTP
To securely send emails through your Gmail account without exposing your real password, follow these steps:

1. **Enable 2-Step Verification** on your Google account:
   - Go to [Google Account Security](https://myaccount.google.com/security).
   - Under the "Signing in to Google" section, enable **2-Step Verification**.

2. **Generate an App Password**:
   - After enabling 2-Step Verification, go back to the **Security** tab.
   - Under "Signing in to Google", select **App passwords**.
   - Choose `Mail` as the app and `Other` as the device (e.g., "Django App").
   - Google will generate a 16-character app password. **Copy it**, as this is the one you'll use in your `settings.py`.

3. **Update the `settings.py`** in your Django project:

         EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'
         EMAIL_HOST = 'smtp.gmail.com'
         EMAIL_PORT = 587
         EMAIL_USE_TLS = True
         EMAIL_HOST_USER = 'your_email@gmail.com'  # Replace with your Gmail
         EMAIL_HOST_PASSWORD = 'your_generated_app_password'  # Replace with the app password
      ---------------------------------------------------------------------------------------------------------------------------------------



## 👨‍💻 Authors
   - **Abdulla Omar Ali Sayed**

aabdula2712@gmail.com • [GitHub](https://github.com/Abdulla-2712) • [LinkedIn](https://linkedin.com/in/abdulla-omar-ali/)

- **Zeyad Mohamed Elsayed Gasser**

zeyadgasser2510@gmail.com • [GitHub](https://github.com/ZEYAD-GASSER) • [LinkedIn](https://www.linkedin.com/in/zeyad-gasser-699852272/)
## Need Help?

If you face any issues or cannot run the project, feel free to reach out to the authors — they’d be happy to help!
