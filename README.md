# REBO - Restaurant Booking System

## Authors

- Trương Công Thiên Phú
- Đặng Quang Hưng

## Introduction
REBO is a comprehensive digital platform designed to bridge the gap between diners and restaurant owners. By digitizing the entire reservation lifecycle—from discovery and booking to service completion and feedback—REBO ensures transparency, reliability, and operational efficiency for both parties.

## 🚀 Vision
Our vision is to build a simple and trustworthy restaurant booking ecosystem. We solve the common pain points of manual reservation management, such as unclear table availability, hidden surcharges, and the lack of verified customer feedback.

## 🛠 Tech Stack

- **Frontend:** Next.js (TypeScript)
- **Backend:** Java Spring Boot
- **Database:** PostgreSQL
- **Design:** Figma

## ✨ Key Features

The system supports three primary user roles: **Customers**, **Restaurant Merchants**, and **Administrators**.

### 👤 For Customers
- **Restaurant Discovery:** Search by name, area, or specific dishes.
- **Real-time Booking:** View table types, capacity, and live availability before selecting a preferred slot.
- **Transparent Pricing:** Automated calculation of booking fees and surcharges for extra guests.
- **Secure Payments:** Integrated payment flow to secure reservations.
- **Feedback Loop:** Submit ratings and reviews after completing a meal.

### 🏪 For Restaurant Owners
- **Merchant Dashboard:** Manage restaurant profiles, operating hours, and location data.
- **Inventory Management:** Control table categories, seating capacities, and dynamic booking prices.
- **Digital Menus:** Upload and update dish lists to help customers decide.
- **Order Management:** Accept, decline, or update the status of incoming reservations.

### 🛡️ For Administrators
- **Merchant Verification:** Review business licenses and approve restaurant registrations.
- **System Oversight:** Handle complaints, moderate reviews, and manage platform listings.

## 🔄 Core Business Processes

1.  **The Booking Flow:** Users find a restaurant $\rightarrow$ Select table type & time $\rightarrow$ System validates availability $\rightarrow$ User confirms & pays $\rightarrow$ Booking is created.
2.  **The Service Flow:** Merchant confirms the booking $\rightarrow$ Customer arrives $\rightarrow$ Merchant updates status to "In Service" $\rightarrow$ Merchant marks as "Completed."
3.  **The Feedback Flow:** Once the service is marked complete, the customer is prompted to leave a rating and review on the restaurant's profile.

## 🛡️ Security & Quality (NFRs)

* **RBAC:** Strict Role-Based Access Control between Users, Merchants, and Admins.
* **Data Integrity:** Secure storage of personal data and payment logs.
* **Availability:** Target uptime of 99.5% for reliable booking services.
* **Audit Logs:** Detailed history tracking for every status change in a booking to prevent disputes.

## 📈 Roadmap

- **Release 1 (MVP):** Core booking, merchant onboarding, and basic rating system.
- **Release 2:** Dispute management, advanced search filters, and quick order tracking.
- **Release 3:** Real-time analytics for merchants and promotional/loyalty features.