# GroceryGo Privacy & Account Support Website

A standalone, lightweight, static legal and privacy portal for the **GroceryGo** mobile grocery delivery service operating in **Sahiwal, Punjab, Pakistan**.

## Overview

This website provides official privacy documentation and account deletion procedures meeting Google Play Developer policy requirements.

### Architecture & Design
- **100% Static HTML5 & CSS3:** No frontend frameworks, zero JavaScript runtime dependencies, loads instantly in any browser.
- **Privacy-First:** Zero cookies, zero tracking scripts, zero third-party analytics, and zero external runtime dependencies.
- **GroceryGo Branding:** Custom styling using official brand colors (Orange `#FF6B00`, Charcoal `#1A1C1E`, Clean White/Off-White `#F8F9FA`).
- **Mobile Responsive:** Seamless layout across mobile phones, tablets, and desktop displays.

## Pages

1. **`index.html`** — Legal and support landing hub linking to the Privacy Policy, Account Deletion guide, and contact channels.
2. **`privacy.html`** — Comprehensive Privacy Policy accurately detailing data collection, processing, service providers (Firebase, OtpBird), payment model (Cash on Delivery), and user rights.
3. **`delete-account.html`** — Dedicated Google Play compliant Account Deletion Resource detailing both in-app deletion (`Profile > Danger Zone > Delete Account`) and email deletion requests, with full transparency on deleted vs. retained data.
4. **`styles.css`** — Clean, modular vanilla CSS design system.

## Verification of Backend Alignment

- **Authentication:** WhatsApp OTP authentication via OtpBird. No passwords stored.
- **Payment Method:** Cash on Delivery (COD) exclusively. No credit card or banking details collected.
- **Account Deletion:** Verified against the backend `deleteMyAccount` Cloud Function:
  - Saved delivery addresses in `users/{uid}/addresses` are permanently deleted.
  - User identity in Firebase Authentication is deleted.
  - Firestore user profile is anonymized (`fullName: "Deleted User"`, `phone: "Deleted"`, email and notification tokens cleared).
  - Past completed order logs are retained for accounting, delivery fulfillment verification, and tax purposes.

## Contact

- **Service:** GroceryGo
- **Location:** Sahiwal, Punjab, Pakistan
- **Email:** grocery.pk.store@gmail.com
