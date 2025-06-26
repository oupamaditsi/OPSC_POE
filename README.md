 BudgetBuddy – Final Project Report 

Open-Source Coding (Final Submission) 

Group Members: 

Name 

Student Number 

Kone Moshapo 

St10365593 

Lwane Maditsi 

St10307990 

Tswelopele Lemaoana 

St10222552 

Ntokozo Molefe 

St10376406 

 

1. Introduction 

1.1 Purpose of the App 

BudgetBuddy is a personal finance mobile app designed to simplify the process of tracking and managing expenses. It turns a typically stressful activity into an intuitive and even enjoyable experience through the use of gamification and interactive visuals. 

The app encourages users to: 

Track daily expenses with ease 

Stick to monthly budgets 

Identify spending patterns 

Celebrate financial discipline through rewards 

By incorporating psychological motivators like badges and challenges, BudgetBuddy supports the development of long-term financial habits in a fun and meaningful way. 

 

2. App Features & Functionalities 

2.1 Core Features 

Feature 

Description 

User Registration/Login 

Secure local authentication using SHA-256 hashed passwords. 

Expense Categories 

Users can create custom categories like Groceries, Bills, Entertainment, etc. 

Expense Logging 

Users can add expenses with amount, date, description, and category. 

Receipt Attachment 

Users can upload or capture a photo of a receipt (compressed image). 

Budget Setting 

Users can set a monthly budget and per-category limits. 

Expense Filtering 

View expenses by user-selected date ranges and categories. 

Receipt Viewing 

Access attached receipt images through the expense list. 

Total Spent Per Category 

Automatically calculates total per category for a selected date range. 

Local Storage 

All data is stored offline using SQLite. 

2.2 Advanced Features 

Feature 

Description 

Spending Graphs 

Line and pie charts for daily, weekly, or monthly tracking using MPAndroidChart. 

Budget Dashboard 

Visual dashboard showing how close the user is to budget limits. 

Overspending Alerts 

Categories that exceed budget limits are highlighted in red. 

Gamification 

Users earn badges for habits like staying under budget or logging daily expenses. 

Financial Challenges 

“No-Spend Weekend” or “7-Day Log Streak” challenges with rewards. 

 

3. Design Considerations 

3.1 UI/UX Design 

The design of BudgetBuddy prioritizes: 

Simplicity: Clean interface to prevent cognitive overload. 

Consistency: Material Design guidelines followed for familiar navigation. 

Accessibility: Clear fonts, color contrast, and visual indicators. 

3.2 Navigation Flow 

Users move through intuitive screens such as: 

Login/Register → Dashboard → Add/View Expenses → Budget Overview → Gamification 

3.3 Mockups 

All screen mockups were created using Figma. Each screen was reviewed and improved based on: 

User feedback 

Visual clarity 

Navigation ease 

 

4. Database Design 

The app uses SQL as a local storage solution. The database includes the following tables: 

Users: id, username, hashed_password 

Categories: id, name, user_id 

Expenses: id, amount, date, description, category_id, receipt_image_path 

Budget: id, user_id, monthly_limit, category_limit 

Achievements: id, user_id, type, date_earned 

Data integrity and normalization were maintained to ensure consistent performance and scalability. 

 

5. GitHub & Youtube Video 

5.1 Repository 

Project hosted on GitHub: https://github.com/ntok-29/OPSC_POE.git 

Video posted by:https://youtube.com/shorts/Pn857j0nkcs 

 

6. GitHub Actions  

We implemented GitHub Actions for automated builds and tests to ensure code quality.  

This pipeline ensures: 

Clean builds on every push to main 

Early detection of errors 

Time-saving automation 

 

7. Testing & Evaluation 

7.1 Testing Methods 

Manual testing of all core features 

Usability testing with student volunteers 

Bug tracking and iterative improvements 

7.2 Results 

All core features performed as expected 

Usability feedback was positive 

Areas for future improvement: multi-device sync and notification reminders 

 

8. Challenges & Solutions 

Challenge 

Solution 

Offline image storage 

Implemented image compression and saved paths in DB 

Tracking trends 

Used MPAndroidChart for dynamic data display 

App engagement 

Gamification elements (badges, challenges) to motivate usage 

 

9. Conclusion 

BudgetBuddy combines practical financial tools with engaging design to help users build better money habits. Through intuitive features, secure local storage, and positive reinforcement (via gamification), the app turns budgeting into a rewarding daily habit. 

 

10. References 

Google ML Kit Documentation 

MPAndroidChart GitHub Repository 

Material Design Guidelines (2023) 

Journal of Behavioral Finance (2024) – “Gamification in FinTech” 

Android Developer Docs: SQLite, File Storage, Camera Access 

 


***BudgetBuddy source code Final Part***

BudgetBuddy is an intuitive personal finance app designed to make budgeting 
engaging rather than stressful. By incorporating gamification elements and visual 
feedback, it encourages users to develop healthy financial habits. 

Video presentation:  

DOCUMENTATION OF THE APP (MANUAL):
1. New users will be required to create an account by entering their email address, username and password.
2. For returning users, only the email and password will be required to access the account.
3. After logging in/signing up you will then see the dashboard of the app. The dashboard contains the current balance, expenses balance, budget progress
and the transactions tab for all the transactions you've made.
4. Whilst on the dashboard, you will see a bottom navigation bar which allows you to access other tabs in the app like the budget page, chart page and the settings page.
5. You can also log your income and expenses (e.g. Entertainment, Transport, Rent, Tuition, etc..) with their own categories so you can keep track of your budget easily.
6. In the Charts page the user will be presented with a pie chart of all your expenses, savings, etc. This is the most effective way you can keep track of your overall funds.
7. There will also be achievements depending on how much you've saved on a monthly basis to keep the user motivated. And many more features in the application.
8. Then lastly you have your settings page where you can change your username, password, and a bunch of other settings in there.


BudgetBuddy transforms financial management through: 
Behavioral Psychology: Gamification encourages consistent use 
Finance Assistance: Smart suggestions prevent budget fatigue 
Family Focus: Multi-user support for household budgets
