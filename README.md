# SpendSmart – Personal Budget & Expense Tracker

SpendSmart is a personal finance mobile and web application designed to help users track expenses, manage budgets, and gain clear insight into their spending habits. The app focuses on simplicity, privacy, and fast interaction without requiring users to link bank accounts.

---

## Overview

SpendSmart allows users to:
- Track daily expenses in seconds  
- Set monthly budgets by category  
- View spending summaries and trends  
- Analyze financial habits through visual reports  
- Maintain full control over their financial data  

The goal is to provide a clean, lightweight alternative to complex budgeting tools.

---

## Key Features

### Expense Tracking
- Add income and expenses quickly  
- Assign categories (Food, Rent, Travel, Entertainment, etc.)  
- Edit or delete transactions  
- Optional notes for each entry  

### Budget Management
- Monthly budget setup per category  
- Overall spending limit tracking  
- Real-time progress indicators  
- Alerts at 75% and 100% of budget usage  

### Dashboard
- Total spending overview  
- Recent transaction list  
- Budget progress visualization  
- Quick financial summary  

### Reports
- Monthly spending breakdown  
- Pie and bar chart visualization  
- 6-month spending trends  
- Export reports as PDF or CSV  

### User Accounts
- Email/password authentication  
- Google OAuth login support  
- Secure JWT-based sessions  
- Password recovery option  

---

## Platform Support

### Mobile
- Android (Android 10+)  
- iOS (iOS 15+)  

### Web
- Fully responsive browser version  
- Supported browsers: Chrome, Firefox, Safari, Edge  

---

## Tech Stack

### Front-End
- React Native (Mobile)  
- React.js (Web)  
- TypeScript  
- Redux Toolkit  
- Material UI / React Native Paper  
- Victory Native / Recharts (Data Visualization)  

### Back-End
- Node.js + Express.js  
- PostgreSQL (Primary database)  
- MongoDB (Preferences & notifications)  
- JWT Authentication  
- Google OAuth 2.0  
- Firebase Cloud Messaging  

### Infrastructure
- AWS EC2 / RDS / S3  
- Git & GitHub version control  

### APIs
- ExchangeRate API (currency conversion)  
- Firebase (push notifications)  
- Plaid (planned future integration)  

---

## Architecture

SpendSmart uses a hybrid database approach:
- PostgreSQL handles structured financial data such as users, transactions, and budgets  
- MongoDB stores flexible data like user preferences and notification settings  

This ensures both performance and scalability depending on data type.

---

## Design Philosophy

The app is designed with a minimal and user-focused approach:
- Clean black-and-white interface  
- Simple navigation structure  
- Fast one-handed interaction  
- Material Design icons  
- Reduced clutter for better usability  

---

## Core Screens

### Login Screen
- Email/password login  
- Google sign-in option  
- Simple onboarding flow  

### Dashboard
- Monthly financial summary  
- Budget progress indicators  
- Recent transactions  
- Floating action button for quick expense entry  

### Add Expense Screen
- Quick amount input  
- Category selection grid  
- Optional notes and receipt attachment  
- One-tap save  

### Reports Screen
- Monthly selector  
- Pie and bar charts  
- Transaction history  
- Export options  

---

## Project Status

**Status:** Final / Production Ready  
**Development Cycle:** Completed (16-week project timeline)

---

## Future Improvements

- Bank syncing via Plaid integration  
- AI-based spending insights  
- Cloud sync across devices  
- Advanced financial forecasting  
- Dark mode UI  

---

## Purpose

SpendSmart was created to solve the problem of inconsistent and overly complex budgeting tools. It provides a fast, private, and easy way for users to understand and control their finances without unnecessary features or subscriptions.

---

## License

This project is part of a course-based academic submission and is intended for educational purposes.
