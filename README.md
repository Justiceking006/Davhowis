# MLM Referral System – Backend Guide

## Overview

This project is a **multi-level marketing (MLM) web application** where users register with an onboarding fee using a system-generated pin (coupon code) and refer others to advance through referral tiers (TRs). Each referral tier has specific rules and commission percentages. 

This README is your complete guide to building the backend for both the **Admin Dashboard** and the **User Profile/Dashboard**.

---

## System Architecture

- **Frontend**: Handled separately using Tailwind CSS.
- **Backend**: Built using **pure PHP (no frameworks)**.
- **Database**: MySQL (assumed).
- **Deadline**: **May 16, 2025**
- **Time Commitment**: ~2 hours/day.

---

## Core Entities

- **Users**
- **Referral Links / Tree**
- **Tiers (TR1, TR2, …)**
- **Admin**
- **Transactions (Registration, Tier Purchases)**
- **Coupon Codes (Pins)**

---

## Features & Responsibilities

### 1. User Dashboard/Profile

Each registered user should have access to a dashboard with the following features:

- **Referral Link Display**
- **Referral Tree Visualization**
  - Show number of referrals
  - Show referral levels (e.g., TR1, TR2, etc.)
- **Earnings & Commission Summary**
- **Tier Progress**
  - Current TR tier
  - Requirements to move up
- **Manual Tier Purchase Option**
- **Referral Stats**
  - Total referrals
  - Active referrals
- **Payment History**
- **Profile Info Editing**
- **Pin Entry during signup (validated from DB)**

### 2. Admin Dashboard

Admin panel must include:

- **View All Users**
- **View Referral Trees**
- **Generate & Manage Pins**
  - Mark pins as used/unused
  - Assign pins to WhatsApp-verified users
- **Track Payments**
  - Registration payments
  - Tier upgrade payments
- **Commission Settings**
  - Set commission % for each tier
- **View Tier Rules**
  - TR1 requires 10 direct referrals, TR2 requires 10 from each of 10, etc.
- **Tier Color Coding and Customization**
- **User Management**
  - Upgrade/downgrade tier manually
  - Block/suspend user
- **Basic Analytics**
  - Total revenue
  - Number of users per tier
  - Referral conversion rates

---

## Backend Development Plan (May 9–May 16)

Total Working Days: 8  
Time per Day: 2 hours  
Total Time: 16 hours

| Date       | Task                                                                 |
|------------|----------------------------------------------------------------------|
| May 9      | Set up database schema (users, referrals, pins, tiers, payments)     |
| May 10     | Implement registration with pin validation + login system            |
| May 11     | Build user dashboard: profile + referral link generation             |
| May 12     | Build referral tree logic + tier progression logic                   |
| May 13     | Implement payment tracking + manual tier purchase backend            |
| May 14     | Build admin dashboard: view users, manage pins, commissions          |
| May 15     | Add tier rules logic, stats, analytics, TR color coding              |
| May 16     | Final testing, bug fixes, documentation, deployment prep             |

---

## Optional Enhancements (Post MVP)

- Email notifications
- WhatsApp integration for pin delivery
- Responsive API for mobile version
- 2FA for admin

---

## Notes

- Keep code modular and well-commented.
- Use sessions for login state.
- Prevent referral fraud (one device/multiple accounts).
- Consider pagination for large user/commission datasets.

---

## Communication

- Use GitHub commits and short daily notes to show progress.
- Collaborate with frontend dev (Jusytech) to match UI expectations.
