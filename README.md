# 🩺 DermaByte — AI-Powered Dermatology & Telehealth System

<!-- TECH BADGES -->
<p align="left">
  <img src="https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white" alt="Flutter" />
  <img src="https://img.shields.io/badge/AI--Integration-Dermatology-red?style=for-the-badge" alt="AI" />
  <img src="https://img.shields.io/badge/Telehealth-Zoom%20SDK-blue?style=for-the-badge" alt="Zoom" />
  <img src="https://img.shields.io/badge/REST%20APIs-Dio-orange?style=for-the-badge" alt="REST APIs" />
  <img src="https://img.shields.io/badge/Architecture-Clean-brightgreen?style=for-the-badge" alt="Clean Architecture" />
</p>

> 🚀 Healthcare app built on **Clean Architecture**. Connects Patients, Doctors, and Labs in one dynamic workflow from AI scan to Zoom sessions.

---

### ⚡ 🔮 The Patient-Doctor-Lab Workflow

#### 1️⃣ 🤖 Patient: AI Skin Scan
* **🧠 Logic:** Send skin photos to backend AI for instant analysis.
* **⚙️ Steps:** Uploads image using `FormData` via **Dio** ➔ Receives AI result ➔ Attaches result automatically to Doctor booking.

#### 2️⃣ 🤝 Doctor: Review & Lab Requests
* **🧠 Logic:** Live "Open Ticket" between patient and doctor before the session.
* **⚙️ Steps:** Doctor checks AI result ➔ Requests specific lab tests ➔ Patient's UI updates instantly via Cubit.

#### 3️⃣ 🧪 Lab: Booking & Upload
* **🧠 Logic:** Integrated lab subsystem with zero local caching.
* **⚙️ Steps:** Patient books a lab from the app ➔ Lab uploads results directly to API ➔ Doctor views reports instantly on dashboard.

#### 4️⃣ 🎥 Telehealth: Online Zoom Session
* **🧠 Logic:** Live video consultation inside the app.
* **⚙️ Steps:** Verifies lab files ➔ Generates meeting token ➔ Launches live **Zoom Session**.

---

### 🛠️ 💻 Tech Stack

* **📱 Framework:** Flutter (iOS & Android)
* **📐 Architecture:** Feature-Driven Clean Architecture
* **🔄 State Management:** Flutter BLoC / Cubit
* **🌐 Network:** REST APIs (Dio & Custom Interceptors)
* **🎥 Integration:** Zoom SDK
