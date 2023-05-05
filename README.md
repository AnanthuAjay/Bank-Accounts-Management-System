# Bank Accounts Management System

This project is a software development project for creating a banking application. The application is used to maintain customer account details, specifically SavingsBankAccount with the bank. The bank officials are able to create new accounts, update account details, calculate interest, withdraw money, and deposit money. The project includes multiple exercises that build on each other, including creating a base Account class and sub classes for different account types, implementing encapsulation, inheritance, and interfaces. The final exercise involves creating a generic service class and using casting to call the subtype methods. This project is for software developers looking to practice their object-oriented programming skills and apply software design principles to create a functional banking application.


## Made for

This project is made to be ultized for:

- Programming beginners who are looking to learn Java programming and want to gain experience in object-oriented programming.
- Also, provides a good opportunity for more experienced Java developers to practice their skills and deepen their understanding of these concepts.


## Roadmap

Create an new java project on an IDE of your choice.
- 	Project Requirement

	A bank requires an application which is used to maintain customers account details.
	Customers can have SavingsBankAccount with the bank.
	The bank officials need to do the following operations on these accounts.

	1.Create a new account for customers

	2.Update account 
    
	3.Calculate interest

	4.Withdraw money
    
	5.Deposit money

	Now write a Account class with instance variables accountNumber,accountHolderName, Balance
	Write a method withdrawMoney(float amountToWithdraw)

	Write a main class, which will create a Account object and populate values 
	to the instance variables and call 
	the withdrawMoney() method.

	Apply encapsulation to your code so that the balance will be hidden and only accessed through accessor method.




- 	Now, Additional project requirement came up.

	The bank officals would like to add more account types such as SBAccount FDAccount,CurrentAccount, LoanAccount
	Apply inheritance and refactor your code to have Account as your base class and all the other classes are sub classes of Account class.
	Move the generic variables and methods to the base class. Include specific vairables and methods to the sub classes.

	Hint

	FDAccount has tenure, autoRenewal (boolean) etc

    CurrentAccount has overDraftLimit

	LoanAccount has EMI, loanOutStanding, tenure

- Now, Add a  feature for calculating interest for each account.
	You use the HAS-A relationship principle for that by creating a new class InterestCalculator and use that inside the each of accont type as reference.
	Call the calculateInterest() method of InterestCalculator inside the calculateInterst() method of SBAccount/FDAccount.

	Hint

	Simple interest =pnr/100 

    p--principal 

    n=period

    r=rate of interest

    sb account=4%

    fd account =7%


- Need to include the feature 'Automatic renewal of fixed deposit tenure' for the account. It is not applicable to all type of accounts. As it only applicable to FDAccount. It is not appropriate to have this feature in base class.

	So write a interface Renewable with abstract method autoRenewal(int tenure) and implement this interface in the FDAccount class.

	Hint

	Simple interest =pnr/100 Have a instance variable maturity date in your FDAccount. Check if isAutoRenewal is true if it is true then check if the maturity date is less than or equal to current date then do auto renewal for the period equal to the tenure and update maturity date with new maturity date which is equal to current date+tenure.

- Each type of account should have specific implementation of interest calculation.

	Solution:
    Override the calculateInterest() method of base class Account in the sub classes.
    Hint
    ----
    Use the formula for calculating simple interest simple Interest = (P * r * t)/100
    
    Assume t= 1 year
    
    For SBAccount use a interest rate 5%
    
    For FDAccount use a interest rate 7%

- Provide constructor for your classes.

- Create overloaded version of calculateInterest() method in InterestCalculator for calculating interest of SBAccount and FDAccount.

- Provide interface ICalculator for the concrete class InterestCalculator and use that interface
in your code for calling the methods.

- Write a Generic service class and create Account object and objects of its sub types.
Use casting to call the sub type methods

