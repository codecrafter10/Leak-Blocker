# LeakBlocker – Blockchain-Based Secure Exam Management System

LeakBlocker is a **blockchain-inspired Exam Management System** built using **HTML, CSS, and JavaScript**.  
It focuses on **preventing question paper leaks** and increasing **transparency, traceability, and security** in the exam process.

The system provides **two main panels**:

- **Admin Panel**
- **Faculty Panel**

> ⚠️ Note: This is a **front-end only (simulation)** project. No real backend or live blockchain network is used.  
> All blockchain, encryption, and logs are **simulated using JavaScript** for learning and demonstration purposes.

---

## 🎯 Project Objective

The main objective of LeakBlocker is to:

- Reduce the risk of **question paper leaks**
- Maintain an **immutable trail** of all important actions (upload, lock, view, distribute)
- Use **blockchain concepts** (blocks, hashes, previous hash, ledger) to make actions **verifiable and tamper-evident**
- Provide a **simple, interactive UI** using only **HTML, CSS, JS**

---

## ✨ Key Features

### 🔐 1. Role-Based Access (Admin & Faculty)

- Separate login screens for:
  - **Admin**
  - **Faculty**
- Different dashboards depending on user role
- Only authorized users can perform sensitive actions like:
  - Uploading question papers
  - Locking papers
  - Changing exam status

---

### ⛓️ 2. Blockchain-Style Audit Trail

- Every important action is converted into a **blockchain transaction**, such as:
  - Question paper created
  - Paper uploaded
  - Paper locked
  - Paper viewed
  - Paper distributed
- Each **block** contains:
  - Block index
  - Timestamp
  - Action type
  - User (Admin/Faculty)
  - Exam ID / Paper ID
  - Previous block hash
  - Current block hash (simulated)
- All blocks are stored in a **JavaScript array**, representing the **ledger**
- A **visual “Ledger / Timeline” page** shows these entries like a block explorer

---

### 🧾 3. Question Paper Upload & Status Flow

- Faculty can:
  - Upload question paper details (title, subject, exam date, etc.)
  - Simulate uploading a file (front-end only form)
  - Preview the paper on the screen
- Paper status moves through stages:
  - `Draft → Uploaded → Locked → Ready for Distribution → Distributed`
- Each status change is:
  - Stored as a **block**
  - Shown in the **dashboard in real-time style UI**

---

### 💧 4. Watermarking & AI-Style Time Stamping

- When a paper is previewed, a **dynamic watermark** is displayed, e.g.:
  - `Confidential – Exam ID: EXM101`
  - `Faculty ID: FAC-001`
  - Date & time of access
- Watermark is added using **CSS + JS** and appears over the question paper content
- **AI-style timestamps**, like:
  - “Uploaded 2 minutes ago”
  - “Last viewed 10 seconds ago”
- Time is handled using **JavaScript Date** and periodically updated

---

### 🔑 5. Secure Access Keys (Simulation)

- Admin can generate **secure access keys / tokens** for:
  - Locking & unlocking papers
  - Marking a paper as “Ready for Distribution”
- JavaScript is used to:
  - Generate random keys
  - Validate them on actions
  - Log each key usage as a **block in the ledger**

---

### 📅 6. Exam Scheduling Module

- Admin can:
  - Create exams with:
    - Exam name
    - Course / subject
    - Date & time
    - Assigned faculty
  - View a list of upcoming exams
- Each new exam creation is logged as a blockchain-style transaction

---

### 📊 7. Dashboard & Visual Logs

- **Admin Dashboard**:
  - Total exams
  - Total papers uploaded
  - Recent actions (latest blocks)
  - Status overview of question papers
- **Faculty Dashboard**:
  - Exams assigned to that faculty
  - Paper upload history
  - Latest actions performed by that faculty
- **Audit Log / Ledger Page**:
  - Table or card view of all blocks (transactions)
  - Shows who did what, and when

---

## 🛠️ Tech Stack

- **HTML5** – Structure, forms, and panels
- **CSS3** – Layout, responsive design, dashboards, cards, watermarks
- **JavaScript (ES6)** –  
  - Logic for:
    - Blockchain simulation (blocks, hashes)
    - Timers and timestamps
    - Role-based view rendering
    - Status changes and logs
    - Simple “encryption key” simulation

---

## 📂 Suggested Folder Structure

``bash
LeakBlocker/
├─ index.html              # Landing + Login
├─ admin-dashboard.html    # Admin panel
├─ faculty-dashboard.html  # Faculty panel
├─ ledger.html             # Blockchain / audit log view
├─ css/
│  ├─ style.css            # Global styles
│  ├─ admin.css           # Admin-specific styles
│  └─ faculty.css         # Faculty-specific styles
├─ js/
│  ├─ app.js               # Main app logic
│  ├─ blockchain.js        # Blockchain simulation (Block, Blockchain classes)
│  ├─ auth.js              # Simple login + role handling (front-end only)
│  └─ ui.js                # DOM updates, dashboards, rendering logs
└─ assets/
   ├─ logo.png
