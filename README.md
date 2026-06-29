# SpendSmart – Personal Budget & Expense Tracker
### Application Outline Report – Updated | Version 1.1 | Week 4 Update

---

## I. Version Changelog

| Version | Date | Changes Made | Status |
|---------|------|--------------|--------|
| v1.0 | Week 1 | Initial outline submitted -- project description, problem statement, platform, front/back end, functionality, and wireframe descriptions | Complete |
| v1.1 | Week 4 | Added changelog section, refined functionality details, updated database plan to clarify PostgreSQL vs MongoDB usage, added notes on API error handling | Current |
| v1.2 | Week 7 | Code pushed to GitHub -- working login screen, expense entry screen, and basic dashboard; README updated to reflect current build | In Progress |
| v2.0 | Week 8 (Final) | Final submission -- all core screens complete, budget logic implemented, reports screen functional, full README and Wiki updated | Planned |

### Summary of Changes This Week (v1.1)

Since the initial outline was submitted in week 1, a few things have been adjusted based on a better understanding of the scope:

- Clarified the database structure -- PostgreSQL handles all the core transactional data (users, expenses, budgets) while MongoDB is just for preferences and notification settings since that data doesn't need to be relational
- Expanded the functionality section to include notes on how the app will handle API errors and connectivity issues -- something I forgot to think about in the first draft
- Removed the Plaid integration from the core plan and moved it to a future enhancement. It adds a lot of complexity and isn't really necessary to demonstrate the core functionality of the app
- Updated the wireframe section to be more specific about navigation flow between screens

---

## II. Project Description

SpendSmart is a budget and expense tracking app built for people who want to actually know where their money is going. The idea came from personal experience honestly -- I'd try to keep track of spending in a notes app or spreadsheet and it would last maybe two weeks before I stopped. Other apps I tried were either way too complicated or kept pushing me to connect a bank account which wasn't something I was comfortable with.

SpendSmart is meant to be the middle ground: simple enough to use every day, but detailed enough to give real insight into spending habits.

- **App Name:** SpendSmart – Personal Budget & Expense Tracker
- **Who it's for:** People who want to track spending without a huge learning curve -- mainly college students and young adults
- **What it does:** Quick expense logging, monthly budgets per category, and simple reports
- **Timeline:** 16 weeks (this semester)

---

## III. Problem Addressing

Most people have no idea what they actually spend in a month until they check their bank account and it's lower than expected. The tools that exist are either overkill or just not useful enough to keep using.

### A. The Problems
- Manually tracking expenses in a notes app or spreadsheet stops working pretty fast
- You don't realize you've gone over budget until it's already happened
- A lot of budget apps require linking a bank account or paying for a subscription to get anything useful
- Looking back at spending patterns across multiple months is basically impossible with most free tools

### B. What This App Does About It
- Logging an expense takes less than 10 seconds -- just amount, category, done
- Notifications go out before you actually hit your limit, not after
- No bank linking needed, everything is entered manually so it stays private
- Monthly reports let you compare spending month to month in a simple chart

---

## IV. Platform

### A. Mobile (main platform)
- iPhone and iPad -- iOS 15 and up
- Android phones -- Android 10 and up

### B. Web (secondary)
- Browser version for people who want to check things on a computer
  - Works on Chrome, Firefox, Safari, Edge

### C. Distribution
- App Store and Google Play for mobile
- Web version hosted through AWS

---

## V. Front/Back End Support

### A. Front End
- React Native for mobile, React.js for the web side
- Keeping components shared between both as much as possible to save time
- Material UI and React Native Paper for the visual components
- Redux Toolkit for managing app state
- TypeScript to keep the code cleaner and catch errors early
- Charts handled by Victory Native (mobile) and Recharts (web)

### B. Back End
- Node.js and Express for the API
- PostgreSQL for the main database -- users, transactions, budget settings
  - MongoDB for storing preferences and notification settings since that data is less structured
- Auth done with JWT tokens, Google login supported through OAuth 2.0
- Hosted on AWS (EC2, RDS, S3)
- Firebase for push notifications
- Git and GitHub for version control throughout the project

### C. Outside APIs
- ExchangeRate-API -- for handling different currencies
- Plaid -- moved to future enhancement, not part of core build

---

## VI. Functionality

### A. Accounts / Login
- Create an account with email and password or sign in with Google
- Standard password reset through email
- Token-based sessions so you stay logged in without it being a security issue

### B. Adding Expenses
- Tap add, enter the amount, pick a category, optionally add a note -- that's it
- Built-in categories: Food, Transportation, Housing, Entertainment, Health, Shopping, Other
- Can add custom categories if the defaults don't cover something
- Edit or delete entries if you mess up

### C. Budgets
- Set a limit for each category at the start of the month
- Can also set one overall monthly spending cap
- Progress bars on the home screen so you can see where you stand
- Notifications go out at 75% and 100% of whatever limit you set

### D. Dashboard and Reports
- Home screen gives a quick snapshot -- how much you've spent, recent transactions, budget status
- Pie chart breaking down where money went by category
- Line chart showing the last 6 months so you can spot patterns
- Export the whole report as a PDF or CSV if you need it

### E. Settings
- Change currency
- Turn notifications on or off
- Update account info
- Download your data or delete your account

---

## VII. Design / Wireframes

Full wireframes are being built in Figma and will be attached in the next submission. Navigation flow has been updated since v1.0 -- the Add screen is now accessible from any screen via a floating button rather than only through the bottom nav bar.

### A. Login Screen
- Logo up top, centered
- Email and password fields
- Sign In button, Google login option below it
- Link to sign up if you don't have an account yet

### B. Home / Dashboard
- Greeting at the top with the current month shown
- Big summary card showing total spent vs budget remaining
- Row of category cards you can scroll through, each with a small progress bar
- List of your last few transactions underneath
- Nav bar at the bottom: Home, Reports, Settings + floating Add button

### C. Add Expense Screen
- Amount field front and center, big enough to tap easily
- Category picker below it as a grid of icons
- Date defaults to today but you can change it
- Small text field for a note if you want one
- Option to attach a photo of a receipt
- Save button at the bottom

### D. Reports Screen
- Pick which month you want to look at up top
- Pie chart and bar chart for that month's spending
- Scrollable list of all transactions for the month
- Export button at the bottom

### E. General Design Choices
- Keeping it black and white, clean and minimal
- Font will be Inter or something similar, nothing fancy
- Using Material Design icons since they're consistent and recognizable
- Making sure contrast and text sizes meet accessibility standards

---

*SpendSmart | Outline v1.1 | Week 4 Update*
