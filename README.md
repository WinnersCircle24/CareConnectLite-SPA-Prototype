# CareConnectLite: SPA Scheduling Prototype



## 📌 Project Overview

CareConnectLite is a front-end Single-Page Application (SPA) prototype designed for a student health clinic. Built without heavy frameworks, it utilizes Vanilla JavaScript, HTML5, and native CSS variables to deliver a responsive, zero-dependency user interface.



**My Role:** Business Analysis & UX Design  

**Focus:** Translating user requirements into an intuitive scheduling workflow while ensuring front-end components mapped cleanly to backend data structures.



---



## 🏗️ Architecture & Mock Backend



To demonstrate full application logic without requiring a live server, this prototype features an **In-Memory Relational Database Simulation**. 



The JavaScript engine simulates a backend environment by managing state across five distinct arrays that represent SQL tables:

* `Users`

* `Clinicians`

* `Appointments`

* `IntakeForms`

* `Notifications`



### ⚙️ Key Technical Features:

* **Relational Data Mapping:** Uses integer Foreign Keys (e.g., `userId`, `clinicianId`) to link data across simulated tables.

* **Simulated SQL JOINs:** Render functions dynamically resolve user and provider names from ID references before painting the UI.

* **Cascading CRUD Operations:** Booking an appointment automatically triggers cascading `INSERT` operations to generate linked Intake Forms and Notification records.

* **Session State Management:** Simulates active user sessions to scope read/write permissions for appointments and dashboards.



---



## 🎨 UI/UX Execution

* **Custom CSS Design System:** Replicated a modern utility-class design system (similar to Tailwind) using pure CSS variables for maximum portability.

* **Transient State Handling:** Replaced native browser alerts with a custom, branded toast notification system and modal overlays.

* **Zero-Trust Input:** implemented strict DOM-method generation (`textContent`) over `innerHTML` injection to prevent simulated XSS vulnerabilities in user-derived strings.