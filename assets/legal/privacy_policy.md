# TRADEBENCH (PTY) LTD — PRIVACY POLICY

**Version:** 1.0  
**Effective Date:** 1 October 2026  
**Governing Law:** Republic of South Africa (Protection of Personal Information Act No. 4 of 2013 — **POPIA**)

---

## 1. Summary and Introduction

Tradebench (Pty) Ltd ("**Tradebench**", "**we**", "**us**", or "**our**") respects your privacy and is dedicated to safeguarding your personal information in strict compliance with the Protection of Personal Information Act No. 4 of 2013 (**POPIA**) and international mobile application marketplace standards.

Tradebench operates a construction trade-profile, credential verification, and contractor-discovery platform comprising the mobile application, website, PDF CV generator, search tools, and administrative portals (collectively, the "**Platform**").

This Privacy Policy applies to all registered users and visitors:
- **Contractors (Work Seekers)**: Skilled tradespeople who create profiles, progress through verification tiers, generate digital PDF trade CVs, and showcase their workmanship.
- **Hirers (Work Givers)**: Contractors, subcontractors, businesses, project managers, foremen, and individuals searching for, shortlisting, and unlocking contact details of Contractors.

---

## 2. Responsible Party and Information Officer

For purposes of POPIA, Tradebench (Pty) Ltd acts as the Responsible Party for the personal information processed through the Platform.

- **Company Name:** Tradebench (Pty) Ltd
- **Physical Address:** South Africa
- **Information Officer:** Tradebench Privacy Desk
- **Privacy & Support Contact:** support@tradebench.co.za / privacy@tradebench.co.za

---

## 3. Personal Information We Collect

We adhere to the principle of data minimisation. We only collect personal information that is necessary for account security, geolocation-based trade discovery, tiered credential verification, and facilitating lawful contact between Hirers and Contractors.

> **NO EMAIL ADDRESSES COLLECTED:**  
> Tradebench uses cellphone numbers and One-Time PIN (OTP) SMS verification as the primary authentication and account management mechanism. We do not collect or process personal email addresses from users during registration or onboarding.

### A. Account Creation & Authentication (All Users)
When registering an account via the Sign-Up screen, we collect:
- Full Name
- Cellphone Number (verified via 6-digit SMS OTP)
- Account Password (stored in securely hashed and salted format)
- Account Role Selection (*Contractor* or *Hirer*)

### B. Hirer (Work Giver) Information
During Hirer onboarding and profile setup:
- Profile photograph
- Operating location (suburb, province, country, and geographic coordinates via Google Places)
- Account entity classification (Individual Hirer vs. Company)
- Company name (if registering on behalf of an enterprise or business)
- Subscription and unlock balance records (subscription tier, monthly unlock allocations, and unlock history)

### C. Contractor (Work Seeker) Information & Verification Tiers
Contractor information is structured across three verification tiers:

1. **Tier 1 (General Trade Information)**: Profile photo, primary and secondary trade categories (e.g., plumbing, electrical, carpentry, bricklaying), years of industry experience, tool ownership, transport availability, expected labour rates (hourly, daily, after-hours), and general location coordinates for radius filtering.
2. **Tier 2 (Portfolio, Bio & Professional References)**: Professional bio summary, project history (project titles, descriptions, completion dates, work photos), and two professional references:
   - Referee full names (displayed on public profile)
   - Referee cellphone numbers (strictly stored in Gated Private Data)
   *(Note: Contractors must obtain prior express consent from referee individuals before submitting their names and contact numbers).*
3. **Tier 3 (Identity Verification & Accredited Qualifications)**: Facial liveness selfie photo, government-issued Identity Document or Passport, trade certificates and qualifications, and verification status (*unverified*, *review*, or *verified*).

### D. Automatically Collected Device & Geolocation Data
1. **Device Geolocation (GPS & Geohashing)**: With your explicit permission, we access GPS coordinates to compute Geohashes via Google Places SDK to enable proximity-based search within a Hirer's selected radius.
2. **App Telemetry & Diagnostics**: Device model, operating system version, crash reports (via Firebase Crashlytics), and anonymised feature interaction analytics (via Firebase Analytics).

---

## 4. Purpose and Lawful Basis for Processing (POPIA)

We process personal information under the following lawful grounds established by POPIA:

- **User Authentication & Account Management**: Performance of Contract (POPIA s11(1)(b))
- **Trade Discovery & Radius Search**: Performance of Contract / Consent
- **PDF CV Generation & Export**: Performance of Contract (at user's request)
- **Tiered Verification & Trust Badging**: Performance of Contract & Legitimate Interest
- **Profile Unlock & Contact Exchange**: Performance of Contract
- **Security, Fraud Prevention & Moderation**: Legitimate Interest & Legal Obligation
- **Service Notifications & System Alerts**: Performance of Contract / Consent

---

## 5. Architectural Privacy: The Split-Document Model

To prevent unauthorized data harvesting, commercial spam, and bulk scraping, Tradebench enforces technical separation of user data at the database level:

- **Public Profile (`/users/{userId}`)**: Accessible by authenticated platform users. Contains: Full Name, Profile Photo, Trade Categories, Rates, Bio, Reference Names, Verification Badge, and Geohash Area.
- **Portfolio Data (`/users/{userId}/portfolio/data`)**: Accessible by authenticated users viewing contractor profiles. Contains: Project photos, project descriptions, completion dates, and verified certificate title labels.
- **Gated Private Data (`/users/{userId}/private/data`)**: STRICTLY RESTRICTED ACCESS. Contains: Contractor's direct cellphone number, referee cellphone numbers, identity documents, selfie photo, and raw certificate files.

**Access to Gated Private Data is permitted only to:**
1. The account owner (Contractor themselves)
2. Authorized Tradebench Administrators (for manual verification and safety moderation)
3. An approved Hirer with an active, recorded Unlock in `/unlocks/{hirerId}_{contractorId}`

---

## 6. How We Disclose and Share Information

Tradebench does not sell, rent, or trade your personal information. We disclose data only in the following defined scenarios:
1. **Between Platform Users**: Public profile information is visible to registered users browsing the platform directory. When a Hirer uses an unlock credit or subscription allowance to unlock a Contractor's profile, the Contractor's direct cellphone number is made visible to that specific Hirer.
2. **Technical Service Providers**: Google Cloud & Firebase (hosting, database, file storage, authentication, push notifications, Crashlytics, Analytics), Google Places SDK (location mapping), and In-App Payment Processors (Google Play Billing, Apple App Store).
3. **Legal Compliance & Protection**: When required to do so by South African law, court subpoena, or lawful police request.

---

## 7. Cross-Border Data Transfers

Tradebench utilizes Google Cloud / Firebase infrastructure. Personal information may be stored on secure cloud servers located outside the Republic of South Africa (e.g., in European Union or United States data centres). In accordance with Section 72 of POPIA, we ensure that the cloud provider is subject to laws or binding agreements that provide an adequate level of data protection substantially similar to POPIA.

---

## 8. Data Security and Safeguards

Tradebench implements appropriate technical and organisational measures to secure the integrity and confidentiality of personal information:
- End-to-end data encryption in transit (HTTPS / TLS).
- Server-side encryption at rest across all database collections and cloud storage buckets.
- Cloud Firestore Security Rules preventing direct querying or downloading of sensitive identification files and phone numbers without verified authorization.
- Administrative audit logging and role-based access restrictions.

---

## 9. Data Retention and Account Deletion

1. **Active Accounts**: We retain your information for as long as your account is active and necessary to provide you with the Platform services.
2. **Account Deletion (Right to be Forgotten)**: You can request the permanent deletion of your account at any time through the **Account Settings** tab in the app or by contacting **support@tradebench.co.za**. Upon deletion, your profile, portfolio photos, private documents, and contact details are permanently removed from active databases.
3. **Administrative & Audit Records**: Moderation notes, fraud-prevention flags, and report logs may be archived in restricted format for up to 3 years for legal compliance and risk management.

---

## 10. Your Rights Under POPIA

As a data subject under South African law, you have the right to:
1. **Request Access**: Ask whether we hold personal information about you and receive a copy.
2. **Request Correction / Rectification**: Update or correct any inaccurate, outdated, or incomplete information.
3. **Request Deletion / Destruction**: Request deletion of personal information we are no longer authorized to retain.
4. **Object to Processing**: Object on reasonable grounds to the processing of your personal information.
5. **Lodge a Complaint with the Regulator**: Submit a complaint to the South African **Information Regulator**:
   - **Website:** https://inforegulator.org.za
   - **Complaints Email:** POPIAComplaints@inforegulator.org.za / complaints.IR@justice.gov.za

---

## 11. Protection of Minors

Tradebench is intended exclusively for individuals aged **18 years and older** who are legally permitted to work and enter into commercial contracts. We do not knowingly register accounts or collect personal information from minors.

---

## 12. Changes to this Privacy Policy

We may update this Privacy Policy from time to time. When material changes are made, we will notify you through the app or require your renewed acceptance before proceeding.

---

## 13. How to Contact Us

For any questions, requests to exercise your POPIA rights, or concerns regarding this Privacy Policy:
- **Company:** Tradebench (Pty) Ltd
- **Email:** hello@tradebench.co.za
