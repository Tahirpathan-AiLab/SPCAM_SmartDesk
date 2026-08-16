## Code Description

**SPCAM SmartDesk** is a full-stack **College / Institute Management System** built with **Django**, designed to digitize and centralize the day-to-day academic and administrative workflows of a college. The platform brings students, faculty, and administrators onto a single web portal, replacing scattered paperwork and manual record-keeping with a structured, database-driven system.

The system was built for **SPCAM** to handle core academic operations such as **student onboarding through admission forms**, **secure authentication**, **student profile management**, **subject and class management**, **exam marks entry and tracking**, **faculty record management**, and an **admin dashboard** for overseeing the entire institution.

My contribution covers the **complete end-to-end development** of the platform — from designing the relational database schema to building the Django backend logic, wiring up URL routing, handling file uploads for admission documents, and developing the front-end templates that students, faculty, and admins interact with.

Unlike a simple static college website, SPCAM SmartDesk is a **dynamic, data-driven web application**. Every form submission, mark entry, and profile update is persisted to a relational database, allowing the institution to maintain accurate, queryable academic records instead of relying on physical files or disconnected spreadsheets.

The repository demonstrates how a real-world institutional workflow can be digitized using Django's MVT (Model-View-Template) architecture, combining relational database design, form handling, file/document uploads, authentication, and role-based dashboards into a single cohesive system.

---

## System Workflow

The workflow begins the moment a prospective or existing student lands on the portal's landing page. From there, users are routed through **sign-up and sign-in flows** that authenticate them against the `Signup_user` model before granting access to protected areas of the site.

Once authenticated, students can access their **personal profile**, view and edit their academic details, and submit a detailed **Admission Form** — capturing personal information, parental details, academic history, and category-specific documents such as photographs, higher secondary certificates, caste certificates, marksheets, and Aadhar card, all stored via Django's `FileField` uploads.

On the academic side, the system maintains structured relationships between **Classes**, **Subjects**, and **Students**, allowing administrators to define subjects per class and semester. Faculty members are able to record and update **exam marks** for students against specific subjects, with each entry linked through foreign keys to preserve data integrity across the `ExamMarks`, `Student_profile`, and `Subject` tables.

The project also includes a dedicated **Faculty module**, where staff details — including qualifications, experience, research work, publications, and seminar participation — are stored and displayed, giving the institution a searchable digital record of its teaching staff.

For oversight, a **SPCAM Admin panel** and **Analytics view** allow administrators to monitor submissions, review student data, and manage the platform as a whole, while a **Reviews module** and **Tables view** provide additional feedback and tabular reporting layers within the portal.

The final result is a connected academic ecosystem where student records, admission documents, faculty information, and exam performance all live within a single, queryable Django-powered database.

---

## Methods Implemented

This project combines multiple web-development and data-management techniques to build a reliable institutional platform.

### Relational Database Modeling

The core of the system is built around Django ORM models — `Signup_user`, `Student_profile`, `AdmissionForm`, `Class`, `Subject`, `ExamMarks`, and `Faculty` — each capturing a distinct academic entity while remaining linked through foreign-key relationships to preserve consistency across the database.

### Authentication & Session Handling

Custom sign-up and sign-in views manage user authentication and session state, controlling access to protected pages such as the student profile, marks entry, and admin dashboard.

### Document & File Upload Handling

The admission workflow uses Django `FileField`s to securely accept and store multiple category-specific documents per student — photographs, certificates, and marksheets — organized into dedicated upload directories.

### Dynamic Class–Subject–Marks Mapping

Classes and subjects are modeled as related entities so that exam marks can be recorded per student, per subject, per semester, enabling structured academic performance tracking over time.

### Faculty Record Management

A dedicated model and set of views allow faculty profiles — including experience, education, research output, and publication counts — to be added, stored, and displayed through the portal.

### Admin Dashboard & Analytics

A host-only admin view (`spcam_admin`) and an analytics view give administrators a consolidated look at platform activity, submissions, and academic data.

### Template-Driven Front End

Django's template engine renders all user-facing pages — sign-in/sign-up, profiles, admission forms, tables, reviews, and analytics — using a consistent HTML/CSS/JS front end served through Django's static and media file handling.

---

## Key Features

* Student **sign-up and sign-in** authentication flow
* Editable **student profile** with contact, academic, and personal details
* Detailed **online admission form** with parental, academic, and document fields
* Secure **document uploads** for photographs, certificates, and marksheets
* **Class and subject management** linked to specific semesters
* **Exam marks entry and tracking** mapped to students and subjects
* Dedicated **faculty module** storing qualifications, research, and publications
* **Admin dashboard** for institution-wide oversight
* **Analytics view** for reviewing platform and academic data
* **Reviews and tables** modules for feedback and tabular reporting
* Media and static file handling for images, documents, and uploads
* Deployment-ready configuration for **Render** and **Vercel**

---

## Project Workflow

<p align="center">
  <img src="https://img.shields.io/badge/1-Student%20Sign%20Up%20%2F%20Sign%20In-4CAF50?style=for-the-badge"/>
</p>

<p align="center">⬇️</p>

<p align="center">
  <img src="https://img.shields.io/badge/2-Student%20Profile%20Setup-2196F3?style=for-the-badge"/>
</p>

<p align="center">⬇️</p>

<p align="center">
  <img src="https://img.shields.io/badge/3-Admission%20Form%20Submission-FF9800?style=for-the-badge"/>
</p>

<p align="center">⬇️</p>

<p align="center">
  <img src="https://img.shields.io/badge/4-Document%20Upload%20%26%20Storage-E91E63?style=for-the-badge"/>
</p>

<p align="center">⬇️</p>

<p align="center">
  <img src="https://img.shields.io/badge/5-Class%20%26%20Subject%20Mapping-9C27B0?style=for-the-badge"/>
</p>

<p align="center">⬇️</p>

<p align="center">
  <img src="https://img.shields.io/badge/6-Exam%20Marks%20Entry-00BCD4?style=for-the-badge"/>
</p>

<p align="center">⬇️</p>

<p align="center">
  <img src="https://img.shields.io/badge/7-Faculty%20Record%20Management-795548?style=for-the-badge"/>
</p>

<p align="center">⬇️</p>

<p align="center">
  <img src="https://img.shields.io/badge/8-Admin%20Dashboard%20Review-607D8B?style=for-the-badge"/>
</p>

<p align="center">⬇️</p>

<p align="center">
  <img src="https://img.shields.io/badge/9-Analytics%20%26%20Reports-3F51B5?style=for-the-badge"/>
</p>

<p align="center">⬇️</p>

<p align="center">
  <img src="https://img.shields.io/badge/10-Deployment-009688?style=for-the-badge"/>
</p>

---

## Technologies Used

<p align="center">
  <img src="https://skillicons.dev/icons?i=python" alt="Python"/>
  <img src="https://skillicons.dev/icons?i=django" alt="Django"/>
  <img src="https://skillicons.dev/icons?i=html" alt="HTML5"/>
  <img src="https://skillicons.dev/icons?i=css" alt="CSS3"/>
  <img src="https://skillicons.dev/icons?i=js" alt="JavaScript"/>
  <img src="https://skillicons.dev/icons?i=sqlite" alt="SQLite"/>
  <img src="https://skillicons.dev/icons?i=vscode" alt="VS Code"/>
  <img src="https://skillicons.dev/icons?i=git" alt="Git"/>
  <img src="https://skillicons.dev/icons?i=vercel" alt="Vercel"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white"/>
  <img src="https://img.shields.io/badge/Django%20REST%20Framework-A30000?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white"/>
  <img src="https://img.shields.io/badge/Gunicorn-499848?style=for-the-badge&logo=gunicorn&logoColor=white"/>
  <img src="https://img.shields.io/badge/Pillow-6DB33F?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white"/>
  <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white"/>
  <img src="https://img.shields.io/badge/Plotly-3F4F75?style=for-the-badge&logo=plotly&logoColor=white"/>
</p>

---

## Project Structure

```text
SPCAM_SmartDesk
│
├── college                      # Django project configuration
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
│
├── database                     # Core application (models, views, forms)
│   ├── models.py
│   ├── views.py
│   ├── urls.py
│   ├── forms.py
│   ├── admin.py
│   ├── migrations/
│   └── img/
│
├── faculty                      # Faculty photos and documents
│   ├── photos/
│   └── uploads/
│
├── templates                    # HTML templates (Django Template Engine)
│   ├── index.html
│   ├── signin.html
│   ├── signup.html
│   ├── profile.html
│   ├── student_profile.html
│   ├── student_profile_Edit.html
│   ├── marks_adding.html
│   ├── class_subject.html
│   ├── class_subject_add.html
│   ├── analitics.html
│   ├── reviwes.html
│   ├── tables.html
│   └── spcam_admin.html
│
├── static                       # CSS, JS, icons, and static images
│   ├── style.css
│   ├── script.js
│   ├── icons/
│   ├── images/
│   └── Faculties/
│
├── uploads                      # Admission document uploads
│   ├── photograph/
│   ├── application_form/
│   ├── caste_certificate/
│   ├── higher_secondary_certificate/
│   ├── ssc_hsc_marksheets/
│   └── aadhar_card/
│
├── db.sqlite3
├── manage.py
├── build.sh
├── vercel.json
└── requirements.txt
```

---

## Core Modules

The application is organized around a set of interconnected Django models that represent the institution's academic structure.

### User & Authentication

- Signup_user
- Session-based sign-in / sign-out flow

### Student Records

- Student_profile
- AdmissionForm (personal, parental, academic, and document fields)

### Academic Structure

- Class
- Subject
- ExamMarks

### Faculty Records

- Faculty (qualifications, experience, research, publications, seminars)

### Document Uploads

- photograph
- application_form
- higher_secondary_certificate
- caste_certificate
- ssc_hsc_marksheets
- aadhar_card
- marriage_certificate
- other_qualifications

---

## Output

After successful setup and execution, the project provides:

* A fully functional **student portal** with sign-up, sign-in, and profile management.
* An **online admission form** with multi-document upload support.
* A structured **class–subject–marks** system for academic tracking.
* A **faculty directory** with detailed staff records.
* An **admin dashboard** for institution-wide management.
* **Analytics and tables views** for reviewing academic data.
* A SQLite-backed relational database (`db.sqlite3`) holding all institutional records.
* Deployment-ready build scripts for **Render** (`build.sh`) and **Vercel** (`vercel.json`).

---

## Applications

The SPCAM SmartDesk platform can directly support several real-world institutional needs, including:

* College / Institute Management Systems
* Student Admission & Onboarding Portals
* Academic Record & Marks Management
* Faculty Directory & Staff Management
* Institutional Admin Dashboards
* Digital Document Collection & Storage
* Class & Subject Scheduling Systems
* Campus ERP Solutions

---

## Acknowledgements

This project, **SPCAM SmartDesk**, was designed and developed to digitize the academic and administrative operations of **SPCAM**, providing a unified platform for students, faculty, and administrators.

All backend logic, database design, authentication flow, document upload handling, and front-end templates were implemented using **Django** to deliver a functional, institution-ready college management system.

---

## Conclusion

This project represents a complete **College Management System** built on Django, covering the full lifecycle of a student's interaction with an institution — from **sign-up and admission**, through **academic record-keeping**, to **faculty and administrative oversight**.

By combining relational database modeling, secure document handling, role-based views, and a template-driven front end into a single reproducible Django application, SPCAM SmartDesk provides a scalable foundation for building and deploying real-world campus ERP and student-management platforms.
