# 🏥 Clinic Management System ERD

This project defines the **Entity-Relationship Diagram (ERD)** for a modern Clinic Management System. It serves as the digital backbone of a clinic, ensuring smooth data flow from patient scheduling to consultation, diagnostics, and billing—without losing critical information at any stage.

---

## 🔑 Key Features

### 📅 Appointments vs. Consultations

The system separates **Bookings** from **Actual Visits**:

* **Appointments** track scheduled visits, cancellations, and no-shows.
* **Consultations** store actual medical interactions.

This keeps patient medical history clean and accurate while still tracking operational data.

---

### 🔄 The Diagnostic Loop

Doctors can prescribe multiple tests during a single consultation:

* Each consultation can generate multiple **prescribed tests**
* Each prescribed test is linked to its **test report**

This creates a clear trace:

> Consultation → Test Prescription → Test Report

---

### 🏥 Specialty Management

Doctors are grouped into **specialties** (e.g., Cardiology, Pediatrics):

* Makes the system scalable and organized
* Improves searchability and filtering

---

## 🗂️ Data Model Overview

### 👥 The People

Core entities representing users of the system:

* **patients** – Stores patient profiles
* **doctors** – Stores doctor profiles
* **specialties** – Master list of medical departments

---

### 🔁 The Workflow

Tracks the patient journey:

* **appointments** – Initial booking records
* **consultations** – Actual visits with diagnoses and notes

---

### 🧪 The Labs

Handles diagnostics and reports:

* **test_catalog** – List of available medical tests
* **prescribed_tests** – Tests ordered by doctors
* **test_reports** – Results linked to prescribed tests

---

### 💳 The Financials

Tracks billing and payments:

* **payments** – Records transactions linked to consultations

---

## 🛠️ ERD Conventions

* **PK (Primary Key)**
  Unique identifier for each record in a table

* **FK (Foreign Key)**
  Field used to link one table to another

* **Relationships (Arrows)**
  Indicate how entities are connected:

  * One doctor → Many appointments
  * One consultation → Many prescribed tests
  * One prescribed test → One test report

---

## 🚀 Purpose

This ERD is designed to:

* Maintain clean separation between operational and medical data
* Enable scalability for growing clinics
* Ensure traceability across consultations, diagnostics, and billing
* Support efficient querying and reporting

---

