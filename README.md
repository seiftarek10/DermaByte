# 🩺 DermaByte — Advanced Medical Dermatology Ecosystem

<!-- TECH BADGES -->
<p align="left">
  <img src="https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white" alt="Flutter" />
  <img src="https://img.shields.io/badge/REST%20APIs-Dio%20%2F%20Http-orange?style=for-the-badge" alt="REST APIs" />
  <img src="https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black" alt="Firebase" />
  <img src="https://img.shields.io/badge/BLoC%20%2F%20Cubit-0175C2?style=for-the-badge&logo=dart&logoColor=white" alt="BLoC" />
  <img src="https://img.shields.io/badge/Architecture-Clean-brightgreen?style=for-the-badge" alt="Clean Architecture" />
</p>

> 🚀 A production-ready healthcare application built on strict **Clean Architecture**. Designed for seamless patient-to-doctor workflows and secure medical data handling.

---

### 🏗️ 📐 Presentation & Medical UI Components

* **🧩 Medical Widget Library:** Custom generic components (Scan Shimmers, Adaptive Patient Cards, Form Fields) engineered to isolate the **Presentation Layer** (**DRY Principle**).
* **⚡ 60fps Performance:** Highly optimized widget trees leveraging `const` constructors to eliminate redundant builds during data-heavy rendering.
* **🎨 Centralized Theme Injector:** Standardized dark/light medical themes to guarantee complete visual consistency across clinical dashboards.

---

### ⚡ 🔮 Core Project Functions

#### 1️⃣ 👤 PATIENT: Offline-First Health Records (`fetchPatientHistory`)
* **🧠 Logic:** Zero UI lag when viewing medical scans or consultation history.
* **⚙️ Steps:** Pulls cached data from **Hive DB** instantly ➔ Fetches background updates from server via repository contracts.

#### 2️⃣ 🔍 PATIENT: Zero-Leak Data Fetching & Scan Pagination
* **🧠 Logic:** Handles large medical logs and reports smoothly without spiking device memory.
* **⚙️ Steps:** Tracks logs via a dynamic cursor ➔ Fetches records in fixed blocks from **REST API / Cloud Firestore** ➔ Appends lazy rows to UI.

#### 3️⃣ 🔐 SECURITY: Compliant Identity Pipeline (`executeSecureAuth`)
* **🧠 Logic:** Bulletproof user/doctor authentication flow ensuring strict data privacy.
* **⚙️ Steps:** Fires encryption-ready requests to backend ➔ Safely caches session tokens via secure local storage ➔ Dispatches state via Cubit.

#### 4️⃣ 💼 BACKEND: Hybrid Healthcare Data Repository
* **🧠 Logic:** Synchronizes static medical profiles with live real-time clinical updates.
* **⚙️ Steps:** Combines **REST APIs** (for historical charts) and **Firestore Streams** (for live consultation statuses) under abstract contracts.

---

### 🛠️ 💻 Tech Stack

* **📱 Framework:** Flutter (Cross-Platform iOS & Android)
* **📐 Architecture:** Feature-Driven Clean Architecture & SOLID
* **🔄 State Management:** Flutter BloC / Cubit (Unidirectional Flow)
* **🌐 Network:** REST APIs (Dio) & Firebase Cloud Firestore
* **💾 Data Persistence:** Hive Local Binary DB & Secure Storage
* **🩺 Context:** Dermatology & Clinical E-Health Integration
