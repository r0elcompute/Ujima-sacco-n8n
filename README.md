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

## 🛠️ Technical Architecture & System Data Flow

The Ujima SACCO platform utilizes a decoupled, asynchronous multi-agent architecture. Data transforms seamlessly from a client-side application payload into an audited, structured ledger transaction through a specialized multi-track pipeline.

### 1. Ujima Sacco Dashboard/Front End UI
The diagram below illustrates the prototype/front end user interface for Ujima Sacco.

![landing page hero section](assets/hero.png)
![more information page](assets/more-info.png)
![sign up form](assets/signup-form.png)
![footer](assets/footer.png)

### 2. Production n8n Visual Workflow Pipeline

The visual canvas below displays the live node setup executing inside the n8n orchestration instance, displaying the automated processing from initial webhook trigger to the final ledger append actions.

![Ujima SACCO n8n Backend Workflow Engine](assets/workflow.png)

---

### 3. Architectural Implementation Highlights

* **The Webhook Handshake Optimization:** To accommodate unstable mobile networks in regional coastal trading hubs, the primary n8n webhook response behavior is configured to **"Respond to Webhook Node"**. By emitting an immediate `200 OK` handshake upon payload ingestion, the client frontend interface is decoupled from background computation times—eliminating visual lag or app freezes.
* **The GUARD Protocol (Defensive Type-Safety):** To handle raw form inputs cleanly, data fields undergo explicit type-casting within a dedicated JavaScript node. Converting numeric character strings into true floats (`.toNumber()`) before evaluation eliminates variable mismatches and ensures continuous platform availability during peak transactional windows.
* **Algorithmic Risk Boundary Hard-Coding:** The **KES 15,000** threshold acts as an automated circuit breaker. Low-exposure transactions run autonomously under a zero-variance model framework, while any high-exposure asset risk is intercepted, parsed into an automated dossier, and cleanly routed to a human credit officer for local contextual evaluation.
