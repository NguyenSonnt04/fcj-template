---
title: "System Screenshots"
date: 2024-01-01
weight: 11
chapter: false
pre: " <b> 5.11. </b> "
---

### 1. Admin Portal Interface Overview
The administration portal of **TrustBite** is built using **Next.js** and **TailwindCSS**, providing a clean and intuitive interface for managing user verification workflows and anti-fraud queues.

Below is the detailed description of each module interface in the system along with screenshot checkpoints:

---

### 2. Dashboard Overview
The central dashboard displays real-time system health, API status (Online/Offline), total active restaurants, and the capability/permission details of the logged-in administrator.

The interface is divided into functional modules via the left sidebar:
*   **Main:** Overview Dashboard.
*   **Management:** Restaurants & Users.
*   **Trust:** Review Moderation & Receipt Verification Queue.
*   **System:** Audit Logs & API Health Monitoring.

> [!IMPORTANT]
> **Screenshot Checkpoint:**
> * **Screenshot 19:** Admin Portal homepage showing the central command dashboard and online statuses of modular API components.

---

### 3. Restaurant Management Screen
Displays a table listing all restaurants registered in the system. Administrators can search by name, filter by status (Active, Draft, Suspended, Closed), and view calculated Trust Scores.

Clicking a restaurant opens a detail modal allowing management of:
*   Name, Address, and Phone Number.
*   **Latitude** and **Longitude** coordinate fields used for GPS proximity checks.
*   Restaurant images (uploading and configuring the primary avatar image).

> [!IMPORTANT]
> **Screenshot Checkpoint:**
> * **Screenshot 20:** Restaurant list grid and the detail editing modal displaying latitude and longitude input coordinates.

---

### 4. User Management Screen
Displays a list of all user profiles registered on the system, including phone numbers, display names, experience points (EXP), ranks, and security roles.

The role assignment modal allows quickly assigning roles:
*   **USER**: Standard consumer review author.
*   **MERCHANT**: Restaurant owner.
*   **ADMIN**: System administrator with full access privileges.

> [!IMPORTANT]
> **Screenshot Checkpoint:**
> * **Screenshot 21:** User management table displaying user accounts and the Cognito role assignment dropdown menu.

---

### 5. Receipt Verification Queue Screen
The core screen of the anti-fraud system, displaying food reviews accompanied by receipts currently in the **PENDING_ADMIN_REVIEW** state (risk scores between 31 and 60).

The queue audit detail view displays:
1.  The raw receipt image uploaded by the user.
2.  OCR parsed text blocks from AWS Textract (merchant name, invoice number, transaction date, total amount).
3.  The computed **Fraud Risk Score** alongside warning flags (e.g., *GPS distance > 200m*, *New account created < 24h*, etc.).
4.  Action buttons to decide outcome (**APPROVE** / **REJECT** / **REFERENCE ONLY**) along with a mandatory audit reason input.

> [!IMPORTANT]
> **Screenshot Checkpoint:**
> * **Screenshot 22:** Receipt verification audit queue detail page displaying the uploaded invoice, parsed OCR blocks, and the calculated fraud risk assessment breakdown.
