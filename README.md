# 🩺 DermaByte — Advanced Medical Dermatology Ecosystem

<!-- TECH BADGES -->
<p align="left">
  <img src="https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white" alt="Flutter" />
  <img src="https://img.shields.io/badge/REST%20APIs-Dio%20%2F%20Retrofit-orange?style=for-the-badge" alt="REST APIs" />
  <img src="https://img.shields.io/badge/State--Management-BLoC%20%2F%20Cubit-0175C2?style=for-the-badge&logo=dart&logoColor=white" alt="BLoC" />
  <img src="https://img.shields.io/badge/Storage-Hive%20DB-green?style=for-the-badge" alt="Hive" />
  <img src="https://img.shields.io/badge/Architecture-Clean-brightgreen?style=for-the-badge" alt="Clean Architecture" />
</p>

> 🚀 A production-grade healthcare application built on strict **Clean Architecture (Domain, Data, Presentation)**. Powered entirely by a **Centralized REST API** infrastructure for patient diagnostics and clinical data management.

---

### 🏗️ 📐 Presentation & Medical UI Components

* **🧩 Medical Widget Library:** Custom generic widgets (Scan Area Trackers, Patient Logs, Shimmer Loaders) built as abstract wrappers to enforce the **DRY Principle**.
* **⚡ 60fps Performance:** strict utilization of `const` constructors and localized state rebuilding via Cubit to prevent full screen lagging during heavy imaging lists.
* **🎨 Theme Injector:** Centralized Dark/Light healthcare-compliant theme configurations for consistent user experience.

---

### ⚡ 🔮 Core Project Functions & Detailed Logic

#### 1️⃣ 🔍 DIAGNOSTICS: Secure Skin Scan & Image Upload (`uploadAndAnalyzeScan`)
* **🧠 Logic:** Multi-part file stream processing to upload high-resolution dermatological photos safely to the API.
* **⚙️ Steps:** Compresses the raw image to prevent payload timeouts ➔ Packs file into a `FormData` object via **Dio** ➔ Tracks progress stream for UI percentage indicators ➔ Receives the diagnostic response or machine-learning analysis tokens from the backend.

#### 2️⃣ 👤 PATIENT FLOW: Offline-First Medical History (`getPatientMedicalRecords`)
* **🧠 Logic:** Instant caching architecture ensuring physicians and patients access historical diagnoses without network dependency.
* **⚙️ Steps:** Queries local **Hive Box** for an instant UI render ➔ Executes background HTTP GET request via Dio ➔ Compares responses to update local storage ➔ Silently updates UI if new clinical reports are available.

#### 3️⃣ 📅 BOOKINGS: Realtime Consultation Scheduler (`fetchAvailableSlots`)
* **🧠 Logic:** Dynamic filtering of clinical appointments and doctor timetables based on live server availability.
* **⚙️ Steps:** Passes date and specialty parameters via API endpoints ➔ Normalizes JSON arrays into immutable Domain entities ➔ Maps data directly into interactive time-slot grids managed by a dedicated Booking Cubit.

#### 4️⃣ 🌐 NETWORK INFRASTRUCTURE: Resilient Interceptor Engine (`DioClientFactory`)
* **🧠 Logic:** Centralized API middleware layer to handle global exceptions, security headers, and JWT updates automatically.
* **⚙️ Steps:** Intercepts outgoing requests to inject Bearer tokens ➔ Listens for HTTP 401 Unauthorized errors ➔ Executes token refresh loops automatically ➔ Globally catches and formats validation errors for user-friendly UI popups.

---

### 🛠️ 💻 Tech Stack & Production Patterns

* **📱 Framework:** Flutter (Cross-Platform iOS & Android)
* **📐 Architecture:** Feature-Driven Clean Architecture & SOLID Principles
* **🔄 State Management:** Flutter BloC / Cubit (Unidirectional Flow)
* **🌐 Network Layer:** Advanced REST APIs (Dio Client, Custom Interceptors, Error Handling)
* **💾 Data Persistence:** Hive Local Binary DB (Secure Session & Records Caching)
