# 🩺 DermaByte — AI-Powered Dermatology & Telehealth Ecosystem

<!-- TECH BADGES -->
<p align="left">
  <img src="https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white" alt="Flutter" />
  <img src="https://img.shields.io/badge/AI--Integration-Dermatology-red?style=for-the-badge" alt="AI" />
  <img src="https://img.shields.io/badge/Telehealth-Zoom%20SDK-blue?style=for-the-badge" alt="Zoom" />
  <img src="https://img.shields.io/badge/REST%20APIs-Dio%20%2F%20HTTP-orange?style=for-the-badge" alt="REST APIs" />
  <img src="https://img.shields.io/badge/Architecture-Clean-brightgreen?style=for-the-badge" alt="Clean Architecture" />
</p>

> 🚀 Elite telehealth pipeline connecting Patients, Doctors, and Labs via strict **Clean Architecture**. Automates the medical lifecycle from AI diagnosis to live Zoom consultation.

---

### 🏗️ 📐 Presentation & Medical UI

* **🧩 Atomic Clinical Widgets:** Generic components (AI Scan Frames, Dynamic Lab Reports, Live Chat/Request Boards) to prevent UI duplication.
* **⚡ State-Driven Workflows:** Localized Cubit states to handle real-time medical order mutations without full screen lagging.

---

### ⚡ 🔮 Core Project Functions (The Patient-Doctor-Lab Lifecycle)

#### 1️⃣ 🤖 AI DIAGNOSTICS: Skin Scan Pipeline (`analyzeSkinCondition`)
* **🧠 Logic:** Direct image streaming to a backend AI model for immediate dermatological assessment.
* **⚙️ Steps:** Uploads photo via `FormData` ➔ Receives AI diagnostic tokens ➔ Automatically attaches the AI result to the doctor’s booking request.

#### 2️⃣ 🤝 DOCTOR PORTAL: Live Request & Lab Orders (`manageDoctorRequest`)
* **🧠 Logic:** Dynamic open-ticket system between patient and physician before the physical session.
* **⚙️ Steps:** Doctor reviews AI result ➔ Requests specific lab tests inside the open ticket ➔ Instantly updates patient's live UI state.

#### 3️⃣ 🧪 LAB INTEGRATION: In-App Booking & Upload (`bookAndUploadLabTest`)
* **🧠 Logic:** Third-party Lab workflow handled entirely within the API infrastructure.
* **⚙️ Steps:** Patient books a certified Lab via the app ➔ Lab uploads results directly to the backend ➔ Doctor instantly views reports on their clinical dashboard.

#### 4️⃣ 🎥 TELEHEALTH: Live Zoom Session (`initializeZoomSession`)
* **🧠 Logic:** Secure virtual consultation execution based on fully analyzed medical profiles.
* **⚙️ Steps:** Validates lab test completion ➔ Generates dynamic video tokens ➔ Launches the live **Zoom virtual session** inside the app.

---

### 🛠️ 💻 Tech Stack

* **📱 Framework:** Flutter (iOS & Android)
* **📐 Architecture:** Feature-Driven Clean Architecture (Data, Domain, Presentation)
* **🔄 State Management:** Flutter BLoC / Cubit
* **🌐 Network:** REST APIs (Dio, Multi-part Image Uploads, Custom Interceptors)
* **🎥 Integrations:** In-App Video Consultation (Zoom SDK Integration)
