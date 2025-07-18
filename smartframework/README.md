# 🩺 FHIR Lesson 21 – Building Simple SMART on FHIR Applications

Welcome to **Lesson 21** of the FHIR curriculum: _Building Simple SMART on FHIR Applications_. This lesson provides a step-by-step guide to building secure, standards-compliant applications that authenticate and access FHIR resources using the **SMART on FHIR** protocol with OAuth 2.0.

👨‍🏫 _Instructors:_  
- **Patrick W. Jamieson, M.D.**, Technical Product Manager  
- **Russ Leftwich, M.D.**, Senior Clinical Advisor, Interoperability  

---

## 🎯 Lesson Objectives

- Understand how to use OAuth 2.0 access tokens to authorize FHIR API calls
- Build a series of SMART apps using progressive design techniques
- Separate concerns using modular Python code: `smart_auth.py`, `fhir_client.py`
- Use FHIR scopes to enforce access control and simulate patient-specific portals

---

## 🛠 Prerequisites

You must first clone and run the [SecureDockerFHIR](https://github.com/pjamiesointersystems/SecureDockerfhir) repository, which provides:

- A secure IRIS for Health Community Edition instance
- HTTPS support via SSL certificates
- A preconfigured Web Gateway for encrypted token flow

⚠️ Without HTTPS, OAuth-based FHIR access will fail—even with valid tokens:contentReference[oaicite:0]{index=0}.

---

## 🧪 Applications Built in This Lesson

### 🔓 Application 1: Basic SMART Authorization
- Launches the browser for OAuth login
- Retrieves a Patient resource using a bearer token
- Displays patient name and ID in the terminal

### 🧱 Application 2: Modular OAuth + FHIR Client
- Splits authentication and API logic into separate modules
- Lists multiple patients by name and FHIR ID
- Promotes reusable, maintainable code structure

### 🩺 Application 3: Retrieve Observations
- Selects a patient and displays related `Observation` resources
- Parses values and codes in a readable format
- Demonstrates token reuse and scoped resource filtering

### 🔐 Application 4: Patient-Facing Portal with Limited Scopes
- Implements SMART scopes like `patient/Patient.read`, `patient/Observation.read`
- Demonstrates how data access is constrained
- Shows Auth0 action for embedding the patient ID in the token claims:contentReference[oaicite:1]{index=1}

---

## 📂 Repository Contents

- `smart_auth.py` – Handles SMART on FHIR login and token flow  
- `fhir_client.py` – Wraps common FHIR API interactions  
- `textual_app.py` – Terminal UI for login, patient selection, and data display  
- `README.md` – This document  

---

## 🔮 Next Steps

In upcoming lessons, you’ll build on these SMART foundations to support clinical decision tools, app registration, consent management, and full patient portal experiences. This lesson equips you with a secure, scalable starting point for all future FHIR app development.

> "SMART on FHIR makes it possible to innovate securely—with real data, real users, and real trust."

---

## 📬 Questions?

Feel free to open an issue or start a discussion on this GitHub repository. Happy coding!


