# N26 Challenge
## Monefy Test Plan
Before starting the test plan, I did an exploratory test battery to understand the features and the application goal. Then, I wrote the following tests in order of prioritization I would use, and each block has its found issues:

Income
---------
- Create a new income with a valid value
> Example: 500, 500.99
- Create a new income using the calculator
> Example: 1000/2
- Create a new income with an invalid value
> Example: Insert values = 0
- Create incomes using diferents categories and check if it'll appear correctly in the balance 
> Example: Deposits, Salary, Savings
- Create incomes for differente accounts 
> Example: cash, paypal account, credit card
- Check if the incomes are being reported correctly on balance

Expense
---------
- Create a new expense with valid values
> Example: 100, 100.99
- Create a new expense using the calculator
> Example: 100/2
- Create a new income with an invalid value
> Example: Insert values = 0
- Create incomes using diferents categories
> Example: House, Pet, Bills
- Create an expense for differents accounts
> Example: cash, paypal account, credit card
- Check if the expenses are being shown correctly in the balance
- Check if the expenses are being shown correctly in the initial graphic 

Balance
---------
- Check if the balance value are correct according to the incomes/expenses registered
- Check if the incomes are being shown in balance
- Check if the expenses are being shown in balance
- Create a new income/expense from the balance screen
- Check if the records are organized by the correct category
- Change the balance filter to show the records by category
- Change the balance filter to how the records by day
- Edit a income/outcome register and check if the balance changed correctly
- Delete a record from balance and check if the value is correct 
> ### Found Issues
> 1. If you have accounts with different types of currency, the balance doesn't show two values. Instead, it will plus the balance of each account without considering the currency. 

Filters
----------
- Filter incomes/expenses by account
- Filter incomes/expenses by day
- Filter incomes/expenses by week
- Filter incomes/expenses by year
- Filter incomes/expense by "all" 
> Actually, I didn't understand well how this filter works. So it's supposed to show the records from the beginning of the app use? 
- Filter incomes/expenses using a interval of days
- Filter incomes/expenses using a especific day using "choose date"
> ### Found Issues
> 1. In the Interval filter, the history always shows the same interval instead of the last used filters. Besides, it isn't easy to understand if it's a history or a filter suggestion. 
> 2. The filter allows applying intervals of coming days.
> 3. After filtering using an interval and changing the filter for a day, week or month, the filter will use the data used for the "interval." Example: If you filter from 1st May to 30th May and change the filter to "day," the day shown is 1st May instead of the actual day.

Search
----------
- Search records using the category
- Search records using the value
- Click in the search result and check if it follows to edit income/expense screen

Transfer
----------
- Create a new transfer from one account to other
- Create a new transfer to the same account (it should not work)
- Check if the transfers appears in the ballance
- Check if the transfers appears in the graphic
> ### Found Issues
> 1. The transfers aren't shown in the balance or the graph if you don't use the filter by account.

Menu > Accounts
-----------------
- Create a new Account
- Edit a created account
- Create a transfer for a new account
- Disable an account
- Merge an account
- Delete an account
> ### Found Issues
> 1. When you merge an account, the application creates a backup file (I don't know if it is the expected behavior, but the app only gives message feedback for the backup and not for the merge).
> 2. It's possible to merge accounts with different types of currencies. For example, you can merge an account in BRL with another in USD.

Menu > Settings
-----------
### balance
- Active/Deactive budget
- Active/Deactive carry over
- Active/Deactive future recurring records
### general settings
- Active/Deactive dark theme
- Change language
- Change the currency 
- Change first day of the week 
- Change first day of the month
- Create a passcode protection with PIN 
- Activate touch ID/face ID as passcode 
- Check if the "Review Application" leads to an app store review page
- Check if the "Export to file" generates a csv file with all the monefy info. 
- Check if a pop up with the app info appear em "About Monefy" is selected. 
- Check if the purchade ID is being copied 
### synchronization
- Enable/Disable Google Drive synchronization
- Enable/Disable Dropbox synchronization
### data backup 
- Create a backup file
- Restore data from a backup data
- Clear data
> ### Found Issues
> 1. When the Budget is active, the balance shows a value even if you didn't put any income. Example: I set a budget of 10.000, and the balance changed to 333.33. 

Menu > Categories
-------------------
- Create a new category of expense 
- Edit a category of expense
- Delete a category of expense
- Repeat the flow above for the income categories

Menu > Categories
-------------------
- Edit the decimal places of a currency
- Create a rate for a currency