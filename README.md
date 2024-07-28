## Expenses Sharing Application

#Objective

Design and implement a backend for a daily-expenses sharing application. This application allows users to add expenses and split them based on three methods: exact amounts, percentages, and equal splits. It manages user details, validates inputs, and generates downloadable balance sheets.

#### Features

1.User Management
Each user has an email, name, and mobile numb
Users can be created and retrieved via API endpoints.

2.Expense Management
Users can add expenses and split them among participants.

3.Three methods of splitting expenses:
Equal: Split equally among all participants.
Exact: Specify the exact amount each participant owes.
Percentage: Specify the percentage each participant owes (ensuring percentages add up to 100%).

4.Balance Sheet
Show individual expenses.
Show overall expenses for all users.
Provide a feature to download the balance sheet.

### Queries
* Add User: 
**(Input Format)**: Add_User [name] [Email] [PhoneNumber]


* Add Equal Expense to User Account:
**(Input Format)** : Add_Expense [ExpenseName] [totalAmount] [paidBy UserId] [createdBy UserId] [totalUsers] Equal [User 1 Id] [User 2 Id] .....[User totalUsers Id]


* Add Exact Expense to User Account:
**(Input Format)** : Add_Expense [ExpenseName] [totalAmount] [paidBy UserId] [createdBy UserId] [totalUsers] Exact [User 1 Id] [User 2 Id] ......[User totalUsers Id] [Amount Paid by User 1] [Amount Paid by User 2] ......


* Add Percent Expense to User Account:
***(Input Format)*** : Add_Expense [ExpenseName] [totalAmount] [paidBy UserId] [createdBy UserId] [totalUsers] Percent [User 1 Id] [User 2 Id] ......[User totalUsers Id] [Percent Share by User 1] [Percent Share by User 2] .....

### Sample Test Case

* Add_User jasmin jasmin@j.com 9876543876
* Add_Expense Food 200 1 1 3 Equal 1 2 3
* Add_Expense car 100 1 1 3 Exact 1 2 3 40 50 10
* Add_Expense Shopping 400 4 4 3 Percent 2 3 4 30 50 20
* Show_All_User_Balance
* Show_User_Data 2
* Show_User_Expense 1
