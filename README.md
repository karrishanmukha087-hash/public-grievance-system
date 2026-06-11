# Public Grievance Management System

A complete, professional, secure, and responsive Public Grievance Portal where citizens can register, lodge complaints, track grievance progress through a live history timeline, and receive notification feeds. Administrators can manage complaints, departments, compile Excel/PDF reports, and analyze data through an analytics dashboard.

---

## 🌐 Live Website Links
* **Citizen Portal (Live)**: [https://public-grievance-system-riuf.onrender.com](https://public-grievance-system-riuf.onrender.com)
* **Admin Portal (Live)**: [https://public-grievance-system-riuf.onrender.com/admin.html](https://public-grievance-system-riuf.onrender.com/admin.html)

### 🔑 Default Credentials
* **Admin Username/Email**: `admin` or `admin@grievanceportal.gov`
* **Admin Password**: `Admin@123`

---

## 🚀 Key Features

* **Citizen Dashboard**: Lodge grievances with file attachments (PDF/images), track timelines, and manage profile settings.
* **Notification Feed**: Real-time in-app alerts on status shifts.
* **Email Notifications**: Confirmation emails on registration, grievance lodging, and status updates (uses `nodemailer` with SMTP or local simulation fallback).
* **Admin Control Center**: KPI summary grids, real-time monthly trend and category graphs (Chart.js), filterable queue, and user account management.
* **Excel & PDF Reports**: Generate structured intervals summary (Daily, Weekly, Monthly, Yearly) client-side using SheetJS (`xlsx`) and `jspdf`.
* **Dark Mode Toggle**: Persistent theme settings (light/dark) using CSS variables and localStorage.

---

## 🛠️ Technology Stack

* **Frontend**: HTML5, CSS3, JavaScript, Bootstrap 5
* **Backend**: Node.js, Express.js
* **Database**: MySQL (local/production) or SQLite (cloud deployment fallback)
* **Authentication**: JWT, bcrypt Password Hashing
* **File Upload**: Multer

---

## ⚙️ How to Configure Permanent Data Persistence
This project runs using an SQLite database fallback on Render's free tier. Since free instances wipe local files when sleeping, follow these steps to connect a free persistent MySQL database:

1. Sign up on [Clever Cloud](https://www.clever-cloud.com/).
2. Create a free **MySQL Add-on** (Shared/Dev plan).
3. In your **Render Dashboard**, go to **Environment** settings and add:
   * `DB_HOST` = *(Your Clever Cloud Host)*
   * `DB_USER` = *(Your Clever Cloud User)*
   * `DB_PASSWORD` = *(Your Clever Cloud Password)*
   * `DB_NAME` = *(Your Clever Cloud Database Name)*
4. Save Changes to redeploy with persistent cloud storage!
