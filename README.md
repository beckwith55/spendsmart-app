# SpendSmart – Personal Budget & Expense Tracker
### Application Outline Report | Version 1.0 | Mobile & Web

---

## I. Project Description

SpendSmart is a budget and expense tracking app built for people who want to actually know where their money is going. The idea came from a pretty common frustration -- most people either rely on spreadsheets (which are a pain to maintain) or download some bloated finance app that takes 20 minutes to set up and still doesn't tell you anything useful. SpendSmart is meant to be the middle ground: simple enough to use every day, but detailed enough to give you real insight into your spending.

- **App Name:** SpendSmart – Personal Budget & Expense Tracker
- **Target Users:** Mostly people in their 20s and 30s trying to get a better handle on day-to-day spending
- **Main Goal:** Let users log expenses quickly, set budgets by category, and see a clear picture of where their money goes each month
- **Project Timeline:** Built over a 16-week semester

---

## II. Problem Addressing

The core problem is simple: most people don't really know how much they spend or where. It's not that they don't care -- they just don't have a tool that makes tracking easy enough to stick with. Existing apps are either too basic or require linking bank accounts, which a lot of people aren't comfortable doing.

### A. Problems Being Solved
- Keeping track of expenses manually is tedious and most people give up within a week
- It's easy to blow past a budget when you have no real-time way to know how close you are
- Most free apps are cluttered with features people don't need or push you to pay for anything useful
- There's no easy way to look back at past months and spot trends in your spending

### B. How SpendSmart Addresses These
- Quick-entry expense logging -- adding a transaction takes under 10 seconds
- Budget alerts sent to your phone when you're getting close to a limit
- Clean monthly reports that show spending by category without overwhelming the user
- No bank linking required -- fully manual, which keeps it private and low-friction

---

## III. Platform

### A. Primary Platform – Mobile
- iOS (iPhone and iPad) -- requires iOS 15 or later
- Android -- requires Android 10 (API 29) or higher

### B. Secondary Platform – Web
- A browser-based version for users who prefer managing finances on a laptop or desktop
  - Works on Chrome, Firefox, Safari, and Edge (current and previous version)

### C. How It Gets to Users
- Mobile: distributed through the Apple App Store and Google Play Store
- Web: hosted on AWS, accessible through any modern browser

---

## IV. Front/Back End Support

### A. Front End
- React Native for mobile, React.js for the web version -- shared component logic where possible
- UI components: React Native Paper (mobile) and Material UI (web)
- State management handled with Redux Toolkit
- Charts and graphs: Victory Native on mobile, Recharts on web
- Written in TypeScript for better code reliability

### B. Back End
- Node.js with Express.js handling the REST API
- PostgreSQL as the main database -- stores users, transactions, and budget data
  - MongoDB used alongside it for user preferences and notification settings
- Login handled with JWT tokens; Google Sign-In supported via OAuth 2.0
- Hosted on AWS -- EC2 for the server, RDS for the database, S3 for any stored files
- Push notifications sent through Firebase Cloud Messaging
- Code managed with Git and hosted on GitHub

### C. Third-Party Integrations
- Plaid API: available as an optional add-on for users who want to auto-import bank transactions
- ExchangeRate-API: supports multiple currencies for users outside the US

---

## V. Functionality

### A. Login & Account Creation
- Sign up with an email and password, or use Google to log in faster
- Forgot password flow handled through email
- Sessions managed securely with token-based auth

### B. Logging Expenses
- Enter an amount, pick a category, add a date and optional note -- done
- Default categories: Food, Transportation, Housing, Entertainment, Health, Shopping, Other
- Users can create their own custom categories if needed
- Edit or delete any past entry

### C. Setting & Managing Budgets
- Set a spending limit for each category at the start of the month
- Set an overall monthly cap on top of the category limits
- Progress bars show how much of each budget has been used
- Get a push notification at 75% and again at 100% of any budget limit

### D. Dashboard & Reports
- Home screen shows a monthly summary, recent transactions, and budget health at a glance
- Spending breakdown by category shown as a pie chart
- Six-month trend line so you can see if your habits are improving
- Reports can be exported as a PDF or CSV

### E. Settings
- Switch between currencies
- Control which notifications you receive
- Update account info
- Export your data or delete your account entirely (GDPR compliant)

---

## VI. Design (Wireframes)

Full wireframe mockups will be built in Figma and included with the next submission. Below are the key screens planned for the app.

### A. Login / Registration Screen
- App logo and name centered at the top
- Email and password fields below
- Two buttons: Sign In and Continue with Google
- Link to create a new account at the bottom

### B. Home Dashboard
- Header shows a greeting, the current month, and the user's profile icon
- A summary card shows total spent vs. total budget with a circular indicator
- Category cards scroll horizontally, each showing a mini progress bar
- The five most recent transactions are listed below
- Bottom nav bar: Home, Add, Reports, Settings

### C. Add Expense Screen
- Large amount input at the top -- tapping brings up a number pad
- Category grid below for quick selection
- Date picker defaults to today but can be changed
- Optional description field and a camera icon for attaching a receipt photo
- Save button at the bottom

### D. Reports Screen
- Month picker at the top to flip between months
- Pie chart showing category breakdown for that month
- Bar chart showing spending week by week
- Full transaction list for the selected month below the charts
- Export button for PDF or CSV

### E. Visual Design Notes
- Color scheme: black and white primary, clean and readable
- Font: Inter or Roboto, kept simple with three size levels
- Icons from the Material Design set
- Accessibility: meets WCAG 2.1 AA contrast standards, supports larger text sizes

---

*SpendSmart | Application Outline | v1.0*
