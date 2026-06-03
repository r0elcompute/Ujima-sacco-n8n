# Ujima SACCO: Decentralized Agentic Credit Appraisal Portal

An ethically aligned, localized financial technology MVP designed to bridge the credit gap for informal market traders (e.g., Mama Mbogas, agricultural wholesalers) in East Africa. This repository contains the front-end user interface and the backend technical workflow architecture built during the AI Safari Expedition.

## 🚀 Live Links
* **Live Web Portal:** [https://ujima-sacco.netlify.app/]
* **Automated Data Ledger:** [https://docs.google.com/spreadsheets/d/13KdJ2iEGHm52LgmJUBD-nD20h2PVZ01oksKtry2Qt9Q/edit?usp=sharing]

---

## 📌 Project Overview
Traditional credit scoring models systematically exclude informal traders by demanding rigid financial footprints, such as monthly corporate payslips. This structural bias causes an estimated **68% rejection rate** for viable informal businesses. 

**Ujima SACCO** solves this by implementing a decentralized multi-agent system that evaluates transaction velocity against regional seasonal cycles (e.g., agricultural harvest calendars) rather than arbitrary 30-day templates, ensuring user dignity and financial inclusion.

### Core Architecture Components
1. **Accessible Front-End Portal:** A clean, responsive HTML5/CSS3 sign-up interface tailored for desktop and mobile environments.
2. **Dynamic n8n Logic Engine:** A backend automation pipeline running a live production webhook to process incoming application metadata.
3. **Automated Risk Triage (HUNT Framework):** Conditional logical routing based on a calibrated threshold of KES 15,000 to distribute operational loads.
4. **Transparent Distributed Ledger:** A Google Sheets central ledger mapping automated actions against human-in-the-loop escalations.

---

## 🛠️ Technical Architecture & Workflow

Data flows seamlessly from the member-facing portal through a dual-track backend automation pipeline before committing to the core tracking database:

```text
[Netlify Front-End Form] 
       │
       ▼ (POST Request via JSON)
[n8n Production Webhook]
       │
       ▼ (Type Casting .toNumber())
[HUNT Trigger: Amount Check]
       │
       ├─► (True: <= 15,000 KES) ──► [Guardian Agent (Auto-Triage)] ──► [Log to Google Sheets]
       │
       └─► (False: > 15,000 KES) ──► [Hunter Agent (Human Dossier)]  ──► [Log to Google Sheets]